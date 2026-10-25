# dubai-mainline-kernel

The kernel for [dubai-mainline](https://github.com/tuxdotrs/dubai-mainline)
(Motorola Edge 30, SM7325): [sc7280-mainline/linux](https://github.com/sc7280-mainline/linux)
built with nixpkgs `linuxManualConfig`, clang/lld, cross-compiled from x86_64.

    linux/        submodule: sc7280-mainline/linux, tag v7.3.0-sc7280 (no fork)
    config        pmOS' linux-postmarketos-qcom-sc7280 config + our additions
    patches/      applied on top (kernelPatches in default.nix)
    default.nix   the package; called by the userspace repo's device module
    prebuilt/     fallback: pmOS' binary kernel package (motorola-dubai.kernel = "prebuilt")
    toolchain/    parked: pmOS' exact clang 23 toolchain

Build from the meta repo: `./build.sh kernel`. Bumping, config notes and the
patch rationale: dubai-mainline `docs/kernel.md`.
