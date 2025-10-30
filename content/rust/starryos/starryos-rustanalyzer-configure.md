+++
title = "StarryOS：Rust-Analyzer配置"
date = 2025-10-30
[taxonomies]
categories = ["rust"]
tags = ["starryos", "rust-analyzer"]
+++

`vscode|cursor` 工作区设置：
```json
{
  "rust-analyzer.cargo.target": "aarch64-unknown-none-softfloat",
  "rust-analyzer.cargo.allTargets": false,
  "rust-analyzer.cargo.features": [
    "qemu",
    "pci"
  ],
  "rust-analyzer.numThreads": null,
  "rust-analyzer.server.extraEnv": {
    "PATH": "/opt/toolchains/riscv64-linux-musl-cross/bin:/opt/toolchains/aarch64-linux-musl-cross/bin:/home/sk/.local/share/zinit/plugins/direnv---direnv:/home/sk/.local/bin:/home/sk/.rustup/toolchains/esp/xtensa-esp-elf/esp-14.2.0_20240906/xtensa-esp-elf/bin:/home/sk/.local/bin:/opt/toolchains/arm-gnu-toolchain-13.3.rel1-x86_64-aarch64-none-linux-gnu/bin:/opt/nvim-linux64/bin:/home/sk/.cursor-server/bin/5c17eb2968a37f66bc6662f48d6356a100b67be0/bin/remote-cli:/home/sk/.local/share/zinit/polaris/bin:/home/sk/.local/bin:/home/sk/.rustup/toolchains/esp/xtensa-esp-elf/esp-14.2.0_20240906/xtensa-esp-elf/bin:/home/sk/.local/bin:/opt/toolchains/arm-gnu-toolchain-13.3.rel1-x86_64-aarch64-none-linux-gnu/bin:/opt/nvim-linux64/bin:/home/sk/.cursor-server/bin/5c17eb2968a37f66bc6662f48d6356a100b67be0/bin/remote-cli:/home/sk/.local/bin:/home/sk/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin",
    "RUST_BACKTRACE": "full",
  },
}
```

PATH设置不能使用 "PATH=PATH_TO_XX:$PATH" or "PATH=PATH_TO_XX:${env:PATH}"