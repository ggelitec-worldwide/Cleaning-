# ADJ Maintenance Services

Website for ADJ Maintenance Services: office and commercial cleaning, plus appliance installation (microwaves, refrigerators, dishwashers, ranges, washers and dryers).

Call or text: **(561) 727-7860**

## What's in it

- **3D cleaning intro.** The site opens on a dirty office floor. Pressing the red **Clean** button vacuums the trash into the button, squeegees the floor, then sprays and squeegees a dirty mirror to reveal the ADJ logo. The button then turns into the logo and zooms into the site.
- **Scroll showcase.** Each service has a 3D scene that zooms in as you scroll, holds, then grows and fades as the next one arrives. The office scene cleans itself as you scroll.
- **Always-on calling.** The phone number is clickable in the top bar, and a red floating **Call Now** button stays on screen (a full-width bar on phones).

## Files

```
index.html          the whole site (HTML, CSS and JavaScript in one file)
images/logo.webp    full ADJ logo
images/emblem.webp  ADJ emblem (also used as the browser tab icon)
```

The 3D scenes use three.js r128, loaded from cdnjs. Fonts come from Google Fonts. Nothing needs to be installed or built.

## Run it locally

Opening `index.html` directly mostly works, but the logo on the mirror needs a local web server:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## Put it online with GitHub Pages

1. Create a new repository on GitHub and upload these files (keep the `images` folder).
2. In the repository, go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, pick `main` and `/ (root)`, then **Save**.
4. After a minute the site is live at `https://YOUR-USERNAME.github.io/REPO-NAME/`.

To use your own domain, add it under **Settings → Pages → Custom domain** and point your domain's DNS at GitHub Pages.

## Editing

- **Phone number:** search `index.html` for `5617277860` and `(561) 727-7860` and replace every match.
- **Services text:** the service cards are in the `#services` section, and the scroll showcase text is in the `#showcase` section.
- **Colors:** the main colors are defined at the top of the `<style>` block (`--red`, `--ink`, and so on).
