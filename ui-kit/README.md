# Standalone UI Kit

Serve this directory with a static HTTP server and open `index.html`. The UI Kit's HTML, CSS, JavaScript, images, and SVG preview assets are contained here. Google Fonts and Adobe Typekit are loaded from their existing external services; portfolio example links point to the public portfolio.

## Inherited missing asset

`css/components.css` contains two mask references to `assets/icons/quote.svg` in the `.pattern-callout__icon` rule. That relative path resolves from the CSS file to `css/assets/icons/quote.svg`. No such file exists in the source `portfolio-clean` repository, and the UI Kit page does not render `.pattern-callout__icon`. The rule was copied without changing its selector or behavior. If the callout is added to the UI Kit later, supply the intended source SVG and verify its mask path before relying on the icon.
