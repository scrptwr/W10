# Scriptware Windows 10 installation

## Remove all default Windows app

Start PowerShell as administrator and run the following command:

```
Get-AppxPackage | where-object {$_.name –notlike "*store*"} | Remove-AppxPackage
```