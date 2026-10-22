<div align="center"> 
  <h1> Sysmon Installation & Configuration </h1>
</div>

<h2>Overview</h2>
<p>Windows endpoint monitoring using Microsoft Sysmon. It focuses on collecting system telemetry, reviewing security events, investigating suspicious activity, and preparing basic detection logic for a SOC Analyst L1 workflow.</p>

<h2> Objectives</h2>
<ul>
  <li>- Install and configure Microsoft Sysmon.</li>
  <li>- Collect and analyze Windows endpoint events.</li>
  <li>- Practice basic security event triage.</li>
  <li>- Develop Splunk searches for endpoint monitoring.</li>
</ul>

<h2>Tools Used</h2>
<ul>
  <li>Window 10</li>
  <li>Powershell</li>
  <li>Window Event Viewer</li>
  <li>Splunk Enterprise</li>
  <li>Splunk Universal Forwarder</li>
</ul>


<h2>Installation Steps</h2>

<ul>
  <li>
    <strong>Step 1 — Download Sysmon</strong>
    <p>Downloaded Sysmon from the Microsoft Sysinternals website.</p>
  </li>

  <li>
    <strong>Step 2 — Extract Files</strong>
    <p>Extracted the Sysmon package on the Windows 10 virtual machine.</p>
  </li>

  <li>
    <strong>Step 3 — Open PowerShell as Administrator</strong>
    <p>Launched PowerShell with administrative privileges.</p>
  </li>

  <li>
    <strong>Step 4 — Install Sysmon</strong>
    <p>Executed the installation command:</p>
    <pre><code>sysmon64.exe -i</code></pre>
  </li>
</ul>

