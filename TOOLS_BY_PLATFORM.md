# Tools by Platform

Platform support changes frequently. Check the linked project documentation before installing.

| Platform | Good starting set | Notes |
|---|---|---|
| Windows | Android Studio, JADX, Apktool, Ghidra, Wireshark, FLARE-VM | Use WSL or a VM for Linux-first tooling. FLARE-VM should be disposable and isolated. |
| Linux | Android SDK/platform-tools, JADX, Apktool, Ghidra, radare2/Rizin, Frida, Wireshark | Strongest choice for scripting, containers, and reproducible labs. |
| macOS | Android Studio, JADX, Apktool, Ghidra, Frida, Wireshark, Docker | Check architecture-specific packages on Apple Silicon. |
| Android device | ADB, Magisk, KernelSU, LSPosed, Frida | Use a dedicated test device and understand bootloader/data-loss implications. |
| Containers | Docker or Podman, MobSF, mitmproxy, custom Python/Go tools | Containers do not replace a VM when analyzing hostile binaries. |

## Cross-platform foundations

- [Android SDK Platform Tools](https://developer.android.com/tools/releases/platform-tools)
- [Java](https://adoptium.net/) for many Android analysis tools
- [Python](https://www.python.org/) for scripting and automation
- [Git](https://git-scm.com/) for notes, scripts, and reproducibility
- [Docker](https://www.docker.com/) or [Podman](https://podman.io/) for isolated services

## Choosing a setup

- Choose **Linux** for a flexible analysis workstation and automation.
- Choose **Windows** when your target tools or games are Windows-specific.
- Choose **macOS** for a Unix-like development environment with Apple tooling.
- Choose a **VM or disposable device** when handling unknown or hostile files.

Do not install kernel modules, root frameworks, or unknown binaries on a primary personal device without understanding the risks.
