# Tempo website

Static coming soon page for `https://bashubb.com/tempo/`. Publish the `docs/` folder of a GitHub repository `bashubb/tempo` with GitHub Pages (Settings → Pages → main, /docs; leave Custom domain empty, the account's `bashubb.com` serves it under `/tempo/`).

```sh
python3 -m http.server 8778 --bind 127.0.0.1 --directory docs
```

App source: `../../creatorStudio/Tempo/`. Facts on the page (0.5× to 4×, iOS 17, iPhone only, Photos and Files import, no network) come from the code; re-check them when those change.

Shared landing system: `docs/assets/landing.css` and `landing.js` are identical across Wipe, Ringbox and Tempo; site colours live in `tempo.css`. The ramp scene maps scroll to the speed ramp in the inline script (`parts`).

Before submission: add `privacy/` and `support/` pages (App Store Connect needs both URLs), then switch `data-store="soon"` to `"live"` on `<html>` and replace the App Store search links (`data-store-link`) with the real app URL.

Sample clip: “Skaters Doing Tricks”, Coverr (Pexels 854036), CC0.
