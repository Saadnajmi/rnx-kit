---
"@rnx-kit/metro-serializer-esbuild": minor
---

feat(metro-serializer-esbuild): expose `treeShaking` option

Forwards the `treeShaking` flag to esbuild's `build()` options. Lets callers
use the esbuild bundling path (and its metafile emission) without applying
tree-shaking — useful for platform bundles where the goal is metafile-based
size analysis on an unmodified bundle, not actually shaking unused code out.

Default behavior is unchanged: when omitted, esbuild applies its own default
(`true` when `bundle: true`).
