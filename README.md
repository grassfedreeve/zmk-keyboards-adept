# Adept ZMK Module

This repository contains the shield files for the [AdeptBLE](https://github.com/taichan1113/AdeptBLE) to allow users to build firmware. This can be done by adding the module to the west.yml found in your zmk-config's config directory. There is a full guide available for this here: [ZMK Modules Doc](https://zmk.dev/docs/features/modules)

## Usage

Edit your west.yml file found in your zmk-config's config directory to add the adept module. Example:

```
manifest:
  remotes:
    - name: zmkfirmware
      url-base: https://github.com/zmkfirmware
    - name: grassfedreeve
      url-base: https://github.com/grassfedreeve
    - name: badjeff
      url-base: https://github.com/badjeff
  projects:
    - name: zmk
      remote: zmkfirmware
      revision: main
      import: app/west.yml
    - name: zmk-keyboards-adept
      remote: grassfedreeve
      revision: main
    - name: zmk-pmw3610-driver
      remote: badjeff
      revision: main
  self:
    path: config
```
Once you have the module added to your west.yml you can then build firmware as if it was in your config's shield directory or in ZMK main.

