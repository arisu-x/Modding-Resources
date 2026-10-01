# Modding Resources

> A practical, searchable directory of tools and learning resources for Android modding, reverse engineering, native analysis, malware research, networking, and software development.

[![Awesome List](https://img.shields.io/badge/awesome-list-2ea44f?logo=github)](https://github.com/sindresorhus/awesome)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![License: CC0](https://img.shields.io/badge/license-CC0--1.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

Find a tool quickly with `Ctrl`/`Cmd` + `F`, or start with one of the curated paths below.

## Quick navigation

| I want to… | Start here |
|---|---|
| Modify an Android APK | [Android workflow](QUICK_START.md#android-apk-workflow) |
| Inspect Java, Kotlin, or DEX code | [Android reverse engineering](#android-reverse-engineering) |
| Analyze a native `.so` or executable | [Native and binary analysis](#native-and-binary-analysis) |
| Instrument a running app | [Dynamic instrumentation](#dynamic-instrumentation-and-hooking) |
| Learn from beginner to advanced | [Learning paths](LEARNING_PATHS.md) |
| Choose tools by operating system | [Platform matrix](TOOLS_BY_PLATFORM.md) |
| Find a category or understand its scope | [Category guide](CATEGORIES.md) |
| Add a resource | [Contributing guide](CONTRIBUTING.md) |

## Contents

- [Responsible use](#responsible-use)
- [Android reverse engineering](#android-reverse-engineering)
- [Dynamic instrumentation and hooking](#dynamic-instrumentation-and-hooking)
- [Root, patching, and system modification](#root-patching-and-system-modification)
- [Native and binary analysis](#native-and-binary-analysis)
- [Networking and protocol analysis](#networking-and-protocol-analysis)
- [Malware analysis and threat research](#malware-analysis-and-threat-research)
- [Cryptography and data formats](#cryptography-and-data-formats)
- [Automation, emulation, and scripting](#automation-emulation-and-scripting)
- [Developer and workflow tools](#developer-and-workflow-tools)
- [Game modding](#game-modding)
- [Learning resources](#learning-resources)
- [Guides](#guides)

## Responsible use

Use these resources only on software, devices, accounts, and networks that you own or are authorized to test. Respect licenses, terms of service, privacy, and applicable laws. Do not use this list to bypass payments, steal accounts, evade security controls, or distribute malware. Prefer legal training targets, CTFs, open-source projects, and responsible disclosure.

## Android reverse engineering

| Resource | Best for |
|---|---|
| [JADX](https://github.com/skylot/jadx) | Reading DEX as Java-like source with GUI and CLI workflows |
| [Apktool](https://github.com/iBotPeaches/Apktool) | Decoding resources, editing smali, and rebuilding APKs |
| [smali/baksmali](https://github.com/JesusFreke/smali) | Dalvik bytecode assembly and disassembly |
| [Android Studio](https://developer.android.com/studio) | Building, debugging, profiling, and inspecting Android projects |
| [APKLab](https://github.com/Surendrajat/APKLab) | VS Code-based APK reverse engineering workflow |
| [Androguard](https://github.com/androguard/androguard) | Python automation and static analysis of APK/DEX/AXML |
| [MobSF](https://github.com/MobSF/Mobile-Security-Framework-MobSF) | Automated mobile application security testing |
| [uber-apk-signer](https://github.com/patrickfav/uber-apk-signer) | Zip alignment and APK signing |
| [APKiD](https://github.com/rednaga/APKiD) | Identifying packers, obfuscators, and compilers |
| [ReVanced](https://github.com/ReVanced) | Open-source, modular patching framework |

## Dynamic instrumentation and hooking

| Resource | Best for |
|---|---|
| [Frida](https://github.com/frida/frida) | Runtime instrumentation across Java and native code |
| [frida-tools](https://github.com/frida/frida-tools) | Frida CLI utilities and tracing |
| [Frida documentation](https://frida.re/docs/home/) | Official API and usage reference |
| [LSPosed](https://github.com/LSPosed/LSPosed) | ART/Xposed-compatible modules on rooted devices |
| [LSPatch](https://github.com/LSPosed/LSPatch) | Non-root APK-integrated hooking experiments |
| [Pine](https://github.com/canyie/pine) | In-process ART method hooking |
| [Dobby](https://github.com/jmpews/Dobby) | Lightweight native inline hooks |
| [ShadowHook](https://github.com/bytedance/android-inline-hook) | Android ARM/ARM64 native inline hooks |
| [Frida CodeShare](https://codeshare.frida.re/) | Community scripts; review before running |
| [objection](https://github.com/sensepost/objection) | Frida-powered runtime exploration |

## Root, patching, and system modification

| Resource | Best for |
|---|---|
| [Magisk](https://github.com/topjohnwu/Magisk) | Systemless root and module development |
| [KernelSU](https://github.com/tiann/KernelSU) | Kernel-based root and per-app policies |
| [APatch](https://github.com/bmax121/APatch) | Kernel/system patching experiments |
| [LSPosed modules index](https://modules.lsposed.org/) | Discovering community modules |
| [Android platform security](https://source.android.com/docs/security) | Understanding Android security architecture |

## Native and binary analysis

| Resource | Best for |
|---|---|
| [Ghidra](https://github.com/NationalSecurityAgency/ghidra) | Free disassembly, decompilation, and scripting |
| [IDA Free/Pro](https://hex-rays.com/ida-pro) | Interactive disassembly and commercial analysis |
| [Binary Ninja](https://binary.ninja/) | Modern analysis and intermediate languages |
| [Rizin](https://github.com/rizinorg/rizin) | Scriptable reverse engineering framework |
| [Cutter](https://github.com/rizinorg/cutter) | GUI for Rizin |
| [radare2](https://github.com/radareorg/radare2) | CLI disassembly, debugging, and patching |
| [LLDB](https://lldb.llvm.org/) | Native debugging and Android Studio integration |
| [GDB](https://sourceware.org/gdb/) | Portable native debugging |
| [pwndbg](https://github.com/pwndbg/pwndbg) | GDB enhancements for binary analysis |
| [Capstone](https://github.com/capstone-engine/capstone) | Multi-architecture disassembly library |
| [Keystone](https://github.com/keystone-engine/keystone) | Multi-architecture assembler library |
| [Unicorn](https://github.com/unicorn-engine/unicorn) | CPU emulation library |
| [Android NDK](https://developer.android.com/ndk) | Official native build and inspection toolchain |

## Networking and protocol analysis

| Resource | Best for |
|---|---|
| [Wireshark](https://www.wireshark.org/) | Packet capture and protocol inspection |
| [mitmproxy](https://github.com/mitmproxy/mitmproxy) | Interactive HTTP(S) testing proxy |
| [Burp Suite](https://portswigger.net/burp) | Web and mobile security testing |
| [HTTP Toolkit](https://httptoolkit.com/) | Debugging HTTP traffic with a friendly UI |
| [curl](https://curl.se/) | Reproducible HTTP and network requests |
| [Protobuf](https://protobuf.dev/) | Working with structured binary messages |
| [gRPC](https://grpc.io/) | Inspecting and building RPC services |
| [OWASP API Security](https://owasp.org/www-project-api-security/) | API security risks and testing guidance |

## Malware analysis and threat research

| Resource | Best for |
|---|---|
| [REMnux](https://remnux.org/) | Linux toolkit and VM for malware analysis |
| [FLARE-VM](https://github.com/mandiant/flare-vm) | Windows reverse engineering environment |
| [YARA](https://github.com/VirusTotal/yara) | Pattern-based file classification |
| [CAPE Sandbox](https://github.com/kevoreilly/capemon) | Automated malware behavior analysis |
| [Any.Run](https://any.run/) | Interactive sandboxing; check data-sharing terms |
| [VirusTotal](https://www.virustotal.com/) | Multi-engine file and URL intelligence |
| [Sigma](https://github.com/SigmaHQ/sigma) | Portable detection rule format |
| [MITRE ATT&CK](https://attack.mitre.org/) | Adversary tactics, techniques, and procedures |

Run suspicious samples in an isolated lab. Never upload private or sensitive files to public services.

## Cryptography and data formats

| Resource | Best for |
|---|---|
| [CyberChef](https://github.com/gchq/CyberChef) | Safe, repeatable transformations and decoding |
| [OpenSSL](https://www.openssl.org/) | TLS, certificates, hashes, and crypto utilities |
| [Hashcat](https://github.com/hashcat/hashcat) | Authorized password recovery and hash auditing |
| [John the Ripper](https://www.openwall.com/john/) | Authorized password auditing |
| [jq](https://github.com/jqlang/jq) | Querying and transforming JSON |
| [xxd](https://man7.org/linux/man-pages/man1/xxd.1.html) | Hex dumps and binary file inspection |
| [ExifTool](https://exiftool.org/) | Metadata and file-format inspection |
| [Kaitai Struct](https://kaitai.io/) | Describing and parsing binary formats |

## Automation, emulation, and scripting

| Resource | Best for |
|---|---|
| [Qiling](https://github.com/qilingframework/qiling) | Scriptable multi-platform emulation |
| [Unidbg](https://github.com/zhkl0228/unidbg) | Calling Android/iOS native libraries without a device |
| [Ghidra scripts](https://github.com/mandiant/GhidraScripts) | Reusable Ghidra automation examples |
| [Il2CppDumper](https://github.com/Perfare/Il2CppDumper) | Unity IL2CPP metadata analysis |
| [frida-il2cpp-bridge](https://github.com/vfsfitvnm/frida-il2cpp-bridge) | Unity IL2CPP runtime inspection |
| [Python](https://www.python.org/) | General-purpose analysis automation |
| [Go](https://go.dev/) | Fast portable utilities and tooling |
| [PowerShell](https://github.com/PowerShell/PowerShell) | Windows and cross-platform automation |

## Developer and workflow tools

| Resource | Best for |
|---|---|
| [Git](https://git-scm.com/) | Version control and reproducible changes |
| [GitHub CLI](https://cli.github.com/) | GitHub workflows from the terminal |
| [Docker](https://www.docker.com/) | Isolated, repeatable environments |
| [Podman](https://podman.io/) | Daemonless containers |
| [VS Code](https://code.visualstudio.com/) | Lightweight editing and extension-based workflows |
| [Neovim](https://neovim.io/) | Terminal-first, extensible editing |
| [just](https://github.com/casey/just) | Reusable project commands |
| [Task](https://taskfile.dev/) | Cross-platform task automation |
| [pre-commit](https://pre-commit.com/) | Automated formatting and checks |
| [Dev Containers](https://containers.dev/) | Portable development environments |

## Game modding

Use official modding APIs and mod only games you own or are permitted to modify. Avoid cheats, DRM circumvention, multiplayer abuse, and redistribution of copyrighted assets.

| Resource | Best for |
|---|---|
| [BepInEx](https://github.com/BepInEx/BepInEx) | Unity/.NET plugin framework |
| [MelonLoader](https://github.com/LavaGang/MelonLoader) | Unity and Il2Cpp mod loader |
| [Harmony](https://github.com/pardeike/Harmony) | Runtime .NET method patching |
| [Unity documentation](https://docs.unity3d.com/Manual/index.html) | Official Unity development reference |
| [Unreal Engine documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine) | Official Unreal development reference |
| [Godot documentation](https://docs.godotengine.org/) | Open-source engine and scripting reference |

## Learning resources

- [OWASP Mobile Application Security](https://mas.owasp.org/) — mobile testing guide and checklist
- [OWASP Web Security Testing Guide](https://owasp.org/www-project-web-security-testing-guide/) — structured web testing methodology
- [Android Developers](https://developer.android.com/) — official Android platform documentation
- [Android Internals](https://source.android.com/) — AOSP architecture and source documentation
- [Trail of Bits Security Training](https://github.com/trailofbits/training) — practical security exercises
- [pwn.college](https://pwn.college/) — hands-on systems and exploitation education
- [OverTheWire](https://overthewire.org/wargames/) — beginner-friendly security wargames
- [PortSwigger Web Security Academy](https://portswigger.net/web-security) — free web security labs
- [crackmes.one](https://crackmes.one/) — legal reverse engineering challenges
- [CTFtime](https://ctftime.org/) — capture-the-flag events and writeups
- [Ghidra documentation](https://ghidra-sre.org/) — official training material and references

## Guides

- [Quick start](QUICK_START.md) — safe setup and first workflows
- [Category guide](CATEGORIES.md) — what belongs where
- [Learning paths](LEARNING_PATHS.md) — beginner, intermediate, and advanced routes
- [Tools by platform](TOOLS_BY_PLATFORM.md) — Windows, Linux, macOS, and container notes
- [Resources by skill level](RESOURCES_BY_SKILL_LEVEL.md) — a faster starting point for new users

## Contributing

Found a broken link, better replacement, or missing category? See [CONTRIBUTING.md](CONTRIBUTING.md). Keep entries neutral, useful, authorized-use focused, and easy to verify.

## License

This directory is dedicated to the public domain under [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).
