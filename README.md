# fontloader

[![GitHub Workflow Status](https://img.shields.io/github/workflow/status/songww/fontloader/CI?style=for-the-badge)](https://github.com/songww/fontloader/actions/workflows/CI)
[![Crates.io](https://img.shields.io/crates/v/fontloader?style=for-the-badge)](https://crates.io/crates/fontloader)
[![docs.rs](https://img.shields.io/docsrs/fontloader?style=for-the-badge)](https://docs.rs/fontloader)

fontloader is a cross-platform Rust library for load fonts, using native font engines whenever possible.

### Supported Backends

| Platform | Backends    |
|----------|-------------|
| Linux    | fontconfig  |
| BSD      | fontconfig  |
| Windows  | DirectWrite |
| macOS    | Core Text   |

### Known Issues

Since fontloader was originally made solely for rendering monospace fonts in
[Alacritty](https://github.com/alacritty/alacritty), there currently is only
very limited support for proportional fonts.

Loading a lot of different fonts might also lead to resource leakage since they
are not explicitly dropped from the cache.
