# A-Novel UI assets

Brand logos for A-Novel interfaces and documentation.

[![X (formerly Twitter) Follow](https://img.shields.io/twitter/follow/agorastoryverse)](https://twitter.com/agorastoryverse)
[![Discord](https://img.shields.io/discord/1315240114691248138?logo=discord)](https://discord.gg/rp4Qr8cA)

<hr />

![GitHub repo file or directory count](https://img.shields.io/github/directory-file-count/a-novel-kit/ui-assets)
![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/a-novel-kit/ui-assets)
[![GitHub Actions Workflow Status](https://img.shields.io/github/actions/workflow/status/a-novel-kit/ui-assets/main.yaml)](https://github.com/a-novel-kit/ui-assets/actions/workflows/main.yaml)

## What this is

The A-Novel UI assets are the files an interface displays as they are. Each logo ships as responsive
banners and square application icons, in dark and light modes. A generator renders them from reviewed
source artwork, which Git LFS stores.

The assets release on their own schedule. The [A-Novel UI](https://github.com/a-novel-kit/uikit)
components and foundations ship from their own repository.

## Installation

The packages are published to GitHub Packages, which needs a `read:packages` token even to read. The
[developer guide](https://a-novel-kit.github.io/stack/dependencies/node#configure) sets one up. Point
the `@a-novel-kit` scope at that registry in the application's `.npmrc`:

```ini
@a-novel-kit:registry=https://npm.pkg.github.com
```

Install the images, then import a file by its path. Bundlers such as Vite resolve it to a public URL:

```bash
pnpm add @a-novel-kit/ui-images
```

```ts
import bannerUrl from "@a-novel-kit/ui-images/files/banner/160h/agora-banner.png";
```

A Markdown page links the same file on `master` instead:

```text
https://raw.githubusercontent.com/a-novel-kit/ui-assets/master/packages/images/files/banner/960h/agora-banner.png
```

## Packages

| Package                                       | What it is for                                                       |
| --------------------------------------------- | -------------------------------------------------------------------- |
| [`@a-novel-kit/ui-images`](./packages/images) | The brand logos, as responsive banners and square application icons. |

## Contributing

Start with the [developer guide](https://a-novel-kit.github.io/stack/), then read the
[contribution guide](./CONTRIBUTING.md).
