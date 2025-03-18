# BloodHuntr
Veins and Blood *hunting* knife for Active Directory Execution process.

## Projects of

- BlockingDLL: This toolset is for testing blocking DLL process. See [README.md](./BlockingDLL/README.md).
- CloneProcess ./CloneProcess :nThis directory is for process forking and reflection. See [README.md](./CloneProcess/README.md).
- CommandLineSpoofing ./CommandLineSpoofing : This PoC performs Command Line Spoofing. This technique may not work for Windows 11.
- DarkLoadLibrary ./DarkLoadLibrary : PoCs in this directory are for testing Dark Load Library. See [README.md](./DarkLoadLibrary/README.md)
- GhostlyHollowing ./GhostlyHollowing : This PoC performs Ghostly Hollowing.
- Misc ./Misc : This directory is for helper tools to development PoCs in this repository.
- PhantomDllHollower ./PhantomDllHollower : This PoC performs Phantom DLL Hollowing. See [README.md](./PhantomDllHollower/README.md).
- PPIDSpoofing ./PPIDSpoofing : This PoC performs PPID Spoofing.
- ProcessDoppelgaenging ./ProcessDoppelgaenging : This PoC performs Process Doppelgänging. Due to kernel protection improvement for Microsoft Defender, this technique does not work for recent Windows OS (since about 2021, maybe). So if you want to test this technique in newer environment, must be stop `Microsoft` the `Windows Defender Antivirus Service`. See [the issue](#)
- ProcessGhosting ./ProcessGhosting : This PoC performs Process Ghosting. Due to kernel protection, this technique does not work for newer Windows from 22H2.
- [ProcessHerpaderping](./ProcessHerpaderping) : This PoC performs Process Herpaderping. Due to file lock issue, if you choose a fake image file smaller than you want to execute, file size shrinking will be failed and corrupt file signature for herpaderping process. To take full advantage of this technique, fake image file size should be larger than you want to execute. Due to kernel protection, this technique does not work for newer Windows from 22H2.
- [ProcessHollowing](./ProcessHollowing) : This PoC performs Process Hollowing. Unlike the original, the PE image is parsed into a new memory area instead of using `ZwUnmapViewOfSection` or `NtUnmapViewOfSection`.
- [ProcMemScan](./ProcMemScan) : This is a diagnostic tool to investigate remote process. See [README.md](./ProcMemScan/README.md).
- [ProtectedProcess](./ProtectedProcess) : This toolset is for testing Protected Process. See [README.md](./ProtectedProcess/README.md).
- [ReflectiveDLLInjection](./ReflectiveDLLInjection) : This toolset is for testing Reflective DLL Injection. See [README.md](./ReflectiveDLLInjection/README.md).
- [sRDI](./sRDI) : This directory is for tool to sRDI (Shellcode Reflective DLL Injection). See [README.md](./sRDI/README.md).
- [TransactedHollowing](./TransactedHollowing) : This PoC performs Transacted Hollowing.
- [WmiSpawn](./WmiSpawn) : This PoC tries to spawn process with WMI. The processes will be spawn as child processes of `WmiPrvSE.exe`. Supports local machine process execution and remote machine process execution. The usage can see [README.md](./WmiSpawn/README.md).

## Reference

*Blocking DLL*

- Preventing 3rd Party DLLs from [Injecting into your Malware](https://www.ired.team/offensive-security/defense-evasion/preventing-3rd-party-dlls-from-injecting-into-your-processes)
- Staying Under the Radar - Part 1 - PPID [Spoofing and Blocking DLLs](https://crypt0ace.github.io/posts/Staying-under-the-Radar/)
- PPID Spoofing & BlockDLLs with [NtCreateUserProcess](https://offensivedefence.co.uk/posts/ntcreateuserprocess/)

*Command Line Spoofing*

- Hide Artifacts: Process [Argument Spoofing](https://attack.mitre.org/techniques/T1564/010/)
- The return of the spoof part 2: [Command line spoofing](https://blog.nviso.eu/2020/02/04/the-return-of-the-spoof-part-2-command-line-spoofing/)
- *Process Ghosting*
- What you need to know about Process Ghosting, a [new executable image tampering attack](https://www.elastic.co/blog/process-ghosting-a-new-executable-image-tampering-attack)

*Process Herpaderping*

- Process Herpaderping
- Process Herpaderping (Mitre:T1055)


*Process Hollowing*
- Process Injection: [Process Hollowing](https://attack.mitre.org/techniques/T1055/012/)
- Process Hollowing and Portable [Executable Relocations](https://www.ired.team/offensive-security/code-injection-process-injection/process-hollowing-and-pe-image-relocations)


*Ghostly Hollowing and Transacted Hollowing*

- GitHub - hasherezade on [transacted_hollowing](https://github.com/hasherezade/transacted_hollowing)

*Protected Process*

- [Unknown Known DLLs](http://publications.alex-ionescu.com/Recon/Recon%202018%20-%20Unknown%20Known%20DLLs%20and%20other%20code%20integrity%20trust%20violations.pdf)
- [Unreal Mode : Breaking Protected Processes](https://www.nosuchcon.org/talks/2014/D3_05_Alex_ionescu_Breaking_protected_processes.pdf)
- The Evolution of Protected Processes [Part 1: Pass-the-Hash Mitigations in Windows 8.1](https://www.crowdstrike.com/blog/evolution-protected-processes-part-1-pass-hash-mitigations-windows-81/)

## Acknowledgments

Thanks for your research:

- Sulaiman Aziz [@byt3n33dl3](https://x.com/byt3n33dl3)
- Tal Liberman [@tal_liberman](https://x.com/tal_liberman)
- Eugene Kogan [@EuKogan](https://x.com/EuKogan)
- hasherezade [@hasherezade](https://x.com/hasherezade)
- Gabriel Landau [@GabrielLandau](https://x.com/GabrielLandau)
- Forrest Orr [@_forrestorr](https://x.com/_forrestorr)
- Stephen Fewer [@stephenfewer](https://x.com/stephenfewer)
- batsec [@\_batsec\_](https://x.com/_batsec_)
- Nick Landers [@monoxgas](https://x.com/monoxgas)