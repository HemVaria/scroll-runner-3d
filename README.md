# scroll-runner-3d

A scroll-driven 3D runner built with [Three.js](https://threejs.org). Scroll down and she runs; scroll up and she runs in reverse. The camera turns around her as you go.

Single HTML file, no build step, no dependencies to install.

## Run locally

The model is loaded with `fetch`, so open it through a local server rather than as a file:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## Deploy

It's a static site, so any static host works. With Vercel:

```bash
npx vercel --prod
```

## How it works

- `runner_v2.glb` is a textured, rigged character with a running loop baked in.
- Scroll progress scrubs the animation (`AnimationMixer.setTime`), so the stride follows your scroll exactly.
- Scroll keyframes in `index.html` (`keys`) set the character's position, rotation and camera distance per section. Edit them to change the choreography.
- `STRIDES` controls how many run cycles fit into the whole page.

## Use the model

The model is free to use, including commercially, under CC BY 4.0. Just credit this repo:

> "Runner" 3D model by HemVaria — https://github.com/HemVaria/scroll-runner-3d — CC BY 4.0

## License

- Code: [MIT](LICENSE)
- 3D model (`runner_v2.glb`): [CC BY 4.0](LICENSE-MODEL)
