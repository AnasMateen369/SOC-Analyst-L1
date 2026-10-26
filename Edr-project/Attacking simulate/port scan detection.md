


<h1>Nmap Port Scan Reconnaissance → Wazuh Detection Lab</h1>

<h2>Objective</h2>
<p>
Nmap is an open-source port scanning tool that we perform from the Kali Linux
(attacker perspective) against the Windows 10 victim endpoint to gather
information — a phase called <strong>reconnaissance</strong>.
</p>

<h2>Key Points</h2>
<ul>
  <li>Gather information via network reconnaissance.</li>
  <li>Monitor the Windows 10 endpoint.</li>
  <li>Detect suspicious behavior in the Wazuh dashboard.</li>
  <li>Properly analyze the alert in the SIEM — Wazuh Manager.</li>
</ul>

<h2>Attack Overview (Why Recon Matters)</h2>
<p>
Black-hat hackers and cyber attackers commonly perform <strong>Recon with
Passive or Active Port Scanning</strong> to identify infrastructure weaknesses
such as:
</p>
<ul>
  <li>Open ports</li>
  <li>Running unwanted services</li>
  <li>High / critical vulnerabilities</li>
</ul>

<h2>Setup Plan</h2>
<ul>
  <li><strong>Kali Linux</strong> — Attacker — <code>192.168.10.5</code></li>
  <li><strong>Windows 10</strong> — Victim — <code>192.168.10.7</code></li>
  <li><strong>Ubuntu Server</strong> — SIEM / Wazuh Manager — <code>192.168.10.6</code></li>
</ul>

<h2>Tools Used</h2>
<ul>
  <li>Kali Linux — <strong>Nmap</strong></li>
  <li>Windows — <strong>Sysmon</strong></li>
  <li>Wazuh — <strong>Monitor Alerts</strong></li>
</ul>



<h1>Nmap Scan Execution and Wazuh Investigation</h1>

<h2>Attack Preparation</h2>
<ul>
  <li>On the Windows victim machine, run <code>ipconfig</code> to confirm its IP address.</li>
  <li>From Kali Linux, ping the Windows host machine to confirm reachability.</li>
</ul>
<pre><code>ping &lt;windows_host_ip&gt;</code></pre>

<h2>Perform Nmap Scanning</h2>
<pre><code>nmap -sS &lt;windows_host_ip&gt;
nmap -Pn -p 3389 &lt;windows_host_ip&gt;</code></pre>
<p>Example:</p>
<pre><code>nmap -sS 192.168.10.7</code></pre>

<h2>What the Scan Actually Does</h2>
<ul>
  <li>
    <strong><code>-sS</code> (TCP SYN / half-open scan)</strong> —
    Sends a SYN packet to each port. If the target replies with SYN/ACK, the
    port is <em>open</em>; a RST/ACK means <em>closed</em>; no reply means
    <em>filtered</em>. The connection is never fully established, so it is
    stealthier and faster than a full connect scan. Requires root privileges.
  </li>
  <li>
    <strong><code>-Pn</code> (no ping / skip host discovery)</strong> —
    Treats the host as online and skips the initial ICMP echo probe, which is
    useful when the target blocks ping (common on hardened Windows hosts).
  </li>
  <li>
    <strong><code>-p 3389</code> (target port)</strong> —
    Limits the scan to RDP port 3389, testing whether Remote Desktop is
    exposed on the endpoint.
  </li>
</ul>
<p>
Each SYN sent to a closed port causes Windows to respond with a RST, and each
open port (e.g., 3389) returns a SYN/ACK. These raw TCP packets are captured by
Sysmon <strong>Event ID 3 (NetworkConnect)</strong> on the Windows endpoint and
forwarded by the Wazuh Agent to the Wazuh Manager, where correlation rules flag
the repeated connection attempts as reconnaissance.
</p>

<h2>Wazuh Alerts</h2>
<p>Wazuh generated alerts related to:</p>
<ul>
  <li>Network scanning activity</li>
  <li>Suspicious connection attempts</li>
  <li>Reconnaissance behavior</li>
</ul>
<p>The alerts were visible in the Wazuh dashboard.</p>

<h2>Investigation Process</h2>
<p>The following information was analyzed:</p>
<ul>
  <li>Source IP address</li>
  <li>Target endpoint</li>
  <li>Timestamp</li>
  <li>Alert severity</li>
  <li>Associated logs</li>
</ul>

<h2>Security Risk and Impact</h2>
<p>
Port scanning is an important indicator of early-stage attacker activity and
can help security analysts identify:
</p>
<ul>
  <li>Reconnaissance attempts</li>
  <li>Unauthorized scanning</li>
  <li>Potential intrusions</li>
</ul>


