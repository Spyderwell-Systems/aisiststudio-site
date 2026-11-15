# Source refactor validation — 2026-11-15

Branch: `refactor/readable-source` (draft PR #3)

## Verified by GitHub source comparison
- The new `styles.css` is byte-for-byte equal to the original embedded CSS plus its trailing newline.
- The modified `index.html` is exactly the original HTML with its `<style>...</style>` block replaced by `<link rel="stylesheet" href="styles.css">`.
- All internal fragment links with named targets refer to IDs present in `index.html`.
- `styles.css` is referenced as a relative asset; serving it from the same directory as `index.html` is required.
- GitHub's combined commit status endpoint returned no statuses for the refactor commit; this is not a successful CI run.

## Still required before merge
- Open the Netlify deploy preview, confirm the stylesheet is served successfully (HTTP 200) and inspect the browser console.
- Compare desktop and mobile screenshots against the current production page.
- Check font loading, hover/focus styles, and navigation.
- Test with JavaScript disabled and with reduced motion enabled; the latter behavior is addressed separately in draft PR #2.
- Confirm Netlify production branch, publish directory, build command and preview settings from the actual Netlify dashboard.

No browser test, Lighthouse run, Netlify configuration inspection, merge or deployment was performed in this source-level validation.
