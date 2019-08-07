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

## Objectives 2 through 4

These are nicely put together. I have to say, because my first language isn't English, I sometimes struggle to follow what the instructor is saying. Because this is not a full scale penetration test, it is sometimes difficult to know what to log and what to ignore. A good example of this is the last part of the 4th objective, where I spent a few minutes trying to enumerate the final part before realising that "No" is an acceptable answer.

There's some really good stuff in this that is going to be put together into a proper script. Full enumeration should happen almost instantaneously, even if we ignore tools like bloodhound.

28.9 days to go. Only 3.5 videos in so far, but 4/23 objectives have been completed and I've already learned stuff.

Powerview is going to be spending a LOT of time in my day to day security management arsenal, from sysops to pentesting. I'm kicking myself for never discovering this tool before.

## Objectives 5 through 7

Now we're getting somewhere. The parts on bloodhound make me see how easy it can be, and we're now getting into the parts where some real thinking is required. Either I'm not hearing it properly in the video, or it wasn't pointed out for simple things like RealTimeProtection. Still some work to do with messing with ConstrainedLanguage which I've never encountered before (mostly I use JEA for that sort of thing), so this will be fun.

It is worth remembering that these are learning objectives and not necessarily exam points. This is particularly reminding me of my SGDE exam, wherein there are two parts that I thought should be related but couldn't see how (because... they weren't, they just happened to exist in the same space).

## Objectives 8 through 11

Now that we've gotten through a lot of the "basics", the domain persistence parts are fun and somewhat easy to go through. I'm making a cheatsheet as I go so that I can easily refer back to specific commands as necessary, and all I'm doing is flowing through. It's really good fun to execute some of these attacks in the lab environment just knowing that it doesn't matter if you break something or not. The only problem I'm really hitting is the implication that I can execute code via WMI, none of which seems to actually work when I try it. That said, all the file listing and silver ticketing works, so it's probably just that I'm not trying the right thing yet. My goal at the moment is to bolt through the course, then go back and re-do the parts I didn't know before hand - WMI is apparently one of those :)

## Objectives 12 through 16

We've got domain admin, now what can we do with it. Or, we've got domain user, what can we do with that. All very fun :)

## Objectives 17 through 18

Delegation. More delegation. Good to work through, but not something I've ever actually encountered in the wild to my knowledge (as a sysadmin). Still, good to know and it helped me find two anomalies in my own corporate environment.

## Objectives 19 through 22

This! This is what I signed up for. Attacking across trusts both internal and external. Elevating privileges with nothing more than a domain administrator account. These are really quick objectives, really easy to learn now that we've mostly gotten through the course but they are SO DAMNED EFFECTIVE.

And doing that for Objective 22. I've never even seen that (although I did admin that sort of machine for a few years) BUT it worked, and first time.

## Objective 23

I will be holding off on this objective until the end, because of what it takes to execute the attack.

## Defense

What can I say about defense? I made 398 lines of notes from the videos. The deception sections were good reading as well.

My only problem with defense is that it perhaps wasn't as complete as I would like. THAT SAID, there's a blurry line between group policy settings to manage hardening of PAW's, and what you can do to prevent/detect golden tickets, so it's probably good :)

## QUICK REVIEW

Good. Effective. Jumps around a little bit (AMSI bypass, for example, is used a lot but not explained until much later). Overall a really good introduction and I want to say intermediate look into Active Directory.

Following the old 80/20 rule, you could follow this course and implement 20% of the defensive recommendations and dramatically improve your network security. Based on my notes, implementing nearly 60% of the recommendations could be done with NO DETECTABLE CHANGES BY THE END USERS. There's really no excuse.

14 days to go. Time to build significant amounts of automation and prepare for the 24 hour exam.

## Objective 23

This was pretty easy actually once it came to it. Two points to note because I feel like they were glossed over (or I didn't note them down properly). Once shifting up to the forest root, if the domain is reset you may lose access to the system and need a reversion. Don't be afraid to send the email though, they're really responsive :)

Second point is to be sure that you have lsadump'd the forest root admin password. You'll need that to PTH before executing this attack.

## EXAM PREP

Less than 5 hours to go until my exam. Final review of techniques I'm not fully comfortable with, and a final review of the lab manuals to be sure I haven't missed anything.

I have, so far, written nearly 30 pages of notes (LaTeX is a beautiful thing) in preparation for the final report. I have two main cheatsheet documents (one for execution, one for enumeration). The goal of the exam means that I can, to a limited degree, ignore some of the later persistence techniques, but I've got notes on them... just in case :) I have prepared automation for the enumeration phase to be sure that I cover most or all of the points, and I've got a copy of bloodhound ready to go.

Now, for the coffee...
