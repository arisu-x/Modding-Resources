# Quick Start

This guide gives you a safe, repeatable starting point. Work only with applications, games, devices, and accounts you own or are authorized to test.

## Set up a lab

1. Use a separate Android emulator or test device.
2. Keep personal accounts and private data off the lab device.
3. Install [Android Studio](https://developer.android.com/studio), platform tools, and the [Android SDK](https://developer.android.com/tools).
4. Keep project notes, hashes, versions, and commands in a Git repository.
5. Use snapshots or disposable environments before testing modified packages.

## Android APK workflow

1. **Identify the artifact:** record the package name, version, source, and SHA-256 hash.
2. **Inspect safely:** use [JADX](https://github.com/skylot/jadx), [Apktool](https://github.com/iBotPeaches/Apktool), and [APKiD](https://github.com/rednaga/APKiD).
3. **Understand behavior:** review manifest components, permissions, network configuration, native libraries, and exported activities.
4. **Make a minimal change:** edit only software you are authorized to modify; keep a patch or diff.
5. **Rebuild and sign:** use Apktool and [uber-apk-signer](https://github.com/patrickfav/uber-apk-signer).
6. **Test in isolation:** install on the lab device, capture logs with `adb logcat`, and compare behavior with the original.
7. **Document:** note tool versions, changes, limitations, and rollback steps.

## Native library workflow

1. Extract and hash the `.so` file.
2. Check architecture and symbols with Android NDK tools such as `file`, `readelf`, and `llvm-objdump`.
3. Load a copy into [Ghidra](https://github.com/NationalSecurityAgency/ghidra), [Cutter](https://github.com/rizinorg/cutter), or another suitable analyzer.
4. Use [LLDB](https://lldb.llvm.org/) or [Frida](https://github.com/frida/frida) for authorized runtime observations.
5. Record offsets relative to the exact build; addresses can change between versions.

## Useful habits

- Prefer official documentation and source repositories over random downloads.
- Pin versions when documenting a workflow.
- Never publish credentials, private APKs, personal data, or proprietary assets.
- Treat scripts from community indexes as untrusted until reviewed.
- Use legal challenges such as CTFs and crackmes for practice.
