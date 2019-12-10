# setup-ada

This action sets up a Ada/SPARK environment for use in GitHub actions.

# Usage

See [action.yml](action.yml)

Basic:
```yaml
steps:
- uses: actions/checkout@master
- uses: ada-actions/toolchain@dev
  with:
    distrib: fsf
    target: native
- run: gprbuild hello
- uses: ada-actions/toolchain@dev
  with:
    distrib: community
    target: arm-elf
- run: gprbuild --target=arm-eabi --RTS=zfp-microbit hello
```

# License

The scripts and documentation in this project are released under the [MIT License](LICENSE)

# Contributions

Contributions are welcome!  See [Contributor's Guide](docs/contributors.md)
