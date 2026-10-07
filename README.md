# iPhone Duo SF Symbols

<p align="center"><img src="preview.svg" alt="The six iPhone Duo symbols: folded, half open, unfolded, locked, unlocked and waves" width="100%"></p>

Vector SVGs of the iPhone Duo symbols that ship with SF Symbols in macOS 27.2. Apple leaves these symbols unnamed. They appear only as UUIDs, so each file here has a descriptive name.

The repo has two kinds of file:

- **[`templates/`](templates):** full SF Symbols templates, with all 9 weights (Ultralight to Black) in all 3 scales (Small, Medium, Large). Use these in Xcode or the SF Symbols app.
- **The root SVGs:** one plain SVG per symbol, in Regular weight. Use these on the web or in design tools.

| Symbol | File | Source |
| --- | --- | --- |
| <img src="iphone-duo-folded.svg" height="32"> | `iphone-duo-folded.svg` | Apple, `BA5F95BD205B47E982C16A26E541251A` |
| <img src="iphone-duo-half-open.svg" height="32"> | `iphone-duo-half-open.svg` | **Custom, made by [@fedesanchez0](https://github.com/fedesanchez0)** (see below) |
| <img src="iphone-duo-unfolded.svg" height="32"> | `iphone-duo-unfolded.svg` | Apple, `123E64BDCACB4C389C204E2EC290D2A6` |
| <img src="iphone-duo-lock.svg" height="32"> | `iphone-duo-lock.svg` | Apple, `2F45143C03184F9D85936BB967922E8F` |
| <img src="iphone-duo-lock-open.svg" height="32"> | `iphone-duo-lock-open.svg` | Apple, `DB832091731249CDAB30C05B7DE8E354` |
| <img src="iphone-duo-waves.svg" height="32"> | `iphone-duo-waves.svg` | Apple, `C65B77A7ED044C57AF6B355700222834` |

### About the half-open symbol

Apple doesn't ship a half-open, folding version of the iPhone Duo symbol. I drew `iphone-duo-half-open.svg` myself, starting from Apple's folded glyph (`BA5F95BD…`), so it matches the other symbols in weight and style.

## SF Symbols templates

Each file in [`templates/`](templates) is a standard SF Symbols template, with 27 variants plus baseline, cap-height and margin guides. You can use one in two ways:

- **In Xcode:** drag the SVG into an asset catalog. It becomes a symbol image set you can load with `Image("iphone-duo-folded")` in SwiftUI or `UIImage(named:)` in UIKit. It follows Dynamic Type, font weight and `.imageScale` like a built-in symbol.
- **In the SF Symbols app:** choose File › Import Symbol… to add it to your custom symbols, where you can edit or re-export it.

The five Apple templates come straight from the glyphs in macOS 27.2, rendered at every weight and scale. Their size, margins and baseline match Apple's to within 0.001 pt. They keep Apple's layer structure for monochrome, hierarchical, palette and multicolor rendering. For example, on the lock symbols the padlock is the primary layer and the phone outline is the secondary layer.

There are two limitations:

- **No translucent screen fill.** In hierarchical mode, Apple's folded, unfolded and waves symbols tint the phone's screen. In monochrome, Apple hides that fill using an opacity setting that custom symbol templates can't express. Keeping the fill would turn the screen solid black in monochrome, so the templates leave it out. Every other part of each symbol is unchanged.
- **The half-open template has one weight.** The custom half-open symbol only exists in one weight. Its template reuses that drawing for all 9 weights and scales it for Small and Large, so it won't get thinner or bolder with the font weight.

## Usage on the web

Each root SVG is a single `<path>` filled with `currentColor`, so the symbol takes on the text color around it:

```html
<img src="iphone-duo-folded.svg" alt="iPhone Duo" height="24">
```

To recolor a symbol with CSS, paste the SVG inline and set `color` on the parent element. The symbols use SF Symbols' Regular weight at a large point size, and their `viewBox` crops tightly to the glyph.

## Disclaimer

**SF Symbols, the iPhone Duo symbols, and the related designs are the property of Apple Inc.** Apple, iPhone and SF Symbols are trademarks of Apple Inc., registered in the U.S. and other countries. This project is not affiliated with, endorsed by, or sponsored by Apple.

These files are shared unofficially, for reference, for design mockups, and for educational use. Apple's [SF Symbols license](https://developer.apple.com/sf-symbols/) covers them, and in general it allows the symbols only in mockups and in software that runs on Apple platforms. Check Apple's terms before you use them anywhere else. This repository grants no license for Apple's symbols.

The half-open symbol (`iphone-duo-half-open.svg`) is my own work. Because it's derived from Apple's folded glyph, Apple's terms still apply to it.

If you represent Apple and want anything taken down, please [open an issue](../../issues) and I'll remove it.
