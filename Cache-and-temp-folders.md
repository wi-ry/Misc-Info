# Cache and Temp Folders
List of folders that contain temporary files which you most likely don't need/want backed up.

## Browser caches

### Internet Explorer
 - Example path: `AppData\Local\Microsoft\Windows\Temporary Internet Files\Content.IE5`
 - Example PowerShell for finding: `Get-ChildItem -Recurse -Directory | Where { $_.FullName -match "Temporary Internet Files" -AND $_.FullName -match "Content.IE5" }`
 - Example PowerShell for removal: `Get-ChildItem -Recurse -Directory | Where { $_.FullName -match "Temporary Internet Files" -AND $_.FullName -match "Content.IE5" } | Remove-Item -Force`


## Cloud Storage Temp Folders

### OneDrive
 - Example path: `C:\OneDriveTemp`
 - Example find PowerShell: `Get-ChildItem -Recurse -Directory -Force | Where { $_.FullName -match "OneDriveTemp" }` (`-Force` is required for hidden files/folders)
