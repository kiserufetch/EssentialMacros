# Essential Macros

Windows desktop app for **Rust**: weapon-specific recoil presets, per-weapon key binds, and mouse movement along embedded offset patterns while the **left mouse button** is held. Sensitivity, FOV, crosshair, inventory, and overlay options are stored in the Windows **registry** under `HKCU\Software\EssentialM`.

## Features

- **Binds** — assign a key to each weapon; press it to toggle the active preset (highlight in the UI).
- **Recoil scripts** — `.esse` resources define `MoveR` / `Delay` steps; applied globally via a low-level mouse hook when LMB is down and a weapon is selected.
- **Settings** — sensitivity and FOV scale the applied movement; additional toggles (crosshair, inventory fix, overlay) integrate with game-style workflows.

**Supported weapon slots in the UI:** AK47, Berdanka, Beretta, LR300, M249, MP5A4, Pistol, Python, Revolver, SMG, Thompson, M39 (M39 currently reuses AK47 offsets in code).

## Requirements

- Windows  
- [.NET Framework 4.7.2](https://dotnet.microsoft.com/download/dotnet-framework/net472)  
- Visual Studio (or MSBuild) with NuGet restore

## Build

1. Open `EssentialMacros.csproj` in Visual Studio (or build from a Developer Command Prompt).  
2. Restore NuGet packages.  
3. Build configuration **Release**.  
4. Output: `bin\Release\EssentialMacros.exe` (Costura.Fody bundles dependencies into the executable where configured).

## Tech stack

- WPF + Material Design themes  
- [MouseKeyHook](https://github.com/gmamaladze/globalmousekeyhook) for global input  
- Windows Registry for persistence  

## Disclaimer

Using third-party input automation or macros in online games may **violate Facepunch Studios rules**, **Easy Anti-Cheat (EAC)** policy, or both, and can result in **account sanctions**. This software is provided **as-is**; you assume **all risk**.

## License

If no `LICENSE` file is present in the repository, rights and usage terms are unspecified—treat as **all rights reserved** unless the author adds a license.
