# Windows stuff goes here

## Repair Windows 11 update blocked previewing pdf

`Get-ChildItem -Path "$env:USERPROFILE\Downloads" -Filter *.pdf -Recurse | Unblock-File   `

## Disable Bitlocker

Launch an elevated command prompt and run the command:
`manage-bde -off C:`

## Lock screen images are cached here:

`%LocalAppData%\Packages\Microsoft.Windows.ContentDeliveryManager_cw5n1h2txyewy\LocalState\Assets`

## Windows terminal settings.json location
`$env:LocalAppData\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalState\settings.json`

### Changing CTRL-V and CTRL-C behavior on Windows terminal settings.json so vim keybindings still work for visual mode
  
    "actions": [
        {
            "command": "paste",
            "keys": "ctrl+shift+v"
        },
        {
            "command": {
                "action": "copy",
                "singleLine": false
            },
            "keys": "ctrl+shift+c"
        },

## Moving the Recovery Partition

https://thedxt.ca/2023/06/moving-windows-recovery-partition-correctly/

