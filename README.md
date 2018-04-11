# Scriptware Windows 10 installation

## Remove all default Windows app
```
Get-AppxPackage | where-object {$_.name –notlike "*store*"} | Remove-AppxPackage
```