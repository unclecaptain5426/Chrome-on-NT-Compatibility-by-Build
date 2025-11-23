Chrome 5.0.375.127 Stable - last unofficial version for Windows 2000 Beta 3 Build 1964 - Windows Whistler Beta 1 Build 2296

Chrome 33.0.1707.0 Dev / 32.0.1700.107 Stable - last unofficial version for Windows 2000 SP4 without Extended Kernel by using:
 
 advapixp.dll. kernelxp.dll, and userxp.dll by blackwingcat 
 
 wtsapi32.dll, winsta.dll, ws2_32.dll, imm32.dll, and iphlpapi.dll from Windows 2000 Extended Kernel. 

And Chrome 33.0.1707.0 Dev / 32.0.1700.107 Stable - also the last unofficial version for Windows Whistler Late Beta 1 Build 2410 - Windows Whistler Pre-RC 1 Build 2475 by using:
 
 kernelxp.dll by blackwingcat (with API swaps to the wrapper)
 
 wtsapi32.dll, winsta.dll, imm32.dll, icmp.dll (from 2000 SP4), and iphlpapi.dll from Windows 2000 Extended Kernel.

Since chrome_elf.dll was added on Chrome 33.0.1712.2 Dev, Chrome 33.0.1750.xxx-49.0.2623.xxx is unofficially possible with using bwc's wrappers, but it freezes within seconds.

Chrome 49.0.2623.112 (and 34.0.1847.137 is the last for no SSE2, ofc) - is the last unofficial version to work on Windows XP build 2481 with kernelxp.dll by roytam1 (but Windows XP build 2517 (5.1.2517.main.010713-1717) is recommended unofficially especially to replace system core files with the one from XP SP1 in system32 to improve stability) - Windows Longhorn build 40xx or Vista build 5xxx.

Chrome 50 on Windows XP/2003 without One-Core API is not impossible but it can be unstable.

Chrome 51.0.26?? Dev / Chrome 50.0.2664.102 - is the last unofficial version to fully run on Windows Vista without Extended Kernel and Windows 2000 with Extended Kernel.

Frequently Asked Questions

1) Why Chrome 12.0.730+ Dev hardcoded GetNativeSystemInfo?

Because Chrome 12.0.729 Dev / Chrome 11.0.696.77 Stable is the last to use a fallback function like GetStdHandle or something for GetNativeSystemInfo (especially on Windows XP Pre-RC 1 build 2475 and below). Because starting Chrome 12.0.730+ Dev, if GetNativeSystemInfo is replaced with something else, it will trigger an exception CPU divide-by-zero (0xc0000094).

2) Why Chrome 23-32 require any additional DLLs for Windows 2000 without Extended Kernel / and Chrome 23-49 requires any additional files for Windows XP RTM? ===

Because starting at Chrome 23.0.1255.0 Dev, without any minor modifications like these files for Windows XP RTM/2000 SP4 without KernelEx, Chrome starts to lose functionally for the address bar due to imm32.dll and msftedit.dll changes, and by Chrome 24, Chrome will not start on Windows XP RTM/2000 SP4 without KernelEx without minor modifications.

2.1) For Chrome 24-28...You must have the imm32.dll and msftedit.dll from Windows 2000 Extended Kernel, or the address bar will not work (for Windows 2000)

2.2) For Chrome versions 29-32... You must have the imm32.dll from Windows 2000 Extended Kernel, or Chrome will not launch.
   
3) Why chrome_elf.dll does not like Windows XP RTM/2000 SP4?

Because starting at Chrome 33.0.1712.2 Dev, Chrome starts to lose functionally for Windows 2000 SP4 without Extended Kernel, due to chrome_elf.dll being introduced, while it is  still unofficially possible to get it to work on Windows 2000 SP4 without Extended Kernel, but even with normal use after the timeout (up to 60 seconds), it will freeze. So, because later versions (like Chrome 33.0.1712.2 Dev - Chrome 49.0.2623.112) require at least Microsoft Windows XP build 2481 (but Microsoft Windows XP build 2517 & Microsoft Windows .NET Server build 3531 or later is recommended especially to get it fully working is by swapping the ntdll.dll with the one from Microsoft Windows XP SP1, and with just using kernelxp.dll wrappers unofficially + additional XP SP3 DLLs (such as iphlpapi.dll, icmp.dll, imm32.dll (if on 2481-2509 & 3505, then its from Windows 2000 Extended Kernel))).

3.1) 

4) Why chrome requires winhttp.dll?
Note: winhttp.dll must be inserted to system32 or the chrome folder for Windows versions before Windows 2000 SP3 and Windows XP SP1 in order for Chrome to work.
winhttp.dll must be from at least Windows Server 2003 RTM/Windows XP SP2/Windows 2000 SP4 UR1.

Bugs

Google Chrome 6 - 32 is not known to work on Windows 2000 Beta 3 Build 1964 - Windows Whistler Beta 1 Build 2296, due to enforced ADVAPI32/NTDLL functions after 5.0.375.127.

Google Chrome 33 - 49 is not known to work very well on Windows Whistler Beta 1 Build 2410 - Windows Whistler Pre-RC 1 Build 2475 when using kernelxp.dll wrappers by BWC (because it starts but freezes within seconds), but when using roytam1's kernelxp.dll wrappers and attempted to replace GetNativeSystemInfo with something else on kernelxp.dll, it triggers an c0000094 exception. On the other hand, when using Chrome 33 - 49 on Windows Whistler RC 1 Build 2481 - Windows Whistler RC 1 Build 2509, downloading executable files leads to Chrome crashing (because the NTDLL.DLL from XP SP1 does not work on Windows XP builds prior to RC 2 build 2517).

Screenshots

Notes
*Make sure you have 7-Zip & CFF Explorer installed.
*If you are on a non-XP SP2 system... make sure you use --no-sandbox command line.
