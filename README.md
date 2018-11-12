##### Twitter: [@Hktalent3135773](https://twitter.com/Hktalent3135773)
[![Tweet](https://img.shields.io/twitter/url/http/Hktalent3135773.svg?style=social)](https://twitter.com/intent/tweet?original_referer=https%3A%2F%2Fdeveloper.twitter.com%2Fen%2Fdocs%2Ftwitter-for-websites%2Ftweet-button%2Foverview&ref_src=twsrc%5Etfw&text=Venom%20-%20Automated%20Pentest%20Recon%20Scanner%20%40Hktalent3135773&tw_p=tweetbutton&url=https%3A%2F%2Fgithub.com%2Fhktalent%2FVenom)
[![Follow on Twitter](https://img.shields.io/twitter/follow/Hktalent3135773.svg?style=social&label=Follow)](https://twitter.com/intent/follow?screen_name=Hktalent3135773)
[![Github Stars](https://img.shields.io/github/stars/hktalent/Venom.svg?style=social&label=Stars&color=orange)](https://github.com/hktalent/Venom/) 
[![GitHub Followers](https://img.shields.io/github/followers/hktalent.svg?style=social&label=Follow)](https://github.com/hktalent/Venom/)
![GitHub forks](https://img.shields.io/github/forks/hktalent/Venom.svg?style=social&label=Fork)

[![GitHub issues](https://img.shields.io/github/issues/hktalent/Venom.svg)](https://github.com/hktalent/Venom/issues) 
![GitHub watchers](https://img.shields.io/github/watchers/hktalent/Venom.svg?label=Watch)
![GitHub contributors](https://img.shields.io/github/contributors/hktalent/Venom.svg?colorB=red&colorA=orange)
![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/hktalent/Venom.svg?colorB=ff9988&colorA=006666)
![GitHub language count](https://img.shields.io/github/languages/count/hktalent/Venom.svg?colorB=995500&colorA=551166)
![GitHub search hit counter](https://img.shields.io/github/search/hktalent/Venom/goto.svg?colorB=0077ff&colorA=11aadd)
![GitHub top language](https://img.shields.io/github/languages/top/hktalent/Venom.svg?colorB=red&colorA=dd88ff)
![os](https://img.shields.io/badge/OS-Linux,%20Window,%20macOS-green.svg)
![nodejs](https://img.shields.io/badge/nodejs-blue.svg)
![python](https://img.shields.io/badge/python2-red.svg)
![license](https://img.shields.io/github/license/mashape/apistatus.svg)

```
         __    _ ______  ____   _  _____  ____    __
         \  \  //|   ___||    \ | |/     \|    \  /  |
          \  \// |   ___||     \| ||     ||     \/   |
           \__/  |______||__/\____|\_____/|__/\__/|__|1.0.12
    +-----------------+-----------+------------+------------------+
    |  OPTIONS BUILD  | TARGET OS |   FORMAT   |      OUTPUT      |
    +-----------------+-----------+------------+------------------+
    |  1 - shellcode     unix         C             C             |
    |  2 - shellcode     windows      C             DLL           |
    |  3 - shellcode     windows      DLL           DLL           |
    |  4 - shellcode     windows      C             PYTHON/EXE    |
    |  5 - shellcode     windows      C             EXE           |
    |  6   shellcode     windows      PSH-CMD       EXE           |
    |  7 - shellcode     windows      C             RUBY          |
    |  8 - shellcode     windows      MSIEXEC       MSI           |
    |  9 - shellcode     windows      POWERSHELL    BAT           |
    | 10 - shellcode     windows      HTA-PSH       HTA           |
    | 11 - shellcode     windows      PSH-CMD       PS1           |
    | 12 - shellcode     windows      PSH-CMD       BAT           |
    | 13 - shellcode     windows      VBS           VBS           |
    | 14 - shellcode     windows      PSH-CMD       VBS           |
    | 15 - shellcode     windows      PSH-CMD/C     PDF           |
    | 16 - shellcode     webserver    PHP           PHP/PHP       |
    | 17 - shellcode     multi OS     PYTHON        PYTHON        |
    | 18 - shellcode     multi OS     JAVA/PSH      JAR(RCE)      |
    | 19 - web_delivery  multi OS     PYTHON/PSH    PYTHON/BAT    |
    | 20 - shellcode     android      DALVIK        APK           |
    |                                                             |
    |  S - system built-in shells                                 |
    |  F - FAQ (frequent ask questions)                           |
    |  E - exit Shellcode Generator                               |
    +-------------------------------------------------------------+
                                                 SSA-RedTeam@2016_|

[☠ ] Shellcode Generator
[➽ ] Chose Your Venom:
```



# VENOM 1.0.12
```
metasploit Shellcode generator/compiler/listenner
Author: peterubuntu10@sourceforge.net  [ r00t-3xp10it ]
Suspicious-Shell-Activity (SSA) RedTeam develop @2016
HomePage: http://sourceforge.net/u/peterubuntu10/profile/
```

# [ DISCLAMER ]
```
The author does not hold any responsibility for the bad use
of this tool, remember that attacking targets without prior
consent is illegal and punished by law.
```

# [ DESCRIPTION ]
```
The script will use msfvenom (metasploit) to generate shellcode
in diferent formats ( c | python | ruby | dll | msi | hta-psh )
injects the shellcode generated into one template (example: python)
"the python funtion will execute the shellcode into ram" and uses
compilers like gcc (gnu cross compiler) or mingw32 or pyinstaller
to build the executable file, also starts a multi-handler to
recive the remote connection (shell or meterpreter session).

'venom generator' tool reproduces some of the technics used
by Veil-Evasion.py, unicorn.py, powersploit.py, etc, etc, etc..
But venom its not a fork of any of this tools because its writen
using Bash contrary to those tools that uses Python, also
remmenber that veil evasion does not build this formats:
[.msi .hta .vbs .ps1 .dll .php .jar .pdf] payload formats...

"P.S. some payloads are undetectable by AV soluctions... yes!!!"
One of the reasons for that its the use of a funtion to execute
the 2º stage of shell/meterpreter directly into targets ram
the other reazon its the use of external obfuscator/crypters.
```

# [ DEPENDENCIES ]
```
Zenity | Metasploit | GCC (compiler) | Pyinstaller (compiler)
mingw32 (compiler) | pyherion.py (crypter) | wine (emulator)
PEScrambler.exe (PE obfuscator) | apache2 (webserver)| winrar
vbs-obfuscator (crypter) | encrypt_PolarSSL (crypter) and
ettercap MitM+DNS_Spoof (venom domain name attack vector)

"venom.sh will download/install all dependencies as they are needed"
Adicionally as build shell/aux/setup.sh to help you install all venom
framework dependencies (metasploit as to be manually installed). 
```
