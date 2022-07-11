Power Management Hybernate off / High Performance
powercfg /hibernate off
powercfg /setactive 8c5e7fda-e8bf-4a96-9a85-a6e23a8c635c


Disable Search highlights in the Windows Search bar

REG ADD "HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\Windows Search" /v "EnableDynamicContentInWSB" /t REG_DWORD /d "0" /f

Disable Edge Update

Get-ScheduledTask -TaskName MicrosoftEdgeUpdate* | Disable-ScheduledTask | Out-Null
Get-ScheduledTask -TaskName MicrosoftEdgeUpdate* | Unregister-ScheduledTask -Confirm:$False | Out-Null
