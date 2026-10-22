<div align="center">
<h1>Ubuntu Server Installation</h1>
</div>

<h2> Overview </h2>
<p>Ubuntu Server installation and configuration of Ubuntu Server for SOC Analyst Home Lab. Ubuntu is used as a Linux-based server environment for hosting security monitoring tools, collecting logs, and generate alert from practicing SIEM administration and troubleshooting.</p>

<h2>Lab Objectives</h2>
<p>
  <ul>
    <li>- Install and configure Ubuntu Server.</li>
    <li>- Configure network connectivity and verify the server IP address -> like (ip a) or (ip addr) or (ifconfig)</li>
    <li>- Install and manage required Linux packages -> like (sudo apt-get update && sudo apt-get upgrade -y)</li>
    <li>- Configure SSH for remote administration via actual window os.</li>
    <li>- Prepare the server for SIEM deployment and security monitoring.</li>
    <li>- Practice Linux system administration and troubleshooting.</li>
  </ul>
</p>

<h2>System Configuration</h2>

| Component        |    Configuration                  |
| Operating System | Ubuntu Server                     |
| Deployment       | Virtual Machine                   |
| Hypervisor       | Oracle VirtualBox                 |
| Network          | NAT / Host-Only                   |
| IP Address       | `10.0.x.x`                        |
| Administration   | Linux Terminal / SSH              |
| Intended Role    | SIEM Server / Security Monitoring |
| SIEM Platform    | Splunk or Wazuh                   |

<h2>Setup installation</h2>
<p>Step 1: Install Ubuntu Server</p>
<ul>
  <li>- Download the Ubuntu Server ISO from the official website.</li>
  <li>- Create a virtual machine in VirtualBox.</li>
  <li>- Allocate suitable RAM, CPU cores, and virtual disk space.</li>
  <li>- Attach the ISO and complete the Ubuntu installation.</li>
  <li>- Create a user account with password and configure the initial system settings.</li>
</ul>
<p>Step 2: Update the System</p>
<ul>
  <pre>sudo apt-get update -y</pre>
  <pre>sudo apt-get upgrade -y</pre>
</ul>
<p>Step 3: Verify Network Configuration</p>
<pre>
  <li>ip addr</li>
  <li>ip route</li>
  <li>hostname -I</li>
  & 
  <p>ping -c 4 8.8.8.8 <- for network connectivity </p> 
</pre>


<ul>
  <li>
    <p>Step 4: Install and Configure SSH</p>
    <p>Install the OpenSSH server for remote administration.</p>
    <pre><code>sudo apt install openssh-server -y
sudo systemctl enable --now ssh
sudo systemctl status ssh</code></pre>
    <p>Check the SSH service and listening port:</p>
    <pre><code>sudo ss -tlnp | grep ':22'</code></pre>
  </li>


  <li>
    <p>Step 5: Prepare for SIEM Deployment</p>
    <p>Before installing Splunk or Wazuh:</p>
    <ul>
      <li>Verify sufficient free disk space.</li>
      <li>Confirm network connectivity between the server and monitored endpoints.</li>
      <li>Configure the required network mode and firewall rules.</li>
      <li>Document server IP addresses and listening ports.</li>
      <li>Verify service status and review logs during troubleshooting.</li>
    </ul>
  </li>
</ul>


