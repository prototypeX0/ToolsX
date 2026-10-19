save and extract sa Drive C:
run Admin ung powershell, then proceed sa Folder nr Sysmon
irun sa powershell
.\Sysmon64.exe -accepteula -i .\sysmon-config.xml




Invoke-WebRequest -Uri https://packages.wazuh.com/4.x/windows/wazuh-agent-4.14.9-1.msi -OutFile $env:tmp\wazuh-agent; msiexec.exe /i $env:tmp\wazuh-agent /q WAZUH_MANAGER='10.5.0.10' WAZUH_AGENT_NAME='VISCOM-WS1' 


run powershell
sa victim WS at Fileserver
Enable-PSRemoting -Force




<localfile>
  <location>Microsoft-Windows-Sysmon/Operational</location>
  <log_format>eventchannel</log_format>
</localfile>
