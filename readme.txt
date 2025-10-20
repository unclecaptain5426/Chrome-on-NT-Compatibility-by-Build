Chrome 6.0.408 Dev / 5.0.375.127 Stable - last unofficial version for Windows 2000 Beta 3 Build 1964 - Windows Whistler Beta 1 Build 2296
Chrome 17.0.963.26 Dev / Chrome 16.0.912.41 Beta / Chrome 15? / 14.0.835.202 Stable - last unofficial version for Windows Whistler Beta 1 Build 2410 & 2416
Chrome 33.0.1707.0 Dev / 32.0.1700.107 Stable - last unofficial version for vanilla Windows 2000 and Windows Whistler Late Beta 1 Build 2419 through Windows .NET Server build 3590 with imm32.dll from Windows 2000 Extended Kernel.
Chrome 33.0.1750.xxx-49.0.2623.xxx is startable on vanilla Windows 2000 & Windows Whistler build 2419 through Windows .NET Server Build 3590 unofficially, but it either triggers a crash or hang after the timeout (up to 60 seconds).
Chrome 49.0.2623.112 (and 34.0.1847.137 is the last for no SSE2, ofc) - is the last unofficial version to work on Windows XP SP1 Beta Build 2600.1050 and Windows .NET Server Build 3604.
Chrome 50 is startable on Windows XP with kernelxp.dll wrappers unofficially, but with frequent crashes.
Chrome 51.0.26?? Dev / Chrome 50.0.2664.102 - is the last unofficial version to fully run on Windows Vista without Extended Kernel and Windows 2000 with Extended Kernel.
Make sure you have 7-Zip, CFF Explorer, and winhttp.dll (especially on prior to 2000 SP3/XP SP1) installed.
Make sure you use --no-sandbox and --ignore-certificate-errors to get it to fully work.

== Chrome 23-32 situtation for Windows 2000 without Extended Kernel / Windows XP RTM ==
For Chrome versions 23-28, you must have the imm32.dll and msftedit.dll from Windows 2000 Extended Kernel, or the address bar will not work.
For Chrome versions 29-32, you must have the imm32.dll from Windows 2000 Extended Kernel, or Chrome will not launch.


== Why chrome_elf.dll does not like Windows XP RTM/2000 SP4 ==

Because starting at Chrome 33.0.1712.2 Dev, Chrome starts to lose functionally for Windows 2000 SP4 without Extended Kernel / Windows XP RTM without One-Core API (unofficially while using wrappers and additional DLLs to the app) due to chrome_elf.dll being introduced, and so, because later versions (like Chrome 33.0.1712.2 Dev - Chrome 49.0.2623.112) require at least Microsoft Windows XP SP1 (with just using kernelxp.dll wrappers unofficially) or newer.

Note: winhttp.dll must be inserted to system32 or the chrome folder for Windows versions before Windows 2000 SP3 and Windows XP SP1 in order for Chrome to work.
winhttp.dll must be from at least Windows XP SP2/Windows 2000 SP4 UR1.
