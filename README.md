# Three.js VR Starter

A minimal Three.js scene with a spinning cube and a WebXR VR button, ready for Meta Quest.

## Quick start

1. Clone or download this repo.
2. Serve it over HTTPS (required for WebXR). Easiest: enable **GitHub Pages** in the repo settings (Settings → Pages → Source: main branch, root). Your page will be at `https://3dhermit.github.io/threejs-vr-starter/`.
3. On your Quest, open the Quest Browser and visit that URL.
4. Tap **ENTER VR**.

No install, no build step. Three.js loads from a CDN via import maps.

## What it does

- Rotating, color-cycling cube on a ground plane with fog
- `OrbitControls` for desktop preview
- `VRButton` from Three.js addons for immersive sessions
- `renderer.xr.enabled = true` — the one line that turns on WebXR
- Status text showing desktop vs. VR mode

## Next steps

- Add a controller: `renderer.xr.getController(0)` with a line geometry for a ray
- Try a grab interaction with `XRHandModelFactory`
- Swap the cube for a Gaussian splat (see the splat-equirect bot for 360 output)
- Move the camera with `renderer.xr.getCamera()` inside the animation loop

## Notes

- Quest Browser is Chromium-based but lags desktop Chrome — test on-device early
- WebXR needs HTTPS; `localhost` works on desktop for dev
- OpenXR is the underlying standard; WebXR is the browser's implementation of it
