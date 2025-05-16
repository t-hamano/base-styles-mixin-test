This repository is intended to test whether the new @wordpress/base-styles package, which is based on dart-sass, can be compiled with the latest Sass.

You can test it in your Gutenberg project by following these steps:

The `perf-envs` directory is git-ignored, so we will use this directory to test.

```
# First, check out https://github.com/WordPress/gutenberg/pull/70135/
gh pr checkout 70135

# The `perf-env` directory is gitignore'd, so it is an appropriate directory for testing.
cd /path/to/gutenberg/perf-envs

# Clone this repo into the `perf-env` directory.
git clone https://github.com/t-hamano/base-styles-mixin-test.git

cd base-styles-mixin-test
npm install

# Verify that the latest Sass compiles base-styles correctly.
npm run build
npm run watch:js
npm run build:js
```
