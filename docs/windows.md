# Windows stuff goes here

## Secure boot certificate changes

secure boot certificate check powershell

To check if your Windows system has the updated **Windows UEFI CA 2023** Secure Boot certificates, open **PowerShell as Administrator** and run the following command:

```powershell
[System.Text.Encoding]::ASCII.GetString((Get-SecureBootUEFI db).bytes) -match 'Windows UEFI CA 2023'
```

If the output is **True**, the new certificate (valid until 2053) is installed. If the output is **False**, your system is likely still using the older 2011 certificate, which expires in **June 2026**.

### Verification Steps
*   **Active Database Check**: The command above checks the `db` (Signature Database), which contains the certificates currently used to boot the operating system.
*   **Default Database Check**: To verify if the certificate is embedded in the firmware itself (persistent across factory resets), run:
    ```powershell
    [System.Text.Encoding]::ASCII.GetString((Get-SecureBootUEFI dbdefault).bytes) -match 'Windows UEFI CA 2023'
    ```
*   **Additional Certificates**: For a complete verification, you can also check for the presence of other required 2023 certificates using these commands:
    ```powershell
    [System.Text.Encoding]::ASCII.GetString((Get-SecureBootUEFI kek).bytes) -match 'Microsoft Corporation KEK 2K CA 2023'
    [System.Text.Encoding]::ASCII.GetString((Get-SecureBootUEFI db).bytes) -match 'Microsoft UEFI CA 2023'
    [System.Text.Encoding]::ASCII.GetString((Get-SecureBootUEFI db).bytes) -match 'Microsoft Option Rom UEFI CA 2023'
    ```
    Each command returning **True** indicates that specific certificate is installed.

### Alternative Methods
*   **Windows Security App**: After the April 2026 Patch Tuesday updates, the **Windows Security** app includes a built-in verification status for Secure Boot certificates.
*   **Dell Systems**: Dell users can install the `UEFIv2` PowerShell module (`Install-Module -Name UEFIv2`) and use `Get-UEFISecureBootCerts db` to view certificate signatures.

## Repair Windows 11 update blocked previewing pdf

`Get-ChildItem -Path "$env:USERPROFILE\Downloads" -Filter *.pdf -Recurse | Unblock-File   `

## Disable Bitlocker

Launch an elevated command prompt and run the command:
`manage-bde -off C:`

## Windows recall 

Display status in elevated command prompt:

`DISM /Online /Get-FeatureInfo /FeatureName:Recall   `

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

