# Installation

## Required source

Use a clean **Bomberman Land 2 (Japan)** GameCube ISO, game ID **GB2J18**, disc 0, revision 0.

- Size: **1,459,978,240 bytes**
- SHA-256: `50f421edd3b2f9d47ce2732ddc2bec4597ab648fb0016bee0d694861c73f9cf8`

An RVZ must first be converted to a full ISO. The converted file must match this checksum. Other revisions, scrubbed images and already patched ISOs are not supported inputs. Always apply each release to the clean original.

## Windows x64

1. Download and extract the release ZIP into a folder.
2. Double-click **Install.cmd**.
3. Select your clean Japanese ISO, then choose a new output filename.
4. Wait for patching and checksum verification to finish. Keep the original ISO unchanged.
5. Fully stop your emulator and boot the new ISO. Load a normal memory-card save rather than an older emulator save state.

The installer runs PowerShell with an execution-policy override for that process only; it does not change your system policy. A portable xdelta3 patcher is included; no installation or download is needed.

## Other systems / manual patching

Use xdelta3 or [Delta Patcher](https://github.com/marco-calautti/DeltaPatcher) with the original ISO and the supplied `.xdelta` file. With xdelta3:

```text
xdelta3 -d -s "original.iso" "Bomberman-Land-2-English-v0.1.0-beta.1.xdelta" "Bomberman Land 2 English.iso"
```

Verify the result before playing:

- Size: **1,459,978,240 bytes**
- SHA-256: `b6cf727d54d26452f1a3b53cd7362b49123ec755f72da51a6b16bbec00b4991f`

On Windows, run `Get-FileHash -Algorithm SHA256 "your-file.iso"` in PowerShell.

## Real hardware

The output retains the original full disc-image size. Use your existing compatible homebrew/backup-loading setup. This patch does not provide a console loader or bypass a stock console's disc restrictions. Actual console boot and full-game compatibility have not yet been verified. Please report the console, loader and loader version with hardware results.

If source verification fails, do not force the patch. Check the source size and checksum. If patching fails, do not use the partial output; preserve the clean original and report the error.
