# Contributing to A-Novel UI assets

This guide covers what is specific to the UI assets. Set up the shared toolchain with the
[developer guide](https://a-novel-kit.github.io/stack/), and read the [README](./README.md) first for
the package map. The
[libraries, tooling, and platform concepts](https://github.com/a-novel-kit/.github/blob/master/CONTRIBUTING.md)
hold what is true of every library.

## What belongs here

An asset belongs here when an interface or a document displays it as it is, and it changes far less
often than the components. Components, design tokens, and fonts belong to
[A-Novel UI](https://github.com/a-novel-kit/uikit).

`packages/images` owns the brand logos and their source artwork.

## Source artwork

Git LFS stores the source artwork under `packages/images/raw`. Install Git LFS before you commit
there: without it, Git stores the file as an ordinary blob. GitHub keeps every LFS version pushed to
it, so squash your iterations into one commit before you push.

The published files are generated from those sources. Change the source, never a published file, and
regenerate as the [images README](./packages/images/README.md#reproducing-the-images) shows. `pnpm lint`
fails when a published file drifts from its source.

A published path is a consumer contract. Applications import it, and the organization READMEs link it
on `master`. Renaming or removing a file breaks them, so it ships as a breaking change, with those
READMEs updated alongside.

## Before handing off

Format the repository and run every gate CI runs:

```bash
pnpm format
pnpm lint
pnpm build:ci
```

## Questions?

[Open an issue](https://github.com/a-novel-kit/ui-assets/issues) with the asset involved and what you
expected.
