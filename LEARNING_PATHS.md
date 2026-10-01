# Learning Paths

These paths are intentionally tool-light: learn the underlying concepts before collecting more tools.

## Beginner: understand the layers

1. Learn Git, shells, Python basics, files, processes, and permissions.
2. Read the [Android security documentation](https://source.android.com/docs/security).
3. Build a small Android app and inspect your own APK with JADX and Apktool.
4. Practice Java/Kotlin, XML, JSON, HTTP, and basic SQL.
5. Complete beginner labs from [OverTheWire](https://overthewire.org/wargames/) and [pwn.college](https://pwn.college/).

## Intermediate: inspect and instrument

1. Learn Dalvik bytecode, ART, JNI, ELF, ARM64, and memory concepts.
2. Use Ghidra or Cutter on legal crackmes and open-source binaries.
3. Learn Frida scripting and capture observations rather than making assumptions.
4. Study HTTP/TLS with Wireshark and mitmproxy in a controlled lab.
5. Learn common mobile weaknesses through [OWASP MAS](https://mas.owasp.org/).

## Advanced: build reliable tooling

1. Write parsers and automation with Python, Go, or Rust.
2. Study compiler output, calling conventions, loaders, obfuscation, and symbol resolution.
3. Combine static analysis, emulation, and dynamic instrumentation.
4. Create reproducible containers and regression tests for your analysis tools.
5. Publish responsible writeups that identify scope, versions, evidence, and remediation.

## Game modding path

1. Start with official Unity, Unreal, or Godot documentation.
2. Build a small plugin or mod for an open project.
3. Learn the target engine's asset, serialization, and scripting systems.
4. Use BepInEx, MelonLoader, Harmony, or an official SDK only where permitted.
5. Keep offline/single-player experiments separate from competitive or networked games.

## Suggested practice loop

**Question → hypothesis → controlled experiment → evidence → minimal change → test → notes.**

This is more valuable than memorizing a long list of tools.
