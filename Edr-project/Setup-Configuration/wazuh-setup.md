<div align="center"> <h1> Wazuh setup & Configuration </h1> </div> 
<h2>Overview</h2>
<p>deploymenting and configurating Wazuh as a security monitoring open-source platform. It includes an Ubuntu-based Wazuh server, a Windows endpoint agent, endpoint telemetry collection, and basic security event investigations.</p>

<h2>Objective</h2>
<ul>
  <li>Deploy Wazuh Manager, Indexer, and Dashboard.</li>
  <li>Enroll a Windows endpoint with the Wazuh Agent.</li>
  <li>Monitor endpoint security events.</li>
  <li>Integrate Sysmon event collection.</li>
  <li>Investigate alerts and document findings.</li>
  <li>Practice a SOC Analyst L1 workflow.</li>
</ul>

<h2>Technology Stack</h2>

<ul>
  <li>Ubuntu Server 22.04</li>
  <li>Wazuh Indexer</li>
  <li>Wazuh Dashboard</li>
  <li>Windows 10</li>
  <li>Wazuh Agent</li>
  <li>Microsoft Sysmon</li>
  <li>VirtualBox</li>
</ul>

<h2>Wazuh installation on Ubuntu Server</h2>
<pre>curl -sO https://packages.wazuh.com/4.7/wazuh-install.sh
sudo ./wazuh-install.sh -a -i </pre>
<ul>
  <li>Then Access Wazuh Dashboard Via Ubuntu (ip:443)</li>
</ul>


<h2>Sysmon Installation on window 10</h2>


<pre>
# Download Sysmon from Microsoft Sysinternals
# Download sysmonconfig.xml from SwiftOnSecurity GitHub
.\Sysmon64.exe -accepteula -i sysmonconfig.xml</pre>

<h2>install wazuh agent on window 10 like for endpoint</h2>
<ul>
<ol>Download Wazuh agent from Wazuh dashboard.</ol>
  <pre>Invoke-WebRequest -Uri https://wazuh.com -OutFile wazuh-agent.msi</pre>
<ol>Second install, enter Ubuntu Server IP as the Wazuh manager address.</ol>
  <pre>msiexec.exe /i wazuh-agent.msi /q WAZUH_MANAGER="192.168.10.6"</pre>
<ol>Start the Wazuh agent service on window.</ol>
<ol>Verify agent appears as Active in Wazuh dashboard can be visible.</ol>
</ul>
