# PowerShell Tutorial

## 🔹 Basic Syntax

```powershell
# Variables
$var = "value"

# Comments
# This is a comment

# Output
Write-Output "Hello"

# If-Else
if ($x -eq 5) {
    Write-Output "Yes"
} elseif ($x -gt 5) {
    Write-Output "Greater"
} else {
    Write-Output "No"
}

# Loops
foreach ($item in $list) { ... }
for ($i = 0; $i -lt 10; $i++) { ... }
while ($true) { ... }


| Operator    | Description                |
| ----------- | -------------------------- |
| `-eq`       | Equal                      |
| `-ne`       | Not equal                  |
| `-gt`       | Greater than               |
| `-lt`       | Less than                  |
| `-like`     | Wildcard match             |
| `-match`    | Regex match                |
| `-contains` | Contains item (for arrays) |

# Get files
Get-ChildItem -Path "C:\Folder"

# Read file
Get-Content "file.txt"

# Write to file
"Hello" | Out-File "file.txt"

# Copy / Move / Remove
Copy-Item "src.txt" "dest.txt"
Move-Item "a.txt" "b.txt"
Remove-Item "old.txt"

function Greet($name) {
    return "Hello, $name"
}

# Import module
Import-Module Az

# List commands
Get-Command

# Help
Get-Help Get-Process

try {
    # risky code
} catch {
    Write-Output "Error: $_"
} finally {
    # always runs
}

Get-Process | Where-Object { $_.CPU -gt 100 }
Get-Service | Select-Object Name, Status

