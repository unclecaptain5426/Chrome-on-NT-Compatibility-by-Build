Chrome 0.2.149.30 - for Windows 2000 Beta 3 Build 1964 & Windows XP Pre-Beta Build 2250 - Windows XP Beta 1 Build 2296
Chrome 0.2.152+ does not work on Windows 2000 Beta 3 Build 1964 - Windows Whistler Beta 1 Build 2296, even though it is startable, but it crashes on launch. So Chrome 0.2.152+ only works since Windows Whistler Pre-Beta 2 Build 2410
Chrome 12.0.729 Dev / 11.0.696.77 - for Windows XP Pre-Beta 2 Build 2410 & Windows XP Pre-Beta 2 Build 2416, but requires swapping the dnsapi.dll file with the one from 2474 or 2475.
Chrome 12.0.730 Dev+ with modifications is startable on Windows XP Pre-Beta 2 Build 2410/2416 - Windows XP Pre-RC 1 Build 2475, but it does not load webpages (and even enabling --no-sandbox will result in 0xc0000094 division by zero error and webpages will crash with "Aw Snap!" instead), and Task Manager will just instantly Crash Chrome. So Chrome 12.0.730+ only works since Windows XP Pre-RC 1 Build 2481
Chrome 20.0.1132.57 - for Windows XP Pre-RC 1 Build 2481
Chrome 21.0.1145+ does not work for Windows XP Pre-RC 1 Build 2481 - Windows XP SP2 Build 2600.1213 (due to the enhancements of EncodePointer/DecodePointer and EncodeSystemPointer/DecodeSystemPointer kernel functions in KERNEL32.DLL, which they are introduced in Windows XP SP2 Beta Build 2600.2055).

Chrome 0.2.149.30 Beta (Windows Whistler build 2250 through Windows Whistler build 2296) & Chrome 12.0.729 Dev (Windows Whistler build 2410) are these specialized versions due to application binding errors on Whistler builds 2250-2410

For tools Includes 7-Zip, PEtools (changing kernel functions), Resource Hacker (removing manifests), and Guide on how to get these versions to work

You must use --no-sandbox to get Chrome to work.
For XP build 2474 or 2475, --no-sandbox is NOT required.

I managed getting Chrome 10 to work by changing the kernel functions WTSSetQueryToken to WTSFreeMemory on WTSAPI.DLL in chrome.exe and chrome.dll on Whistler 2475.
