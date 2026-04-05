<img width="250" height="250" alt="Collage" src="https://github.com/user-attachments/assets/e88741c7-f175-4f62-b9d1-bb8577091893" />

# WinUI Blank App (Unpackaged) - Visual Studio Template

A custom Visual Studio project template for creating **unpackaged WinUI 3 desktop applications** with a ready-to-run `.exe` file.

Perfect for developers who want to build modern WinUI 3 apps without MSIX packaging, deployment complexity, or the Windows App SDK packaging toolchain.

---

## Features

- **Unpackaged** WinUI 3 application (no MSIX)
- Directly produces a runnable `.exe` file
- Easy debugging with "EXE" launch profile
- Configured for **x64** platform only (can be extended)
- Uses latest **Windows App SDK 1.8** and **.NET 8/10**
- Includes all necessary assets and manifest files
- Ready for single-file publishing (if you enable it later)

> **Note**: Publishing via FolderProfile currently has limitations (as mentioned in the template description).

---

## Installation

### Option 1: Manual Installation (Recommended)

1. Download the latest release or clone this repository.
2. Extract the contents.
3. Copy the folder `WinUI Blank App (Unpackaged)` to your Visual Studio templates location:

   **Common paths:**
   - `%USERPROFILE%\Documents\Visual Studio 18\Templates\ProjectTemplates\C#\`
   - Or for Visual Studio 2022 (preview): `%USERPROFILE%\Documents\Visual Studio 2022\Preview\Templates\ProjectTemplates\`

4. Restart Visual Studio.

### Option 2: .vstemplate Import

You can also import the `.vstemplate` file directly via Visual Studio's "Export Template" / "Manage Project Templates" feature.

---

## How to Use

1. Open Visual Studio
2. Go to **File > New > Project**
3. Search for **"WinUI Blank App (Unpackaged)"**
4. Create the project
5. Press **F5** to run — it should launch the app directly as a normal desktop `.exe`

---

## Project Structure

- `App.xaml` / `App.xaml.cs` — Application entry point
- `MainWindow.xaml` / `MainWindow.xaml.cs` — Main window
- `app.manifest` — Application manifest with PerMonitorV2 DPI awareness
- `Package.appxmanifest` — Kept for reference (not used in unpackaged mode)
- Assets folder with default logos and splash screen

---

## Important Notes

- This template sets `<WindowsPackageType>None</WindowsPackageType>` to disable packaging.
- Publishing is currently **not fully functional** with the included FolderProfile.
- Designed primarily for **development and direct .exe execution**.
- Self-contained, single-file, and trimmed publishing can be enabled manually in the `.csproj` file.

---

## Requirements

- Visual Studio 2022 (17.8 or newer recommended)
- .NET 8.0/10.0 SDK
- Windows 10 17763 or higher (Windows 11 recommended)
- Windows App SDK workload installed

---

## Contributing

Contributions, issues, and feature requests are welcome!

Feel free to fork the project and submit a pull request.

---

## License

This project is licensed under the [MIT License](LICENSE).

---

**Made with ❤️ for the WinUI community**
