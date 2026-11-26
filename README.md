# Third-Party Canary Script Host (`tp-test-assets`)

Cross-origin script host for the [Agentic Web Canary Test Kit](https://github.com/samtout/geo-canary-kit).

## Purpose

Hosting `widget_v2.js` on a separate origin (`samtout.github.io`) from the main fixture page (`canary.geostellar.ai`) creates a genuine cross-origin boundary so external security scanners can be evaluated on **code-origin attribution**—especially Case B, where this third-party script appends a hidden span directly inside a first-party `<main><p>` element.

## Safety Statement

All strings in `widget_v2.js` are harmless, inert canary tokens (`CANARY-<RUN>-*`). No user data, cookies, credentials, storage tokens, or network requests are collected or transmitted.

## Usage

Pass `?run=XXXX` to generate unique canary tokens per test run:

~~~html
<script src="https://samtout.github.io/tp-test-assets/widget_v2.js?run=7F3A"></script>
~~~

See the full test matrix, installation guides, and scorecard in [samtout/geo-canary-kit](https://github.com/samtout/geo-canary-kit).