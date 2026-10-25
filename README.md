# SAG Forms downloads

A desktop forms app for associations. This repository hosts installers and signed in-app updates.

[Download the latest release](https://github.com/me574/sag-releases/releases/latest)

If no release is listed yet, the first installers have not been published. You do not need a GitHub account to download a published release.

## Choose your download

Open the latest release and expand **Assets** if its files are hidden.

| Computer                                             | Download                                              |
| ---------------------------------------------------- | ----------------------------------------------------- |
| Mac with an Apple chip, such as M1, M2, M3, or later | Filename ending in `aarch64-apple-darwin.dmg`         |
| Mac with an Intel processor                          | Filename ending in `x86_64-apple-darwin.dmg`          |
| Windows PC with an Intel/AMD 64-bit processor        | Filename ending in `x86_64-pc-windows-msvc-setup.exe` |

On a Mac, **Apple menu → About This Mac** shows its chip or processor. On Windows, **Settings → System → About → System type** shows the processor architecture. The Windows build targets x64; a native Windows ARM build is not provided.

Use the `.dmg` or `-setup.exe` for a normal first installation. `.app.zip` is an alternative Mac download; `.msi` is an alternative Windows installer. Do not install both Windows installer formats. Files ending in `.app.tar.gz`, `.sig`, `SHA256SUMS.txt`, `update-*.json`, or `latest.json` support updates or download verification. GitHub's **Source code** archives are not installers.

## Install on macOS

1. Download the `.dmg` for your Mac.
2. Double-click it in **Downloads**.
3. Drag **SAG Forms.app** into **Applications**. Wait for copying to finish.
4. Eject the mounted installer from Finder. Open **Finder → Applications**.
5. Right-click **SAG Forms** (or hold Control while clicking) and choose **Open**. If a confirmation offers **Open**, select it.
6. If macOS blocks it with an unidentified-developer or cannot-verify warning, dismiss that dialog, then open **Apple menu → System Settings → Privacy & Security**.
7. Scroll to **Security**, find the notice about SAG Forms, and choose **Open Anyway**. Authenticate if asked, then confirm **Open**. On older macOS versions, look in **System Preferences → Security & Privacy → General**.
8. Later launches can use **Applications** or Spotlight.

Right-click → Open may not provide an exception on newer macOS versions; use the Settings path above after attempting to launch. Always run the installed copy, not the copy inside the mounted DMG, so updates can replace it.

If **Open Anyway** is missing, attempt to open the installed app again and revisit Settings. A managed Mac may require IT approval. If macOS reports malware or a damaged/modified app, stop and contact the maintainer; that is different from an unidentified-developer prompt.

The app is ad-hoc signed, without Apple notarization. See [Apple's guidance for opening downloaded apps](https://support.apple.com/en-us/102445).

## Install on Windows

1. Download the file ending in `x86_64-pc-windows-msvc-setup.exe` from this repository's release page.
2. Open **File Explorer → Downloads**, then double-click the installer.
3. If a **Windows protected your PC** SmartScreen panel appears, click **More info**.
4. Check the filename against the release asset you downloaded. **Unknown publisher** is expected because this app has no commercial Windows signing certificate. If you trust this download, choose **Run anyway**.
5. Follow the setup prompts, keep the default install location, and finish installation. The recommended EXE installs for your current user; routine installation should not require running the app as administrator.
6. If Microsoft **Edge WebView2 Runtime** is missing, setup downloads it. Stay connected until that finishes. This runtime renders the app's window.
7. Open **SAG Forms** from the Start menu, or use **Launch SAG Forms** if setup offers it.

The `.msi` is an alternative for people who need that installer format; it may request administrator approval. The plain `.exe` is not the recommended first-install download and requires WebView2 to be installed already.

If **Run anyway** is missing or your device says installation is blocked by policy, ask your IT administrator or the maintainer. Windows 11 **Smart App Control** can also block unsigned apps and may not offer this override. These steps apply to a SmartScreen reputation prompt; they do not override malware detection, Windows S mode, or organization policy. Leave antivirus and device-wide security protections enabled.

Microsoft documents the [More info → Run anyway flow](https://learn.microsoft.com/en-us/windows/apps/package-and-deploy/publish-first-app), [SmartScreen policy restrictions](https://learn.microsoft.com/en-us/windows/apps/package-and-deploy/smartscreen-reputation), and [Smart App Control](https://support.microsoft.com/en-us/windows/security/threat-malware-protection/smart-app-control-frequently-asked-questions).

## Updates after installation

The app checks on startup. You can also select **Check for updates**. Read the release notes, save any work, then choose **Update and restart**, or choose **Later** to postpone. Stay connected while the package downloads. The app verifies its cryptographic signature and version before installing it. Windows setup closes the app during installation; macOS restarts after installation.

Update signatures are separate from Apple/Windows publisher certificates. They verify the update package but do not guarantee that OS warnings will disappear on future versions. A failed automatic check does not prevent you from using the installed app.

## If installation still fails

Download a fresh copy from the release page and confirm the correct operating system and processor type. If a download appears damaged, compare its SHA-256 hash with the matching target's `SHA256SUMS.txt` file, or ask the maintainer for help. Report your OS version, the downloaded filename, and the exact warning text. Do not send passwords or private form data.
