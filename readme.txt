Chrome 6.0.408 Dev / 5.0.375.127 Stable - last unofficial version for Windows 2000 RC2 Builds - ????
Chrome 30.0.1599.101 - last unofficial version for vanilla Windows 2000 with imm32.dll from Windows 2000 Extended Kernel.
Chrome 31-32 is startable on Windows 2000 unofficially, but it does not load pages properly, and --no-sandbox used triggers an 0x80000003 breakpoint.
Chrome 32.0.1700.107 - last unofficial version for Windows Whistler Late Beta 1 Build 2419 through Windows .NET Server build 3590 with imm32.dll from Windows 2000 Extended Kernel.
Chrome 33-49 is startable on Windows Whistler build 2419 through Windows .NET Server Build 3590 unofficially, but it either triggers a crash or hang after seconds.
Chrome 49.0.2623.112 (and 34.0.1847.137 is the last for no SSE2, ofc) - is the last unofficial version to work on Windows XP SP1 Beta Build 2600.1050 and Windows .NET Server Build 3604.
Chrome 50 is startable on Windows XP with kernelxp.dll wrappers unofficially, but the webpage does not function correctly (as tested on XP SP1).

Make sure you have 7-Zip, CFF Explorer, and winhttp.dll installed.
Make sure you use --no-sandbox and --ignore-certificate-errors to get it to fully work.