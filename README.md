# PowerShell Tutorial

### Variables
```powershell
$var = "value"
```

### Comments
```powershell
# This is a comment
```

### Output
```powershell
Write-Output "Hello"
```

### If-Else
```powershell
if ($x -eq 5) {
    Write-Output "Yes"
} elseif ($x -gt 5) {
    Write-Output "Greater"
} else {
    Write-Output "No"
}
```

### Loops
```powershell
foreach ($item in $list) { ... }
for ($i = 0; $i -lt 10; $i++) { ... }
while ($true) { ... }
```

### Comparison
| Operator    | Description                |
| ----------- | -------------------------- |
| `-eq`       | Equal                      |
| `-ne`       | Not equal                  |
| `-gt`       | Greater than               |
| `-lt`       | Less than                  |
| `-like`     | Wildcard match             |
| `-match`    | Regex match                |
| `-contains` | Contains item (for arrays) |

### Get files
```powershell
Get-ChildItem -Path "C:\Folder"
```

### Read file
```powershell
Get-Content "file.txt"
```

### Write to file
```powershell
"Hello" | Out-File "file.txt"
```

### Copy / Move / Remove
```powershell
Copy-Item "src.txt" "dest.txt"
Move-Item "a.txt" "b.txt"
Remove-Item "old.txt"
```

### Methods
```powershell
function Greet($name) {
    return "Hello, $name"
}
```

### Import module
```powershell
Import-Module Az
```

### List commands
```powershell
Get-Command
```

### Help
```powershell
Get-Help Get-Process
```

### Try Catch
```powershell
try {
    # risky code
} catch {
    Write-Output "Error: $_"
} finally {
    # always runs
}
```
##Pipelines & Filtering
```powershell
Get-Process | Where-Object { $_.CPU -gt 100 }
Get-Service | Select-Object Name, Status
```

