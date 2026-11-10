# Pliego app icon

**Figure:** Johannes Gutenberg. He introduced movable-type printing, the origin of page layout.

**Style:** a black-and-white portrait cut out over a full-bleed colour field, head and shoulders, in
the Nodalia icon family (one historical figure per app, one colour per app).

**Tile:** 512 × 512 viewBox, rounded square `rx=112`, clipped; no border or roundel.

**Provenance:** the portrait is "Portret van Johannes Gutenberg, RP-P-1914-4009.jpg" from
[Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Portret_van_Johannes_Gutenberg,_RP-P-1914-4009.jpg) (CC0). The figure was separated from its
background, converted to black and white and placed over the app colour.
Licence: see [LICENSE.txt](LICENSE.txt).

## Files

| File | Use |
|---|---|
| `designcraft.svg` | master: the portrait as a 1024 px image embedded in an SVG with the tile clip (canonical) |
| `designcraft-small.svg` | lighter 512 px version; also the scalable Linux icon and the web favicon where there is one |
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
