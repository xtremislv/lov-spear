# Lov-Spear source

Lov-Spear is ZestDrop and Rovyl with the changes in these two patches.

| Patch | Applies to |
| --- | --- |
| `zestdrop.patch` | [Maxaccurate/ZestDrop](https://github.com/Maxaccurate/ZestDrop) at commit `0561d01` (MIT) |
| `rovyl.patch` | [HenryCauan/rovyl](https://github.com/HenryCauan/rovyl) at commit `5c4a579` (GPL-3.0-or-later) |

```bash
git clone https://github.com/Maxaccurate/ZestDrop zestdrop && git -C zestdrop checkout 0561d01
git -C zestdrop apply ../zestdrop.patch
git clone https://github.com/HenryCauan/rovyl rovyl && git -C rovyl checkout 5c4a579
git -C rovyl apply ../rovyl.patch
```

Build on Windows with the .NET 10 SDK, Node 20+ and Python 3: build ZestDrop with `build.ps1`, build the launcher
with `npm ci && npm run build` and `electron-builder --win dir`, then place the launcher's `win-unpacked` folder in
the app folder as `launcher\` and rename `ZestDrop.exe` to `Lov-Spear.exe`.

The launcher (modified Rovyl) is licensed under the GNU GPL v3.0 or later. The file tools (modified ZestDrop) are
under the MIT licence.
