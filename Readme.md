# Field Scripts

A single-file showcase of hands-on, vanilla JavaScript — no framework, no build step, no dependencies to install. Open `index.html` in a browser (or serve it with GitHub Pages) and every script runs live, right in the page.

**[Live demo →](https://jamesmakau18.github.io/Js_lab/)**

## Why this exists

Most portfolios describe skills. This one runs them. Each entry is real, working JavaScript you can read top to bottom, press "Run" on, and watch execute in an inline console — the same code, not a screenshot of it.

## What's inside

| # | Script | Covers |
|---|--------|--------|
| 01 | Closures — counter factory & memoize | Closures, higher-order functions, caching |
| 02 | Debounce & throttle | Rate limiting, `setTimeout`, timing control |
| 03 | Custom EventEmitter | Pub/sub, class design, Node-style APIs |
| 04 | Retryable request wrapper | `async`/`await`, error handling, backoff |
| 05 | LRU cache on a Map | Data structures, `Map` insertion order |
| 06 | Express-style middleware pipeline | `next()` chaining, async control flow |
| 07 | Deep clone & deep equal | Recursion, `WeakMap`, object graphs |
| 08 | Reactive state via `Proxy` | Proxy traps, observer pattern, reactivity internals |

## Running it locally

No install required:

```bash
git clone https://github.com/jamesmakau18/Js_lab.git
cd Js_lab
open index.html   # or just double-click it
```

Everything runs client-side in the browser — there's nothing to `npm install`.

## Deploying to GitHub Pages

```bash
git add index.html Readme.md
git commit -m "update field scripts"
git push origin master
```

`master` and `main` are kept in sync in this repo, so either branch works for **Settings → Pages → Deploy from a branch**. Pages is already live at [jamesmakau18.github.io/Js_lab](https://jamesmakau18.github.io/Js_lab/) — pushing to `master` updates the live site within a minute or two.

## Adding your own script

Every entry lives in the `SCRIPTS` array near the top of the `<script>` block in `index.html`:

```js
{
  id: 'unique-id',
  tag: 'category-label',
  title: 'Short title',
  desc: 'One sentence on what it demonstrates.',
  code: `// your JS here — runs inside an async IIFE,
// so top-level await works`,
}
```

Add an object to the array and a new numbered card appears automatically, wired up to the same run button and console output.

## Tech

Plain HTML, CSS, and JavaScript. [highlight.js](https://highlightjs.org/) for syntax highlighting via CDN — the only external dependency, and it's optional (the page still works without it).

## License

MIT — use, fork, or adapt any of these scripts freely.