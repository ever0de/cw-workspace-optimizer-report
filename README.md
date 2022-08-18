# workspace-optimizer test

**It was confirmed that the problem was using the toolchain file, not the problem of a specific version.**

## Command

- success command

```shell
cargo wasm
```

- failed command

```shell
docker run --rm -v "$(pwd)":/code \
  --mount type=volume,source="$(basename "$(pwd)")_cache",target=/code/target \
  --mount type=volume,source=registry_cache,target=/usr/local/cargo/registry \
  cosmwasm/workspace-optimizer:0.12.6
```
