# Pentester Academy - Attacking and Defending Active Directory

No Spoilers

## Setting up

I've deployed a Windows 10 1809 VM, turned on the firewall and disabled all incoming traffic, and then installed chocolatey and a few supporting tools:

```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
refreshenv
choco install -y openvpn git vim
```
Once the email shows up I have access to the client information necessary, the downloads, and the labs! I've added the appropriate configs to a brand new, private, clean git repository, and cloned the repository to my VM.

### VPN

When using "Import file" from the OpenVPN client, it won't place the two other files in the config, open "%UserName%\OpenVPN\config\STUDENTFOLDER" and place the .p12 and .key files in there as well to permit the connection.

### VM

RDP to the VM was excellent. Unzipped the files in the mentioned folder so that they're ready, and started grabbing the videos to watch.

30 days to go :)
