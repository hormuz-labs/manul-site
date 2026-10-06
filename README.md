# manul.si

The website for [Manul](https://github.com/hormuz-labs/manul), the agentic video editor. Astro, static, no framework JS: the only script is the hero demo (`src/components/Demo.astro`), a working miniature of Manul's editor.

The look is a cutting room: paper, ink, and one china-marker red for the notes (circles, arrows, strike-throughs). Type is Archivo (condensed for headlines) and IBM Plex Mono. The demo inside keeps the app's own dark shades and amber, so it looks like Manul really does.

```bash
npm install
npm run dev          # http://localhost:4321
npm run build        # → dist/
node test/demo.mjs   # clicks through the demo in Chrome, screenshots each stage to /tmp/manul-site-shots
node test/sizes.mjs  # checks 18 screen sizes, phone to 2560 wide, for anything spilling off screen
```

Deployed by Cloudflare Pages on every push to `main` (build `npm run build`, output `dist`).

The demo clips in `public/demo/` are real edits (ffmpeg) of "Manul Timofey" by the Moscow Zoo, [CC BY 4.0](https://commons.wikimedia.org/wiki/File:%D0%9C%D0%B0%D0%BD%D1%83%D0%BB_%D0%A2%D0%B8%D0%BC%D0%BE%D1%84%D0%B5%D0%B9_%D0%BD%D0%B0_%D1%80%D0%B0%D0%B7%D0%B6%D0%B8%D1%80%D0%BE%D0%B2%D0%BA%D0%B5.webm).
