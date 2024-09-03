# Mildly Opinionated Default CSS

MOD CSS is a convenient (mildly opinionated!) set of defaults for CSS projects. It is not a complete CSS reset/normalise or framework, although some normalisation is applied (particularly for forms) and there is a section of commonly needed utility classes.

> [!NOTE]
> MOD CSS is intended as a starting point rather than an end result.

## Usage

- Download the latest release and unpack it to your project's CSS assets.
- It is intended that you **do not** modify the `modcss.css` file itself, but that you copy/paste the CSS variable definitions into your own site's custom style sheet and modify them there.
- It is also recommended that you link to the *minified* MOD CSS file (`modcss.min.css`) in your site.

The MOD CSS file must be added before any other styles that might override it.

```html
<head>
    <title>My Cool Site</title>
    <!-- ... more header tags ... -->
    <link href="/assets/styles/modcss.min.css" rel="stylesheet">
    <link href="/assets/styles/my-site-styles.css" rel="stylesheet">
</head>
```

## CSS Variable Definitions

The defaults are my own preferences, feel free to customise them for to your own preferences.

```css
:root {
    --mod-font-serif: Cambria, Times, "Times New Roman", serif;
    --mod-font-sans: Segoe, 'Segoe UI', 'Helvetica Neue', 'Arial Nova', Helvetica, Arial, sans-serif;
    --mod-font-mono: Consolas, monaco, 'Courier New', monospace;
    --mod-font-size: 16px;
    --mod-body-size: 1rem; /* default body text size */
    --mod-font-weight: 400;
    --mod-margins: 1rem 0;
    --mod-borders: 1px solid #a0a0a0;
    --mod-focus-outline: 2px dotted #202020;
    --mod-button: #d0d0d0;
    --mod-button-hover: #e0e0e0;
    --mod-button-active: #b0b0b0;
    --mod-text-dark: #000000;
    --mod-text-medium: #606060;
    --mod-text-light: #ffffff;
    --mod-bg-dark: #404040;
    --mod-bg-medium: #e3e3e3;
    --mod-bg-light: #ffffff;
    --mod-mark-bg: #ffff44;
    --mod-mark-text: #000000;
}
@media screen and (min-width: 900px) {
    :root {
        --mod-body-size: 1.125rem; /* wide-screen body text size */
    }
}
```

## Utility Classes

Currently there is only one utility class, but it is one I use in every project.

### `.vh, .visually-hidden`

> [!TIP]
> Use whichever class name you prefer: short version or descriptive version

This class *visually* hides content by moving it "off-screen" while leaving it in the flow of content (the DOM). It makes it invisible to sighted visitors, but still present for screen-readers (used by visually-impaired visitors) and web-crawlers.

## History

There was an earlier version (ver. 1.x) of this library called "LMD CSS", but when adding the Utility Classes section I decided to rename it to "Mildly Opinionated Default CSS" (MOD CSS) and start afresh from version 2.x.

I *nearly* went with the name "*Slightly* Opinionated Default CSS", but stopped myself in time.
