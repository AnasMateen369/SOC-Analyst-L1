


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

