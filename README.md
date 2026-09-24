# iPhone Duo SF Symbols

<p align="center"><img src="preview.svg" alt="The six iPhone Duo symbols: folded, half open, unfolded, locked, unlocked and waves" width="100%"></p>

Vector SVGs of the iPhone Duo symbols that ship with SF Symbols in macOS 27.2. Apple leaves these symbols unnamed. They appear only as UUIDs, so each file here has a descriptive name.

| Symbol | File | Source |
| --- | --- | --- |
| <img src="iphone-duo-folded.svg" height="32"> | `iphone-duo-folded.svg` | Apple, `BA5F95BD205B47E982C16A26E541251A` |
| <img src="iphone-duo-half-open.svg" height="32"> | `iphone-duo-half-open.svg` | **Custom, made by [@fedebitrig](https://github.com/fedebitrig)** (see below) |
| <img src="iphone-duo-unfolded.svg" height="32"> | `iphone-duo-unfolded.svg` | Apple, `123E64BDCACB4C389C204E2EC290D2A6` |
| <img src="iphone-duo-lock.svg" height="32"> | `iphone-duo-lock.svg` | Apple, `2F45143C03184F9D85936BB967922E8F` |
| <img src="iphone-duo-lock-open.svg" height="32"> | `iphone-duo-lock-open.svg` | Apple, `DB832091731249CDAB30C05B7DE8E354` |
| <img src="iphone-duo-waves.svg" height="32"> | `iphone-duo-waves.svg` | Apple, `C65B77A7ED044C57AF6B355700222834` |

### About the half-open symbol

Apple doesn't ship a half-open, folding version of the iPhone Duo symbol. I drew `iphone-duo-half-open.svg` myself, starting from Apple's folded glyph (`BA5F95BD…`), so it matches the other symbols in weight and style.

## Usage

Each file is a single `<path>` filled with `currentColor`, so the symbol takes on the text color around it:

```html
<img src="iphone-duo-folded.svg" alt="iPhone Duo" height="24">
```

To recolor a symbol with CSS, paste the SVG inline and set `color` on the parent element. The symbols use SF Symbols' Regular weight at a large point size, and their `viewBox` crops tightly to the glyph.

## Disclaimer

**SF Symbols, the iPhone Duo symbols, and the related designs are the property of Apple Inc.** Apple, iPhone and SF Symbols are trademarks of Apple Inc., registered in the U.S. and other countries. This project is not affiliated with, endorsed by, or sponsored by Apple.

These files are shared unofficially, for reference, for design mockups, and for educational use. Apple's [SF Symbols license](https://developer.apple.com/sf-symbols/) covers them, and in general it allows the symbols only in mockups and in software that runs on Apple platforms. Check Apple's terms before you use them anywhere else. This repository grants no license for Apple's symbols.

The half-open symbol (`iphone-duo-half-open.svg`) is my own work. Because it's derived from Apple's folded glyph, Apple's terms still apply to it.

If you represent Apple and want anything taken down, please [open an issue](../../issues) and I'll remove it.
