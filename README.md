# Awesome Android Reverse Engineering & Modding

> A curated directory of tools, frameworks, and repositories for Android and native C/C++ security analysis, reverse engineering, and app modding.

![Awesome](https://img.shields.io/badge/awesome-list-blue)
![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen)
![License](https://img.shields.io/badge/license-CC0--1.0-lightgrey)
![Last Updated](https://img.shields.io/badge/updated-YYYY--MM--DD-informational)

---

## Table of Contents

- [About](#about)
- [Legal & Ethical Use](#legal--ethical-use)
- [Android Reverse Engineering & Decompilation](#android-reverse-engineering--decompilation)
- [Native C/C++ Disassembling & Debugging](#native-cc-disassembling--debugging)
- [Hooking Frameworks (ART and Native)](#hooking-frameworks-art-and-native)
- [API Bypasses and System Modifications](#api-bypasses-and-system-modifications)
- [Scripting & Instrumentation](#scripting--instrumentation)
- [Deobfuscation & Unpacking Tools](#deobfuscation--unpacking-tools)
- [Learning Resources](#learning-resources)
- [Contributing](#contributing)
- [License](#license)

---

## About

This list collects well-regarded tools for analyzing, instrumenting, and modifying Android applications across both the managed layer (Java/Kotlin, Dalvik/ART bytecode) and the native layer (C/C++, JNI, ELF shared libraries).

**Inclusion criteria**

- Actively maintained, or historically important and still widely referenced
- Clear documentation and a public repository or official site
- Relevant to security research, malware analysis, interoperability, or app modding

**Legend**

| Tag | Meaning |
|-----|---------|
| 🟢 | Open source |
| 🔒 | Commercial / closed source |
| 🕰️ | Unmaintained, kept for reference |

---

## Legal & Ethical Use

The tools listed here are intended for **security research, education, interoperability, and modification of software you own or are authorized to test**. Always:

- Obtain written permission before testing apps or services you do not own.
- Respect software licenses, terms of service, and applicable laws (e.g., DMCA, CFAA, and local equivalents).
- Follow responsible disclosure practices when you discover vulnerabilities.

The maintainers of this list do not condone misuse.

---

## Android Reverse Engineering & Decompilation

Tools for unpacking APKs, decompiling DEX bytecode to Java/Kotlin-like source, and editing smali.

| Tool | Description |
|------|-------------|
| [JADX](https://github.com/skylot/jadx) 🟢 | DEX-to-Java decompiler with CLI and GUI, built-in deobfuscation, and a searchable, cross-referenced code view. |
| [Apktool](https://github.com/iBotPeaches/Apktool) 🟢 | Decodes resources and disassembles DEX to smali, then rebuilds modified APKs. The standard for repackaging workflows. |
| [smali / baksmali](https://github.com/JesusFreke/smali) 🟢 | Assembler and disassembler for the Dalvik executable format; the foundation of most bytecode-level patching. |
| [Bytecode Viewer](https://github.com/Konloch/bytecode-viewer) 🟢 | Java/Android bytecode viewer and editor that bundles multiple decompilers for side-by-side comparison. |
| [dex2jar](https://github.com/pxb1988/dex2jar) 🟢 | Converts DEX to JAR so standard Java analysis tools can be applied. |
| [Recaf](https://github.com/Col-E/Recaf) 🟢 | Modern Java bytecode editor with decompilation, assembler, and a plugin system. |
| [Androguard](https://github.com/androguard/androguard) 🟢 | Python framework for static analysis of APK/DEX/AXML files, including call-graph generation and signature checks. |
| [APKLab](https://github.com/APKLab/APKLab) 🟢 | VS Code extension that integrates Apktool, JADX, and signing into a single reverse engineering workflow. |
| [MobSF](https://github.com/MobSF/Mobile-Security-Framework-MobSF) 🟢 | Automated static and dynamic analysis framework for Android, iOS, and Windows mobile apps. |
| [uber-apk-signer](https://github.com/patrickfav/uber-apk-signer) 🟢 | CLI utility for zip-aligning and signing rebuilt APKs across signature schemes. |

---

## Native C/C++ Disassembling & Debugging

Tools for analyzing ELF binaries (`.so`), ARM/ARM64/x86 disassembly, and native debugging.

### Disassemblers & Decompilers

| Tool | Description |
|------|-------------|
| [Ghidra](https://github.com/NationalSecurityAgency/ghidra) 🟢 | NSA's software reverse engineering suite with a powerful decompiler, scripting support, and multi-architecture processors. |
| [IDA Pro / IDA Free](https://hex-rays.com/ida-pro) 🔒 | Industry-standard interactive disassembler with the Hex-Rays decompiler and extensive plugin ecosystem. |
| [Binary Ninja](https://binary.ninja) 🔒 | Modern reverse engineering platform with intermediate languages (BNIL) and a clean scripting API. |
| [Rizin](https://github.com/rizinorg/rizin) 🟢 | Reverse engineering framework and command-line toolset, forked from radare2. |
| [Cutter](https://github.com/rizinorg/cutter) 🟢 | Free GUI for Rizin with a Ghidra decompiler integration. |
| [radare2](https://github.com/radareorg/radare2) 🟢 | Portable, scriptable reverse engineering framework with disassembly, debugging, and patching capabilities. |

### Debuggers

| Tool | Description |
|------|-------------|
| [GDB / gdbserver](https://sourceware.org/gdb/) 🟢 | GNU debugger; `gdbserver` from the Android NDK enables remote debugging of native processes. |
| [LLDB](https://lldb.llvm.org/) 🟢 | LLVM debugger, used by Android Studio for native debugging. |
| [pwndbg](https://github.com/pwndbg/pwndbg) 🟢 | GDB/LLDB plugin that improves exploit development and reverse engineering ergonomics. |
| [GEF](https://github.com/hugsy/gef) 🟢 | Feature-rich GDB enhancement for reverse engineers and exploit developers. |

### Supporting Libraries

| Tool | Description |
|------|-------------|
| [Capstone](https://github.com/capstone-engine/capstone) 🟢 | Lightweight multi-architecture disassembly framework. |
| [Keystone](https://github.com/keystone-engine/keystone) 🟢 | Multi-architecture assembler framework. |
| [Unicorn](https://github.com/unicorn-engine/unicorn) 🟢 | Lightweight multi-architecture CPU emulator framework. |
| [Android NDK](https://developer.android.com/ndk) 🟢 | Official toolchain including `objdump`, `readelf`, `llvm-*` utilities, and symbolication tools. |

---

## Hooking Frameworks (ART and Native)

Frameworks that intercept and modify behavior at the Java/ART layer or the native layer at runtime.

### ART / Java Layer

| Tool | Description |
|------|-------------|
| [LSPosed](https://github.com/LSPosed/LSPosed) 🟢 | Xposed-compatible framework built on ART hooking via Magisk/Zygisk; enables per-app module scoping without modifying APKs. |
| [LSPatch](https://github.com/LSPosed/LSPatch) 🟢 | Non-root Xposed-style framework that embeds hooks by repackaging the target APK. |
| [LSPlant](https://github.com/LSPosed/LSPlant) 🟢 | Standalone ART hooking library used by LSPosed for Android 5.0+ method hooking. |
| [Xposed API (XposedBridge)](https://github.com/rovo89/XposedBridge) 🕰️ | Original Xposed API that defined the module development model still followed by modern frameworks. |
| [Pine](https://github.com/canyie/pine) 🟢 | Dynamic Java method hook framework for ART, usable within a single app process. |
| [SandHook](https://github.com/asLody/SandHook) 🕰️ | Android ART hook library supporting a wide range of Android versions. |
| [Epic](https://github.com/tiann/epic) 🕰️ | Dynamic Java method hooking library for ART in the app process. |

### Native Layer

| Tool | Description |
|------|-------------|
| [Frida](https://github.com/frida/frida) 🟢 | Dynamic instrumentation toolkit that hooks both Java and native functions from JavaScript, with cross-platform support. |
| [Dobby](https://github.com/jmpews/Dobby) 🟢 | Lightweight, multi-platform inline hook framework for native code. |
| [ShadowHook](https://github.com/bytedance/android-inline-hook) 🟢 | ByteDance's Android inline hook library for ARM/ARM64 with stability-focused design. |
| [xHook](https://github.com/iqiyi/xHook) 🕰️ | PLT/GOT hook library for Android native ELF files. |

---

## API Bypasses and System Modifications

Tools for analysis environments, traffic inspection, certificate handling, and system-level customization. Use only on devices and applications you own or are authorized to test.

### Root & System Frameworks

| Tool | Description |
|------|-------------|
| [Magisk](https://github.com/topjohnwu/Magisk) 🟢 | Systemless root solution and module platform, including Zygisk for in-process module injection. |
| [KernelSU](https://github.com/tiann/KernelSU) 🟢 | Kernel-based root solution with per-app profiles and module support. |
| [APatch](https://github.com/bmax121/APatch) 🟢 | Kernel- and system-patching root solution with an integrated module system. |

### Traffic Analysis & Certificate Handling

| Tool | Description |
|------|-------------|
| [mitmproxy](https://github.com/mitmproxy/mitmproxy) 🟢 | Interactive HTTPS proxy for inspecting and modifying traffic during security testing. |
| [Burp Suite](https://portswigger.net/burp) 🔒 | Web and mobile application security testing platform with an intercepting proxy. |
| [MagiskTrustUserCerts](https://github.com/NVISOsecurity/MagiskTrustUserCerts) 🟢 | Magisk module that moves user-installed CA certificates into the system trust store for testing. |
| [apk-mitm](https://github.com/niklashigi/apk-mitm) 🟢 | Automatically patches APKs to allow HTTPS inspection by adjusting network security config. |
| [objection](https://github.com/sensepost/objection) 🟢 | Frida-powered runtime exploration toolkit with built-in helpers for pinning analysis and keystore/filesystem inspection. |
| [reFlutter](https://github.com/Impact-I/reFlutter) 🟢 | Framework for reverse engineering Flutter apps using a patched Flutter engine. |
| [TrustMeAlready](https://github.com/ViRb3/TrustMeAlready) 🕰️ | Xposed module that disables certificate validation checks in target apps for testing. |

### App Patching & Modding

| Tool | Description |
|------|-------------|
| [ReVanced](https://github.com/ReVanced) 🟢 | Open-source patcher framework for applying modular patches to Android apps. |
| [Xposed Modules Repository](https://modules.lsposed.org/) 🟢 | Community index of LSPosed-compatible modules for system and app customization. |

---

## Scripting & Instrumentation

Tools that enable automation, tracing, and emulation for dynamic analysis.

| Tool | Description |
|------|-------------|
| [frida-tools](https://github.com/frida/frida) 🟢 | CLI utilities (`frida`, `frida-trace`, `frida-ps`) for scripting and tracing running processes. |
| [Frida CodeShare](https://codeshare.frida.re/) 🟢 | Community repository of reusable Frida scripts. |
| [r2frida](https://github.com/nowsecure/r2frida) 🟢 | Bridges radare2 and Frida for combined static and dynamic analysis. |
| [jnitrace](https://github.com/chame1eon/jnitrace) 🟢 | Traces JNI API calls made from native libraries, built on Frida. |
| [frida-il2cpp-bridge](https://github.com/vfsfitvnm/frida-il2cpp-bridge) 🟢 | Frida module for inspecting and instrumenting Unity IL2CPP applications at runtime. |
| [Il2CppDumper](https://github.com/Perfare/Il2CppDumper) 🟢 | Extracts type and method metadata from Unity IL2CPP binaries to aid reverse engineering. |
| [Dexcalibur](https://github.com/FrenchYeti/dexcalibur) 🟢 | Android reverse engineering platform that automates hook generation and analysis using Frida. |
| [drozer](https://github.com/WithSecureLabs/drozer) 🟢 | Security assessment framework for Android app attack surface and IPC analysis. |
| [Inspeckage](https://github.com/ac-pm/Inspeckage) 🕰️ | Xposed-based dynamic analysis tool with a web interface for monitoring app behavior. |
| [Qiling Framework](https://github.com/qilingframework/qiling) 🟢 | Scriptable binary emulation framework supporting multiple platforms and architectures. |
| [unidbg](https://github.com/zhkl0228/unidbg) 🟢 | Emulator for calling and analyzing Android/iOS native libraries without a device. |
| [Ghidrathon](https://github.com/mandiant/Ghidrathon) 🟢 | Enables Python 3 scripting in Ghidra. |

---

## Deobfuscation & Unpacking Tools

Tools for identifying protectors, reversing obfuscation, and recovering original code from packed applications.

### Identification

| Tool | Description |
|------|-------------|
| [APKiD](https://github.com/rednaga/APKiD) 🟢 | Identifies compilers, packers, obfuscators, and protectors used in Android apps. |

### Deobfuscation

| Tool | Description |
|------|-------------|
| [Simplify](https://github.com/CalebFenton/simplify) 🕰️ | Generic Android deobfuscator that uses virtual execution to simplify obfuscated code. |
| [Java Deobfuscator](https://github.com/java-deobfuscator/deobfuscator) 🟢 | Deobfuscation tool targeting common Java obfuscators. |
| [JADX (deobfuscation mode)](https://github.com/skylot/jadx) 🟢 | Renames obfuscated identifiers to readable names to improve navigation. |
| [Miasm](https://github.com/cea-sec/miasm) 🟢 | Reverse engineering framework with symbolic execution and IR lifting for code simplification. |

### Unpacking & Dumping

| Tool | Description |
|------|-------------|
| [frida-dexdump](https://github.com/hluwa/frida-dexdump) 🟢 | Locates and dumps DEX files from process memory using Frida. |
| [BlackDex](https://github.com/CodingGay/BlackDex) 🟢 | On-device DEX unpacker that requires no root. |
| [FART](https://github.com/hanbinglengyue/FART) 🕰️ | ART-based active-invocation unpacker for recovering protected DEX methods. |
| [DexHunter](https://github.com/zyq8709/DexHunter) 🕰️ | Modified Dalvik runtime approach for extracting DEX files from packed apps. |

---

## Learning Resources

- [OWASP Mobile Application Security (MAS)](https://mas.owasp.org/) — testing guide, weakness taxonomy, and checklists
- [Android Developers: Security](https://developer.android.com/privacy-and-security/security-tips) — official platform security documentation
- [Frida Documentation](https://frida.re/docs/home/) — official handbook and API reference
- [Ghidra Documentation](https://ghidra-sre.org/) — official site with cheat sheets and training material
- Add books, courses, CTFs, and blogs here

---

## Contributing

Contributions are welcome. Before opening a pull request:

1. Confirm the tool is not already listed.
2. Place it in the most relevant category, in alphabetical order where practical.
3. Use this format:

   ```md
   | [Tool Name](https://link) 🟢 | One-sentence, neutral description of what it does. |
   ```

4. Verify that the link works and that the project is maintained, or mark it 🕰️.
5. Avoid promotional language and do not add tools whose primary purpose is malicious.

See [CONTRIBUTING.md](CONTRIBUTING.md) for full guidelines.

---

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the contributors have waived all copyright and related rights to this work.
