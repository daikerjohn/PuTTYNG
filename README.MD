# PuTTYNG

This is a modieifed version of [PuTTY](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html) from [Simon Tatham](https://www.chiark.greenend.org.uk/~sgtatham/) to be used with [mRemoteNG](https://mremoteng.org/).

| Branch | Build |
|:-----------------: |:-------------------:|
| `Main` | [![Build status](https://ci.appveyor.com/api/projects/status/lbux84r7mt5fh4ar/branch/master?svg=true)](https://ci.appveyor.com/project/mremoteng/puttyng/branch/main) |
| `Develop` | [![Build status](https://ci.appveyor.com/api/projects/status/lbux84r7mt5fh4ar/branch/master?svg=true)](https://ci.appveyor.com/project/mremoteng/puttyng/branch/develop) |

**The following files within the project were modified:**
- BE_ALL_S.C
- CMDLINE.C
- PUTTY.H
- WINDOWS/PUTTY.RC
- WINDOWS/VERSION.RC2 
- WINDOWS/WINDOW.C

**The following file within the project was added:**
- WINDOWS/MAKEFILE.NG
- MAKEFILE = MAKEFILE.NG (merge changes from Makefile.vc)
- rename putty.exe to puttyng.exe
- change the "all" target to only build puttyng.exe

**To update PuTTYNG from the original repository:**
- git remote add putty https://git.tartarus.org/simon/putty.git
- git fetch --tags
- git remote update putty
- git checkout master
- git merge tags/0.76
- git push master

After that create a new tag from within GitHub to trigger the AppVeyor release build.
