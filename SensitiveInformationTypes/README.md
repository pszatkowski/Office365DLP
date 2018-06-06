# Sensitive Information Types
## Installation

1. [Connect to the Office 365 Security & Compliance Center using remote Powershell](http://go.microsoft.com/fwlink/?LinkID=799771&clcid=0x409)
2. In the Security & Compliance Center PowerShell, type 
```powershell
New-DlpSensitiveInformationTypeRulePackage -FileData (Get-Content -Path "C:\PathToRulePack\MyNewRulePack.xml" -Encoding Byte)
```
3. To confirm, type Y and then press ENTER.
4. Verify that your new sensitive information type was uploaded by typing
```powershell
Get-DlpSensitiveInformationType
```
to see a list of all sensitive types. You can quickly separate custom sensitive information types from those which come built in by looking at the Publisher column. You can filter the list to a specific sensitive information type by running 
```powershell
Get-DlpSensitiveInformationType -Identity “name of sensitive information type”.
```