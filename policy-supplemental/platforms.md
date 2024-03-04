## Current primary platforms

| Target           | &nbsp; | O/S                 | &nbsp; | Architecture | &nbsp; | Toolchain                            |
|------------------|--------|---------------------|--------|--------------|--------|--------------------------------------|
| linux-x86\_64    |        | Ubuntu Server 22.04 |        | x86\_64      |        | gcc 11                               |
| linux-generic64  |        | Ubuntu Server 22.04 |        | x86\_64      |        | gcc 11                               |
| linux-x86        |        | Debian 11           |        | x86          |        | gcc 10                               |
| linux-generic32  |        | Debian 11           |        | x86          |        | gcc 10                               |
| linux-aarch64    |        | Ubuntu Server 22.04 |        | AArch64      |        | gcc                                  |
| BSD-x86\_64      |        | FreeBSD 13.2        |        | x86\_64      |        | Clang 11                             |
| VC-WIN64A        |        | Windows Server 2019 |        | x86\_64      |        | Visual Studio 2019 Community Edition |
| VC-WIN32         |        | Windows Server 2019 |        | x86          |        | Visual Studio 2019 Community Edition |
| mingw64          |        | Windows Server 2019 |        | x86\_64      |        | MinGW (64 bit) and MSYS2             |
| darwin64-x86\_64 |        | Mac OS Ventura (13) |        | x86\_64      |        | Apple clang 14                       |
| darwin64-arm64   |        | Mac OS Sonoma (14)  |        | AArch64 (M1) |        | Apple clang 15                       |

## Current secondary platforms

| Target       | &nbsp; | O/S         | &nbsp; | Architecture | &nbsp; | Toolchain       | &nbsp; | Nominated Committer(s) | &nbsp; | Nominated Community Maintainer(s) |
|--------------|--------|-------------|--------|--------------|--------|-----------------|--------|------------------------|--------|-----------------------------------|
| vms-ia64     |        | OpenVMS 8.4 |        | ia64         |        | VSI C 7.4       |        | \@levitte              |        |                                   |
| vms-ia64-p32 |        | OpenVMS 8.4 |        | ia64         |        | VSI C 7.4 [^1]  |        | \@levitte              |        |                                   |
| vms-ia64-p64 |        | OpenVMS 8.4 |        | ia64         |        | VSI C 7.4 [^2]  |        | \@levitte              |        |                                   |
| vms-x86\_64  |        | OpenVMS 8.4 |        | x86\_64      |        | VSI C X7.4 [^3] |        | \@levitte              |        |                                   |

[^1]: [VMS] 32 bit pointer build
[^2]: [VMS] 64 bit pointer build
[^3]: [VMS] cross compile on ia64, currently build only

## Current community platforms

| Target                  | &nbsp; | O/S                | &nbsp; | Architecture            | &nbsp; | Toolchain       | &nbsp; | Nominated Community Member(s)                           |
|-------------------------|--------|--------------------|--------|-------------------------|--------|-----------------|--------|---------------------------------------------------------|
| vms-alpha               |        | OpenVMS 8.4        |        | alpha                   |        | VSI C 7.4       |        | \@levitte                                               |
| vms-alpha-p32           |        | OpenVMS 8.4        |        | alpha                   |        | VSI C 7.4 [^1]  |        | \@levitte                                               |
| vms-alpha-p64           |        | OpenVMS 8.4        |        | alpha                   |        | VSI C 7.4 [^2]  |        | \@levitte                                               |
| nonstop-nsx             |        | NonStop OSS L21.06 |        | x86\_64 ilp32           |        | c99             |        | \@rsbeckerca                                            |
| nonstop-nsx\_put        |        | NonStop OSS L21.06 |        | x86\_64 ilp32 PUT       |        | c99             |        | \@rsbeckerca                                            |
| nonstop-nsx\_64         |        | NonStop OSS L21.06 |        | x86\_64 lp64            |        | c99             |        | \@rsbeckerca                                            |
| nonstop-nsx\_64\_put    |        | NonStop OSS L21.06 |        | x86\_64 lp64 PUT        |        | c99             |        | \@rsbeckerca                                            |
| nonstop-nsx\_spt        |        | NonStop OSS L21.06 |        | x86\_64 ilp32 SPT       |        | c99             |        | \@rsbeckerca                                            |
| nonstop-nsx\_spt\_floss |        | NonStop OSS L21.06 |        | x86\_64 ilp32 SPT FLOSS |        | c99             |        | \@rsbeckerca                                            |
| nonstop-nsv             |        | NonStop OSS L21.06 |        | x86\_64 ilp32           |        | c99             |        | \@rsbeckerca                                            |
| nonstop-nse             |        | NonStop OSS J06.22 |        | ia64 ilp32              |        | c99             |        | \@rsbeckerca                                            |
| nonstop-nse\_put        |        | NonStop OSS J06.22 |        | ia64 ilp32 PUT          |        | c99             |        | \@rsbeckerca                                            |
| nonstop-nse\_64         |        | NonStop OSS J06.22 |        | ia64 lp64               |        | c99             |        | \@rsbeckerca                                            |
| nonstop-nse\_64\_put    |        | NonStop OSS J06.22 |        | ia64 lp64 PUT           |        | c99             |        | \@rsbeckerca                                            |
| nonstop-nse\_spt        |        | NonStop OSS J06.22 |        | ia64 ipl32 SPT          |        | c99             |        | \@rsbeckerca                                            |
| nonstop-nse\_spt\_floss |        | NonStop OSS J06.22 |        | ia64 ipl32 SPT FLOSS    |        | c99             |        | \@rsbeckerca                                            |
| linux64-loongarch64     |        | Linux              |        | loongarch64             |        | gcc             |        | \@shipujin                                              |
| BSD-armv4               |        | FreeBSD            |        | armv4                   |        | LLVM            |        | \@pkubaj                                                |
| BSD-ppc                 |        | FreeBSD            |        | ppc                     |        | LLVM            |        | \@pkubaj                                                |
| BSD-ppc64               |        | FreeBSD            |        | ppc64                   |        | LLVM            |        | \@pkubaj                                                |
| BSD-ppc64le             |        | FreeBSD            |        | ppc64le                 |        | LLVM            |        | \@pkubaj                                                |
| BSD-riscv64             |        | FreeBSD            |        | riscv64                 |        | LLVM            |        | \@pkubaj                                                |
| solaris64-x86\_64-gcc   |        | Solaris            |        | x86\_64                 |        | gcc             |        | \@orcl-jlana \@cernoseka                                |
| solaris64-x86\_64-cc    |        | Solaris            |        | x86\_64                 |        | Sun C           |        | \@orcl-jlana \@cernoseka                                |
| solaris64-sparcv9-gcc   |        | Solaris            |        | Sparc V9 64 bit         |        | gcc             |        | \@orcl-jlana \@cernoseka                                |
| solaris64-sparcv9-cc    |        | Solaris            |        | Sparc V9 64 bit         |        | Sun C           |        | \@orcl-jlana \@cernoseka                                |
| linux64-s390x           |        | Linux              |        | s390x                   |        | gcc             |        | \@holger-dengler \@ifranzki                             |
| hurd-x86                |        | Hurd               |        | x86                     |        | gcc             |        | \@sthibaul                                              |
| hurd-x86\_64            |        | Hurd               |        | x86\_64                 |        | gcc             |        | \@sthibaul                                              |
| ios-xcrun               |        | iOS                |        | armv7                   |        | Apple clang 12  |        | \@fwh-dc                                                |
| ios64-xcrun             |        | iOS                |        | aarch64                 |        | Apple clang 12  |        | \@fwh-dc                                                |
| iossimulator-xcrun      |        | iOS Simulator      |        | x86\_64 or aarch64      |        | Apple clang 12  |        | \@fwh-dc                                                |
| iossimulator-arm64-xcrun|        | iOS Simulator      |        | aarch64                 |        | Apple clang 12  |        | \@fwh-dc                                                |
| iphoneos-cross          |        | iOS                |        | ?                       |        | Apple clang 12  |        | \@fwh-dc                                                |
| ios-cross               |        | iOS                |        | armv7                   |        | Apple clang 12  |        | \@fwh-dc                                                |
| ios64-cross             |        | iOS                |        | aarch64                 |        | Apple clang 12  |        | \@fwh-dc                                                |
| linux-ppc64le           |        | Linux              |        | ppc64 little endian     |        | gcc             |        | \@rohanmclure \@erichte-ibm \@naynajain                 |

## Current unadopted platforms

| Target                 | &nbsp; | O/S                               | &nbsp; | Architecture        | &nbsp; | Toolchain               |
|------------------------|--------|-----------------------------------|--------|---------------------|--------|-------------------------|
| vos-gcc                |        | VOS                               |        | ??                  |        | gcc                     |
| solaris-x86-gcc        |        | Solaris                           |        | x86                 |        | gcc                     |
| solaris-sparcv7-gcc    |        | Solaris                           |        | Sparc V7            |        | gcc                     |
| solaris-sparcv8-gcc    |        | Solaris                           |        | Sparc V8            |        | gcc                     |
| solaris-sparcv9-gcc    |        | Solaris                           |        | Sparc V9 32 bit     |        | gcc                     |
| solaris-sparcv7-cc     |        | Solaris                           |        | Sparc V7            |        | Sun C                   |
| solaris-sparcv8-cc     |        | Solaris                           |        | Sparc V8            |        | Sun C                   |
| solaris-sparcv9-cc     |        | Solaris                           |        | Sparc V9 32 bit     |        | Sun C                   |
| irix-mips3-gcc         |        | Irix 6.x                          |        | mips64 n32          |        | gcc                     |
| irix-mips3-cc          |        | Irix 6.x                          |        | mips64 n32          |        | ??                      |
| irix64-mips4-gcc       |        | Irix 6.x                          |        | mips64 n64          |        | gcc                     |
| irix64-mips4-cc        |        | Irix 6.x                          |        | mips64 n64          |        | ??                      |
| hpux-parisc-gcc        |        | HP-UX                             |        | parisc              |        | gcc                     |
| hpux-parisc1\_1-gcc    |        | HP-UX                             |        | parisc 1.1 32 bit   |        | gcc                     |
| hpux64-parisc2-gcc     |        | HP-UX                             |        | parisc 2.0 64 bit   |        | gcc                     |
| hpux-parisc-cc         |        | HP-UX                             |        | parisc              |        | ??                      |
| hpux-parisc1\_1-cc     |        | HP-UX                             |        | parisc 1.0 32 bit   |        | ??                      |
| hpux64-parisc2-cc      |        | HP-UX                             |        | parisc 2.0 64 bit   |        | ??                      |
| hpux-ia64-cc           |        | HP-UX                             |        | IA64 32 bit         |        | ??                      |
| hpux64-ia64-cc         |        | HP-UX                             |        | IA64 64 bit         |        | ??                      |
| hpux-ia64-gcc          |        | HP-UX                             |        | IA64 32 bit         |        | gcc                     |
| hpux64-ia64-gcc        |        | HP-UX                             |        | IA64 64 bit         |        | gcc                     |
| MPE/iX-gcc             |        | MPE/iX                            |        | parisc?             |        | gcc                     |
| tru64-alpha-gcc        |        | Tru64                             |        | alpha               |        | gcc                     |
| tru64-alpha-cc         |        | Tru64                             |        | alpha               |        | ??                      |
| linux-ppc              |        | Linux                             |        | ppc32               |        | gcc                     |
| linux-ppc64            |        | Linux                             |        | ppc64 big endian    |        | gcc                     |
| linux-armv4            |        | Linux                             |        | armv4               |        | gcc                     |
| linux-arm64ilp32       |        | Linux                             |        | aarch64-ilp32       |        | gcc                     |
| linux-mips32           |        | Linux                             |        | mips32 o32          |        | gcc                     |
| linux-mips64           |        | Linux                             |        | mips64 n32          |        | gcc                     |
| linux64-mips64         |        | Linux                             |        | mips64 64 bit       |        | gcc                     |
| linux64-riscv64        |        | Linux                             |        | riscv64             |        | gcc                     |
| linux-x86-clang        |        | Linux                             |        | x86                 |        | clang                   |
| linux-x86\_64-clang    |        | Linux                             |        | x86\_64             |        | clang                   |
| linux-x32              |        | Linux                             |        | x86\_64 x32         |        | gcc                     |
| linux-ia64             |        | Linux                             |        | ia64                |        | gcc                     |
| linux32-s390x          |        | Linux                             |        | s390x 31 bit        |        | gcc                     |
| linux-sparcv8          |        | Linux                             |        | sparc v8            |        | gcc                     |
| linux-sparcv9          |        | Linux                             |        | sparc v9 32 bit     |        | gcc                     |
| linux64-sparcv9        |        | Linux                             |        | sparc v9 64 bit     |        | gcc                     |
| linux-alpha-gcc        |        | Linux                             |        | alpha               |        | gcc                     |
| linux-c64xplus         |        | Linux                             |        | c64xplus            |        | gcc                     |
| linux-c64xplus         |        | Linux                             |        | c64xplus            |        | gcc                     |
| BSD-x86                |        | FreeBSD / OpenBSD / NetBSD / ?    |        | x86 a.out           |        | ??                      |
| BSD-x86-elf            |        | FreeBSD / OpenBSD / NetBSD / ?    |        | x86 elf             |        | ??                      |
| BSD-sparcv8            |        | ?                                 |        | Sparc v8            |        | ??                      |
| BSD-sparcv9            |        | ?                                 |        | Sparc v9 32 bit     |        | ??                      |
| BSD-ia64               |        | ?                                 |        | IA64                |        | ??                      |
| BSD-x86\_64            |        | OpenBSD / NetBSD / ?              |        | x86\_64             |        | ??                      |
| bsdi-elf-gcc           |        | BSDi                              |        | ??                  |        | ??                      |
| unixware-2.0           |        | unixware 2.0                      |        | ??                  |        | ??                      |
| unixware-2.1           |        | unixware 2.1                      |        | ??                  |        | ??                      |
| unixware-7             |        | unixware 7                        |        | x86                 |        | ??                      |
| unixware-7-gcc         |        | unixware 7                        |        | x86                 |        | gcc                     |
| sco5-cc                |        | Open Server 5?                    |        | x86                 |        | ??                      |
| sco5-gcc               |        | Open Server 5?                    |        | x86                 |        | gcc                     |
| aix-gcc                |        | AIX                               |        | ppc32               |        | gcc                     |
| aix64-gcc              |        | AIX                               |        | ppc64               |        | gcc                     |
| aix64-gcc-as           |        | AIX                               |        | ppc64               |        | gcc with as?            |
| aix-cc                 |        | AIX                               |        | ppc32               |        | ??                      |
| aix64-cc               |        | AIX                               |        | ppc64               |        | ??                      |
| BS2000-OSD             |        | BS2000/OSD                        |        | ??                  |        | ??                      |
| VC-WIN64I              |        | Windows XP / Windows Server 2008? |        | ia64                |        | Visual C                |
| VC-CE                  |        | Windows CE                        |        | x86 / armv4?        |        | Visual C                |
| VC-WIN64A-masm         |        | Windows 10                        |        | x86                 |        | Visual C with masm      |
| mingw                  |        | Windows 10?                       |        | x86                 |        | gcc                     |
| UEFI-x86               |        | UEFI                              |        | x86                 |        | ??                      |
| UEFI-x86\_64           |        | UEFI                              |        | x86\_64             |        | ??                      |
| UWIN                   |        | UWIN                              |        | x86                 |        |                         |
| Cygwin-x86             |        | Windows 10                        |        | x86                 |        | gcc                     |
| Cygwin-x86\_64         |        | Windows 10                        |        | x86\_64             |        | gcc                     |
| darwin-ppc             |        | MacOS?                            |        | ppc32               |        |                         |
| darwin64-ppc           |        | MacOS?                            |        | ppc64               |        |                         |
| darwin-i386            |        | MacOS?                            |        | x86                 |        |                         |
| darwin-i386            |        | MacOS?                            |        | x86                 |        |                         |
| vxworks-ppc60x         |        | vxworks                           |        | ppc32               |        |                         |
| vxworks-ppcgen         |        | vxworks                           |        | ppc32               |        |                         |
| vxworks-ppc405         |        | vxworks                           |        | ppc32 405           |        |                         |
| vxworks-ppc750         |        | vxworks                           |        | ppc32 750           |        |                         |
| vxworks-ppc860         |        | vxworks                           |        | ppc32 860           |        |                         |
| vxworks-simlinux       |        | vxworks                           |        | x86?                |        |                         |
| vxworks-mips           |        | vxworks                           |        | mips32 o32          |        |                         |
| uClinux-dist           |        | uClinux                           |        | ?                   |        | gcc                     |
| uClinux-dist64         |        | uClinux                           |        | ?                   |        | gcc                     |
| android-arm            |        | android                           |        | armv4               |        |                         |
| android-arm64          |        | android                           |        | aarch64             |        |                         |
| android-mips           |        | android                           |        | mips32 o32          |        |                         |
| android-mips64         |        | android                           |        | mips64              |        |                         |
| android-x86            |        | android                           |        | x86                 |        |                         |
| android-x86\_64        |        | android                           |        | x86\_64             |        |                         |
| BC-32                  |        | Windows 10?                       |        | x86                 |        | Borland C, C++ Builder? |
| DJGPP                  |        | DOS?                              |        | x86?                |        | djgpp                   |
| haiku-x86              |        | Haiku                             |        | x86                 |        | gcc?                    |
| haiku-x86\_64          |        | Haiku                             |        | x86\_64             |        | gcc?                    |
| nonstop-nsx\_g         |        | NonStop Guardian                  |        | x86\_64 ilp32       |        |                         |
| nonstop-nsx\_g\_tandem |        | NonStop Guardian                  |        | x86\_64 ilp32       |        |                         |
| nonstop-nse\_g         |        | NonStop Guardian                  |        | ia64 ipl32          |        |                         |
| nonstop-nse\_g\_tandem |        | NonStop Guardian                  |        | ia64 ipl32          |        |                         |
| OS390-Unix             |        | zOS                               |        | s390                |        |                         |
| VC-WIN32-ONECORE       |        | Windows OneCore                   |        | x86                 |        | Visual C                |
| VC-WIN64A-ONECORE      |        | Windows OneCore                   |        | x86\_64             |        | Visual C                |
| VC-WIN32-ARM           |        | Windows OneCore                   |        | arm                 |        | Visual C                |
| VC-WIN64-ARM           |        | Windows OneCore                   |        | aarch64             |        | Visual C                |
| VC-WIN32-UWP           |        | Windows UWP                       |        | x86                 |        | Visual C                |
| VC-WIN64A-UWP          |        | Windows UWP                       |        | x86\_64             |        | Visual C                |
| VC-ARM-UWP             |        | Windows UWP                       |        | arm                 |        | Visual C                |
| VC-ARM64-UWP           |        | Windows UWP                       |        | aarch64             |        | Visual C                |
