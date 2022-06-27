Disable Search highlights in the Windows Search bar

REG ADD "HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\Windows Search" /v "EnableDynamicContentInWSB" /t REG_DWORD /d "0" /f

Disable Edge Update

Get-ScheduledTask -TaskName MicrosoftEdgeUpdate* | Disable-ScheduledTask | Out-Null
Get-ScheduledTask -TaskName MicrosoftEdgeUpdate* | Unregister-ScheduledTask -Confirm:$False | Out-Null
