photoshopscripts
================

Assorted Photoshop scripts... made by me.

Both scripts here are extended versions of Adobe's "Layer Comps To Files" sample script. They export every layer comp in the open document to its own file, with extra options described below.

## The scripts

### Layer Comps To Artboard Files

Exports every layer comp once per artboard. For a document with 3 comps and 2 artboards you get 6 files.

Each file is named `<prefix>_<index>_<comp name>[_<comp comment>]-<artboard name>`, for example `homepage_0000_Dark-Mobile.png`. The prefix defaults to the document name and the index starts at `0000`.

The document needs at least one artboard. Transparent PNG export is supported (thanks [@TrevOwnz](https://github.com/antoniocosta/photoshopscripts/issues/1)).

### Layer Comps To Files (Extended)

Exports every layer comp to its own file, like Photoshop's own "Layer Comps to Files", with these extra options:

- **File Name Comp Index:** Untick it to leave the `_0000` index out of file names. Comp names then have to be unique, or files overwrite each other.
- **Trim Transparency:** Removes transparent padding before saving.
- **Canvas Resize By "@[size]":** A comp named `icon@64` has its canvas resized (cropped or padded) to 64 × 64 px.
- **Image Resize By "@[size]":** A comp named `icon@64` is scaled to 64 × 64 px.

Sizes are square and in pixels. The `@` becomes `_` in the file name (`icon@64` saves as `..._icon_64.png`). Comps without an `@[size]` are saved at their normal size.

### File formats

Both scripts save as BMP, JPEG, PDF, PSD, Targa, TIFF, PNG-8 or PNG-24. Settings are remembered between runs, and both scripts can be recorded in an action.

## Install

1. Download the `.jsx` file you want.
2. Copy it into Photoshop's `Presets/Scripts` folder:
   - macOS: `/Applications/Adobe Photoshop <version>/Presets/Scripts`
   - Windows: `C:\Program Files\Adobe\Adobe Photoshop <version>\Presets\Scripts`
3. Restart Photoshop. The script appears under **File › Scripts**.

To try a script without installing it, use **File › Scripts › Browse...** and pick the `.jsx` file.

## Compatibility

These are ExtendScript scripts, first written for Photoshop CC 2015. Current Photoshop versions still run ExtendScript, but Adobe is moving scripting to UXP, so a future version may drop it. If something breaks in your version, please [open an issue](https://github.com/antoniocosta/photoshopscripts/issues).

Recent Photoshop versions also come with **File › Export › Layer Comps to Files** and **File › Export › Artboards to Files**. Try those first if you don't need the extra options here.

## Credits

Based on Adobe's "Layer Comps To Files" sample script (Copyright 2007 Adobe Systems), written by Naoki Hada, Tom Ruark and Jeffrey Tranberry. Artboard support by Antonio Costa.

## Support

If you like ❤️ this or find it useful 🌟, support the project by buying me a coffee ☕.

<a href="https://www.buymeacoffee.com/antoniocosta" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" style="height: 40px !important;width: 140px !important;" ></a>
