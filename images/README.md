# Brand assets

Put brand files here:

- **`logo.svg`** (or `logo.png`) — your "BLUE WAVE / CONSTRUCTION" wordmark.
  To use it, replace the `<span class="logo-slot">…</span>` placeholder in the
  header of `index.html` with:

  ```html
  <img src="images/logo.svg" alt="Blue Wave Construction" height="40" />
  ```

- **`estimate.pdf`** — your estimate template. Drop it in the repo so the site's
  colors and type can be tuned to match. The brand colors live at the top of the
  `<style>` block in `index.html` under `:root` (`--navy`, `--wave`, etc.) —
  adjust those hex values to match the PDF exactly.

- **`projects/`** — completed-project photos for the Recent Work gallery
  (see `projects/README.md`).
