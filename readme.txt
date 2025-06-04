Chrome 0.2.149.30 Beta (Windows 2000 build 1964+) Chrome 0.2.152+ does not work on Windows 2000 build 1964 through Windows Whistler build 2296 for unknown reasons, so Chrome 0.2.152+ requires Windows Whistler Pre-Beta 2 Build 2410
Chrome 11 Dev?/Chrome 10 Stable (Windows Whistler build 2410/2416+) Chrome 11 can run on these builds, although it is extremely buggy. Chrome 12-1? can run, but does not work on Windows Whistler build 2410 through Windows XP build 2475
Chrome 20.0.1132.57 (Windows XP build 2481+) Chrome 21.0.1145+ does not work on Windows XP build 2481 through Windows XP SP2 build 2600.1213 due to the EncodePointer/DecodePointer & EncodeSystemPointer/DecodeSystemPointer being added to KERNEL32.DLL that will require upgrading to Windows XP SP2 Beta Build 2600.2055

Chrome 0.2.149.30 Beta (Windows Whistler build 2250 through Windows Whistler build 2296) & Chrome 5.0.312 Dev (Windows Whistler build 2410) are these specialized versions due to application binding errors on Whistler builds 2250-2410

For tools Includes 7-Zip, PEtools (changing kernel functions), Resource Hacker (removing manifests), and Guide on how to get these versions to work

You must use --no-sandbox to get Chrome to work.
For Chrome 20 on XP build 2481, --no-sandbox is NOT required.

I managed getting Chrome 10 to work by changing the kernel functions WTSSetQueryToken to WTSFreeMemory on WTSAPI.DLL in chrome.exe and chrome.dll on Whistler 2475.