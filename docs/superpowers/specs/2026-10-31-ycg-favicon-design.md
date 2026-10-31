# YCG Favicon

- **Intent:** Replace the browser's default globe icon with the portfolio's YCG initials.
- **Goal:** Show a recognizable YCG favicon in browser tabs.
- **Non-goals:** Do not change the navbar logo, page title, or other site visuals.
- **Constraints:** Keep the existing static HTML site; use the current brand treatment (dark `YC`, orange `G`) and support crisp rendering at favicon sizes.
- **Approaches:** A standalone SVG favicon is small, scalable, and easy to maintain; a PNG requires preparing bitmap artwork and sizes. **Selected:** standalone SVG, as requested.
- **Implementation choice:** Add `assets/favicon.svg` and reference it from the document head using a favicon `<link>`.
