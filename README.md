# Big Sur Hackintosh on the ASUS STRIX Z490F via OpenCore 0.6.9 with GPU HW Acceleration
![HW info + HW Acceleration](static/working.jpg)
Here's the usual info screenshot plus Netflix working on Safari, a sign of successful GPU HW Acceleration. 

## Working
Everything, except the native macOS updater and some minor sleep bugs, detailed below.


## Not Working
### 1. macOS Software Update is currently buggy
OS updates appear to install, but don't seem to take any effect, aside from successfully updating the recovery partition. Likewise duplicate macOS boot options appear in the OpenCore selector menu post update. This issue seems to have occurred since Apple released macOS 11.2, as the native updater prior to 11.2 was working as intended. This is possibly due to errors in the CSR partition, but I've yet to fully verify this. SIP seems to be working and OK, but might also be the source of this bug.

Current solution is to either install OS updates natively and proceed with a clean install via the updated recovery (migrating all user data via time machine backup restore), or to simply use the internet recovery (untested) to wipe and reinstall the latest macOS (again migrating user data via time machine). Either way keep a bootable USB handy to proceed with the reinstall, as the EFI partition gets wiped when erasing and reformating the macOS boot drive.

### 2. Sleep bugs
This isn't actually so much an issue with going to sleep but rather staying asleep continuously. Occasionally the machine will at random wake itself from sleep, waking for approximatley 2-15 seconds, and then returning to sleep. This is most likely caused by a USB peripheral, the Intel NIC or perhaps powernap working as intended, but I've neglected to investigate this further due to this being a very minor annoyance rather than an actual issue. Likewise this same bug occurs when sleeping on windows, which leads me to believe its caused by the two formers rather than the latter.
