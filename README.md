# yocto-quickstart

![Yocto Project](https://img.shields.io/badge/Yocto-Project-blue) ![Embedded Linux](https://img.shields.io/badge/Embedded-Linux-green)

A practical, beginner-friendly guide to building a custom embedded Linux image with the Yocto Project. Covers everything from host setup to a bootable image running in QEMU or on real hardware.

## What's inside

- Host machine prerequisites and package installation
- Cloning Poky and selecting a release branch
- Build environment setup and `local.conf` configuration
- First build with `bitbake core-image-minimal`
- Running the image in QEMU
- Overview of layers, recipes, and the BitBake task model
- Common pitfalls and how to avoid them

## Requirements

- Linux host (Ubuntu 22.04 LTS or Debian 12 recommended)
- 50+ GB free disk space
- 8+ GB RAM
- Git, Python 3, and build essentials (see `docs/host-setup.md`)

## Quick start

```bash
git clone git://git.yoctoproject.org/poky
cd poky
git checkout scarthgap
source oe-init-build-env
bitbake core-image-minimal
```

Full walkthrough: `docs/getting-started.md`

## Tested images

| Image | Description | Approx. size |
|---|---|---|
| `core-image-minimal` | Shell only | ~10 MB |
| `core-image-base` | Minimal + networking | ~20 MB |
| `core-image-full-cmdline` | CLI tools | ~60 MB |

## Tested machines

- `qemux86-64` — QEMU x86-64 (default)
- `raspberrypi4` — Raspberry Pi 4 (via `meta-raspberrypi`)

## Repository structure

```
yocto-quickstart/
├── docs/
│   ├── getting-started.md
│   ├── host-setup.md
│   ├── layers.md
│   └── troubleshooting.md
├── conf/
│   └── local.conf.example
└── README.md
```

## License

MIT
