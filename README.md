# Scriptware Windows 10 installation

## Remove all default Windows apps

Start PowerShell as administrator and run the following command:

```
Get-AppxPackage | where-object {$_.name –notlike "*store*"} | Remove-AppxPackage
```

## Remove Network icon from File Explorer

1 Open Registry Editor.
1 Go to the following Registry key:

```
HKEY_CLASSES_ROOT\CLSID\{F02C1A0D-BE21-4350-88B0-7367FC96EF3C}\ShellFolder
```

l Set the value data of the DWORD value Attributes to b0940064.

l If you are running a 64-bit operating system, repeat the steps above for the following Registry key:

```
HKEY_CLASSES_ROOT\Wow6432Node\CLSID\{F02C1A0D-BE21-4350-88B0-7367FC96EF3C}}\ShellFolder
```

l  Restart Windows Explorer