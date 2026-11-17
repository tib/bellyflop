# Belly Flop — The Landing Game

A browser-based 3D landing challenge. Flip a returning launch vehicle upright, line it up with the tower arms, slow down, and save enough fuel to finish the landing burn.

**Play:** [bellyflop.lol](https://bellyflop.lol) · **Source:** [github.com/tib/bellyflop](https://github.com/tib/bellyflop)

## Objective

Guide the vehicle into the catch zone and meet all three landing limits at the moment of capture:

- Pad alignment: **90% or higher**
- Vertical alignment: **99% or higher**
- Touchdown speed: **below 20 km/h**

Keep some fuel for the final burn. A slow touch against an arm can gently nudge the vehicle toward the center before the catch point.

## Controls

| Action | Keyboard | Touch |
| --- | --- | --- |
| Move left / right | A / D or ← / → | Left / right buttons |
| Rotate the vehicle | Q / E | Rotation buttons |
| Increase / decrease thrust | W / S or ↑ / ↓ | Thrust buttons |
| Start or restart after a flight | Space | Start / Try Again |
| Restart | R | — |
| Open project information | I | Info button |

## Run locally

No build step or package installation is needed. Python 3 is used only to serve the files over HTTP, which is required for the browser to load the local 3D models.

```sh
./serve.sh
```

Then open <http://127.0.0.1:4173>.

## GitHub Pages

This is a static site. Publish the repository root from the `main` branch in **Settings → Pages → Deploy from a branch**. The empty `.nojekyll` file disables Jekyll processing, so the site files are served directly. The root `CNAME` file sets the custom domain name to `bellyflop.lol`; the domain's DNS records must also be pointed to GitHub Pages.

The site loads Three.js and web fonts from CDNs, so an internet connection is required. The bundled 3D models and share image are served from this repository.

## Models and licensing

The bundled 3D model files are built from geometry generated under MIT-licensed source code. License notices and asset details are in [ASSET-LICENSES.md](ASSET-LICENSES.md) and the `LICENSES/` directory. The game code does not currently include a top-level license.

This is an independent fan-made project and is not affiliated with, endorsed by, or sponsored by any aerospace company. Third-party names and marks remain the property of their respective owners.
