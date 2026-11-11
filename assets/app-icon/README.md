# Pliego app icon

**Figure:** Johannes Gutenberg. He introduced movable-type printing, the origin of page layout.

**Style:** a black-and-white portrait cut out over a full-bleed colour field, head and shoulders, in
the Nodalia icon family (one historical figure per app, one colour per app).

**Tile:** 512 × 512 viewBox, rounded square `rx=112`, clipped; no border or roundel.

**Provenance:** the portrait is "Portret van Johannes Gutenberg, RP-P-1914-4009.jpg" from
[Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Portret_van_Johannes_Gutenberg,_RP-P-1914-4009.jpg) (CC0). The figure was separated from its
background, converted to black and white and placed over the app colour.
Licence: see [LICENSE.txt](LICENSE.txt).

**Linux:** the hicolor icons (`hicolor/scalable` and every PNG size) put the tile on the Nodalix
app grid, like the Colloid icons around it: a 224 px tile inside a 256 px canvas (16 px margin),
a 51.5 px corner radius and a soft shadow. The scalable SVG is made by `tools/nodalia-app-icon.py`
in [nodalix-icon-theme](https://github.com/danielmigueltejedor/nodalix-icon-theme) and
`packaging/icons.sh` renders the PNG sizes from it. macOS icons use Apple's
own grid, with a transparent margin, and the Windows `.ico` and the 1024 px render keep the
full-bleed tile. The window and taskbar icon on Windows is the 256 px
hicolor PNG, so it has the Linux margin and shadow.

## Files

| File | Use |
|---|---|
| `designcraft.svg` | master: the portrait as a 1024 px image embedded in an SVG with the tile clip (canonical) |
| `designcraft-small.svg` | lighter 512 px version; also the web favicon where there is one |
| `designcraft-1024.png` | 1024 px render of the full tile |
| `designcraft-macos-512.png` | Runtime Dock icon on macOS (embedded by `apps/designcraft`) |
| `designcraft.icns` | macOS bundle icon (`CFBundleIconFile`) |
| `designcraft.ico` | Windows exe icon, 16–256 px (embedded by `apps/designcraft/build.rs`) |
| `hicolor/<size>/apps/ai.storyteller.designcraft.png` | Linux icon theme, 16–512 px; the 256 px one is also the runtime window icon on Windows and Linux |
| `hicolor/scalable/apps/ai.storyteller.designcraft.svg` | Linux scalable icon |
| `LICENSE.txt` | MIT OR Apache-2.0 |

The app ID is `ai.storyteller.designcraft`. It's used for the hicolor icon names, the Wayland app ID and
`packaging/linux/ai.storyteller.designcraft.desktop`.

## Regenerate

The icon is a raster portrait, so the SVG files embed an image instead of traced paths. The
derived files in this directory were rendered directly from the portrait. `packaging/icons.sh`
still works on `designcraft.svg` (resvg renders embedded images), but its output will differ slightly
from the committed files in resampling.
