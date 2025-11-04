Chrome 6.0.408 Dev / 5.0.375.127 Stable - last unofficial version for Windows 2000 Beta 3 Build 1964 - Windows Whistler Beta 1 Build 2296
Chrome 33.0.1707.0 Dev / 32.0.1700.107 Stable - last unofficial version for Windows 2000 SP4 without Extended Kernel with just wtsapi32.dll, winsta.dll, ws2_32.dll, imm32.dll, and iphlpapi.dll from Windows 2000 Extended Kernel. And its also the last unofficial version for Windows Whistler Late Beta 1 Build 2410 - Windows Whistler Pre-RC 1 Build 2475 with just wtsapi32.dll, winsta.dll, imm32.dll, and iphlpapi.dll from Windows 2000 Extended Kernel.
Since chrome_elf.dll was added on Chrome 33.0.1712.2 Dev, Chrome 33.0.1750.xxx-49.0.2623.xxx is unofficially possible with using bwc's wrappers, but it freezes within seconds.
Chrome 49.0.2623.112 (and 34.0.1847.137 is the last for no SSE2, ofc) - is the last unofficial version to work on Windows XP build 2481 (but Windows XP build 2517 (5.1.2517.main.010713-1717)/Windows .NET Server Build 3531 (5.1.3531.0.main.010730-1811) - Windows .NET Server Beta 3 Build 3590 (5.1.3590.main.011110-1652)) is recommended unofficially especially to replace ntdll.dll with the one from XP SP1 in system32) - Windows Longhorn build 40xx or Vista build 5xxx.
Chrome 50 is startable on Windows XP with kernelxp.dll wrappers unofficially, but with frequent crashes.
Chrome 51.0.26?? Dev / Chrome 50.0.2664.102 - is the last unofficial version to fully run on Windows Vista without Extended Kernel and Windows 2000 with Extended Kernel.
Make sure you have 7-Zip, CFF Explorer, and winhttp.dll (especially on prior to 2000 SP3/XP SP1) installed.
Make sure you use --no-sandbox and --ignore-certificate-errors to get it to fully work.

== FAQ ==

=== Why Chrome 23-32 require any additional DLLs for Windows 2000 without Extended Kernel / and Chrome 23-49 requires any additional files for Windows XP RTM? ===
Because starting at Chrome 23.0.1255.0 Dev, without any minor modifications like these files for Windows XP RTM/2000 SP4 without KernelEx, Chrome starts to lose functionally for the address bar due to imm32.dll and msftedit.dll changes, and by Chrome 24, Chrome will not start on Windows XP RTM/2000 SP4 without KernelEx without minor modifications.

1) You must have the imm32.dll and msftedit.dll from Windows 2000 Extended Kernel, or the address bar will not work (for Windows 2000)
1.1) You must have ntdll.dll replaced with the one from XP SP1 in system32 (only for Windows XP RC 2 Build 2517 (5.1.2517.main.010713-1717) - Windows .NET Server Beta 3 Build 3590 (5.1.3590.main.011110-1652)), and msftedit.dll from XP SP3, imm32.dll from XP SP3 (and from Windows 2000 Extended Kernel if using Windows XP RC 1 Build 2481 (5.1.2481.main.010523-1905) - Windows XP RC 1 Build 2509 (5.1.2509.main.010702-1146) & Windows Whistler Server Build 3505 (5.1.3505.idx02.010710-1030)), iphlpapi.dll, and icmp.dll from Windows XP SP3 on placed on Chrome-bin, or it will not work (for Windows XP RTM)

2) For Chrome versions 29-32, you must have the imm32.dll from Windows 2000 Extended Kernel, or Chrome will not launch.
2.1) You must have ntdll.dll replaced with the one from XP SP1 in system32 (only for Windows XP RC 2 Build 2517 (5.1.2517.main.010713-1717) - Windows .NET Server Beta 3 Build 3590 (5.1.3590.main.011110-1652)), and imm32.dll from XP SP3 (and from Windows 2000 Extended Kernel if using Windows XP RC 1 Build 2481 (5.1.2481.main.010523-1905) - Windows XP RC 1 Build 2509 (5.1.2509.main.010702-1146)), iphlpapi.dll, and icmp.dll from Windows XP SP3 on placed on Chrome-bin, or it will not work (for Windows XP RTM)

3) For Chrome versions 33-49, it is recommended that you replace the ntdll.dll with the one from XP SP1.
3.1) You must have ntdll.dll replaced with the one from XP SP1 in system32, imm32.dll, iphlpapi.dll, and icmp.dll from Windows XP SP3 on placed on Chrome-bin, or it will not work (for Windows XP RTM)

== Why chrome_elf.dll does not like Windows XP RTM/2000 SP4? ==

Because starting at Chrome 33.0.1712.2 Dev, Chrome starts to lose functionally for Windows 2000 SP4 without Extended Kernel, due to chrome_elf.dll being introduced, while it is  still unofficially possible to get it to work on Windows 2000 SP4 without Extended Kernel, but even with normal use after the timeout (up to 60 seconds), it will freeze. So, because later versions (like Chrome 33.0.1712.2 Dev - Chrome 49.0.2623.112) require at least Microsoft Windows XP build 2481 (with just using kernelxp.dll wrappers unofficially + additional XP SP3 DLLs or newer.

== Why chrome requires winhttp.dll? ==
Note: winhttp.dll must be inserted to system32 or the chrome folder for Windows versions before Windows 2000 SP3 and Windows XP SP1 in order for Chrome to work.
winhttp.dll must be from at least Windows XP SP2/Windows 2000 SP4 UR1.

== Bugs ==

*Google Chrome 6 - 32 is not known to work on Windows 2000 Beta 3 Build 1964 - Windows Whistler Beta 1 Build 2296, due to enforced ADVAPI32 functions after 5.0.375.127.
*Google Chrome 33 - 49 is not known to work very well on Windows Whistler Beta 1 Build 2410 - Windows Whistler Pre-RC 1 Build 2475 when using kernelxp.dll wrappers by BWC (because it starts but freezes within seconds), but when using roytam1's kernelxp.dll wrappers and attempted to replace GetNativeSystemInfo with something else on kernelxp.dll, it triggers an c0000094 exception. On the other hand, when using Chrome 33 - 49 on Windows Whistler RC 1 Build 2481 - Windows Whistler RC 1 Build 2509 + Windows Whistler Server Build 3505, downloading executable files leads to Chrome crashing.
