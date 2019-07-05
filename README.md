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

## Course Intro

I had the privilege of learning powershell from one of Jeffrey Snover's events. I feel like this is going to come in very handy here. If you're reading this before you start the course - go do a bit of powershell. In a month of lunches maybe, or the old Microsoft Virtual Academy videos if they're still around.

29.9 days to go :)

## Objective 1

Through the first 3 videos (including the introduction), documenting as I go, has taken about 2.5 hours all told (including family time, which takes up most of it yes?).

I do a lot of administration using the built in tools from day to day, so I am finding that I am documenting the set of tools I don't understand, and simply noting the relevant section of my own regular tooling. I'm refactoring the notes as I go to try and put them into a semblance of order for what I think will be coming - certainly into the sort of sanity that I would use if I was building a module, or executing a full domain penetration test (which, I suppose I am). Because I have access to the student labs AND my own production environments, I am able to double check commands and see how they look "in the real world" which is quite effective because I know the site.

Will actually execute the Objective 1 before proceeding to the next videos, after I commit this log update.

29.85 days to go :)
