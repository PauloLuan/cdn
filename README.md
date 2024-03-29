# CDN for web fonts

Service for delivering font families to websites using CSS.

fontss font files through jsDelivr's global content delivery network

---

For the font Roboto, it's as easy as adding this to your CSS:

```css
@import url('https://cdn.jsdelivr.net/gh/pauloluan/cdn/fonts/roboto.css');
```

or this to your HTML's `<head>`:

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/pauloluan/cdn/fonts/roboto.css">
```

## Instructions for add new fonts

Font stylesheets are stored in `/fonts`, and font files are stored in `/fonts/src`.

Adding a font:

1. Upload all weights to https://transfonter.org/. The format you upload them in doesn't matter
2. Use these settings: ![transfonter settings](https://i.imgur.com/8eefUiF.png)
3. Press "Convert" and download the archive
4. Clone the GitHub repository to your device: `git clone https://github.com/pauloluan/cdn.git`
5. Open the archive downloaded from transfonter
6. Create a new folder in `/fonts/fonts/src` for the name of the font. Only lowercase letters/numbers and dashes, please! I'll use `font-name` in this example.
7. Move the `.woff` and `.woff2` files to `/fonts/fonts/src/font-name`
8. Move the `.css` file to `/fonts/fonts` and rename to `font-name.css`
9. Open the `.css` file. Do a find-and-replace for all instances of `url('`, and replace it with `url('src/font-name/`. Use the same font name as above.
