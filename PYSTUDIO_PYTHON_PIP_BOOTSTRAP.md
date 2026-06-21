# PyStudio Python/Pip bootstrap

This repository uses `msmt2018/termux-generator` to build a PyStudio bootstrap
that already includes Python and pip.

- Package name: `com.vchangxiao.pystudio`
- Prefix: `/data/data/com.vchangxiao.pystudio/files/usr`
- Default architecture: `aarch64`
- Default additional packages: `python,python-pip`
- Build method: `termux-generator` F-Droid bootstrap patches

## Why this exists

Installing Python with `pkg install python` can fail inside PyStudio while the
package repository and prefix are still being stabilized. This build avoids that
runtime dependency by compiling a bootstrap that already contains Python, pip,
and their runtime dependencies.

## Expected artifacts

- `bootstrap-aarch64.tar.xz`
- `com.vchangxiao.pystudio-f-droid-python-pip-bootstrap-aarch64.tar.xz`
- `xz-aarch64/xz`
- `xz-aarch64/liblzma.so.5`
- `pystudio-python-pip-bootstrap-assets-aarch64.tar.gz`
- `SHA256SUMS.txt`

The `pystudio-python-pip-bootstrap-assets-*.tar.gz` archive preserves the asset
layout expected by the app-side local bootstrap installer.
