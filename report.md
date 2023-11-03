## What happened

The js engine steam used aka v8 has some rce vulnerabilities,and I show how the v8 rce bugs can be used to compromise the user's whole system,with a steam v8's 0day bug and an old windows kernel bug to escape the chrome sandbox.

The exploit chain is not that easy to understand if you are not a browser security researcher,if you are interested in the exploit details,you can DM me in twitter @5n1p3r0010.

## Steps to reproduce

#### environment:

steam: latest version,default config aka sandbox on

windows:  10 1903 without any patch,because I use an old windows kernel bug to escape sandbox,not windows kernel 0day,xd.

FYI my windows iso is cn_windows_10_consumer_editions_version_1903_x64_dvd_8f05241d.iso

#### How:

1.Open a local http server.

2.Use steam to browse the steam_fullchain_x64.html

You can see the steps in repro.mp4

## Impact

The js engine steam main process and some games like cs2\CS:GO DOTA2 used is vulnerable,and there are some in the wild exploit in history.The aforementioned games I also usually play,but I do not want to be pwned by others,xd.I just use the steam v8 0day and windows kernel nday to show the impact of compromising whole system,the v8 rce bug can also be used to exploit the aforementioned games,whose js engine is not sandboxed which means the exploit is much more easy.

## How to fix

I think pin v8 to a version and fix the vulns of that version mannully is the right way,cause if we update chrome aka libcef version,the new chrome version will always be vulnerable,and developers will do much more work.

To fix the current steam's v8 vulns,I provide the v8list.txt which contaions v8 rce bugs,you need to see how the crbug.com/issue_id get patched and fix the bug mannully.

I'd like to offer help to fix the rce bugs if possible.



Best Regards