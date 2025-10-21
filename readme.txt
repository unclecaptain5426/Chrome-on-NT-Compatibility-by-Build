Chrome 6.0.408 Dev / 5.0.375.127 Stable - last unofficial version for Windows 2000 Beta 3 Build 1964 - Windows Whistler Beta 1 Build 2296
Chrome 33.0.1707.0 Dev / 32.0.1700.107 Stable - last unofficial version for vanilla Windows 2000 and Windows Whistler Late Beta 1 Build 2410 through Windows .NET Server build 3590 with imm32.dll from Windows 2000 Extended Kernel.
For an example, Chrome 33.0.1707.0 is usable on Windows Whistler build 2410, but the bug found is that the "Google Chrome has encountered a problem and needs to close. We are sorry for the incovenience." error reporting window shows up as soon as it atarts. So, either keep the error reporting window, or crash Google Chrome.
Since chrome_elf.dll was added on Chrome 33.0.1712.2 Dev, Chrome 33.0.1750.xxx-49.0.2623.xxx is unofficially possible on vanilla Windows 2000 & Windows Whistler build 2419 through Windows .NET Server Build 3590 unofficially, but it either triggers a crash or hang after the timeout (up to 60 seconds).
Chrome 49.0.2623.112 (and 34.0.1847.137 is the last for no SSE2, ofc) - is the last unofficial version to work on Windows XP SP1 Beta Build 2600.1050 and Windows .NET Server Build 3604.
Chrome 50 is startable on Windows XP with kernelxp.dll wrappers unofficially, but with frequent crashes.
Chrome 51.0.26?? Dev / Chrome 50.0.2664.102 - is the last unofficial version to fully run on Windows Vista without Extended Kernel and Windows 2000 with Extended Kernel.
Make sure you have 7-Zip, CFF Explorer, and winhttp.dll (especially on prior to 2000 SP3/XP SP1) installed.
Make sure you use --no-sandbox and --ignore-certificate-errors to get it to fully work.

== FAQ ==

=== Why Chrome 23-32 require any additional DLLs for Windows 2000 without Extended Kernel / Windows XP RTM? ===
Because starting at Chrome 23.0.1255.0 Dev, without any minor modifications like these files for Windows XP RTM/2000 SP4 without KernelEx, Chrome starts to lose functionally for the address bar due to imm32.dll and msftedit.dll changes, and by Chrome 24, Chrome will not start on Windows XP RTM/2000 SP4 without KernelEx without minor modifications.
For Chrome versions 23-28, you must have the imm32.dll and msftedit.dll from Windows 2000 Extended Kernel, or the address bar will not work.
For Chrome versions 29-32, you must have the imm32.dll from Windows 2000 Extended Kernel, or Chrome will not launch.

== Why chrome_elf.dll does not like Windows XP RTM/2000 SP4? ==

Because starting at Chrome 33.0.1712.2 Dev, Chrome starts to lose functionally for Windows 2000 SP4 without Extended Kernel / Windows XP RTM without One-Core API (unofficially while using wrappers and additional DLLs to the app) due to chrome_elf.dll being introduced, while it is  still unofficially possible to get it to work on Windows 2000 SP4 without Extended Kernel / Windows XP RTM without One-Core API, but even with normal use after the timeout (up to 60 seconds), it will trigger a crash or hang. So, because later versions (like Chrome 33.0.1712.2 Dev - Chrome 49.0.2623.112) require at least Microsoft Windows XP SP1 (with just using kernelxp.dll wrappers unofficially) or newer.

== Why chrome requires winhttp.dll? ==
Note: winhttp.dll must be inserted to system32 or the chrome folder for Windows versions before Windows 2000 SP3 and Windows XP SP1 in order for Chrome to work.
winhttp.dll must be from at least Windows XP SP2/Windows 2000 SP4 UR1.
