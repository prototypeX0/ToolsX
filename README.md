save and extract sa Drive C:
run Admin ung powershell, then proceed sa Folder nr Sysmon
irun sa powershell
.\Sysmon64.exe -accepteula -i .\sysmon-config.xml



palitan ang IP ng Wazuh server at ung WAZUH_AGENT_NAME 

Invoke-WebRequest -Uri https://packages.wazuh.com/4.x/windows/wazuh-agent-4.14.9-1.msi -OutFile $env:tmp\wazuh-agent; msiexec.exe /i $env:tmp\wazuh-agent /q WAZUH_MANAGER='10.5.0.10' WAZUH_AGENT_NAME='VISCOM-WS1' 



**sa Victim WS at Fileserver (para sa WinRM**)
run powershell
Enable-PSRemoting -Force




**ilagay sa Ossec conf (sa lahat WS1 and WS 2 at DC at File Server**
<localfile>
  <location>Microsoft-Windows-Sysmon/Operational</location>
  <log_format>eventchannel</log_format>
</localfile>
