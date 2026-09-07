# Occlude

**[Live site →](https://darrenrosbon.github.io/occlude/)**

A concept site for a fictional zero-knowledge "dark pool" — a protocol that routes crypto trades through a shielded pool so the amount, counterparty, and wallet link are never disclosed on-chain, while the fact that a trade happened stays public.

This is a portfolio/demo project. **Occlude is not a real product.** There is no protocol, no smart contract, and no shielded pool behind it — every number, transaction, and queue position on the site is illustrative. The technical claims are grounded in how real zero-knowledge privacy systems actually work (zk-SNARKs, Zcash's shielded pool, Penumbra's private trading venue), but nothing here should be mistaken for a working product or investment opportunity.

## What it's demonstrating

- A raymarched WebGL "shield" hero visual (custom GLSL, no external shader libraries) with orbiting fragments and an ambient particle field, replacing what was originally a static photo
- A generalized horizontal/vertical particle-flow diagram (single shader, one `uOrientation` uniform) for the Shield → Prove → Settle pipeline
- A real-time collision-driven redaction scan (the scan line's position drives which fields redact, not a timed animation)
- A boot sequence, custom cursor, scroll-gated section reveals, and a handful of terminal-styled micro-interactions, all respecting `prefers-reduced-motion`
- Single static `index.html`, no build step, no framework — deployed directly to GitHub Pages

## Stack

Vanilla HTML/CSS/JS, [Three.js](https://threejs.org/) (r128, via CDN) for the WebGL shader work. No bundler, no framework, no dependencies beyond the CDN script tag and Google Fonts.

## Running locally

It's a single file — clone the repo and open `index.html`, or serve the directory with anything static:

```bash
python3 -m http.server 8080
```

## Structure

```
index.html    everything: markup, styles, and scripts inline
og-image.png  static link-preview image (OG/Twitter card)
```
