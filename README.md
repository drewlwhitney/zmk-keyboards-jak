# zmk-keyboards-jak
ZMK firmware for the [Jak keyboard](https://github.com/drewlwhitney/jak).

## Usage
To load the module, modify your `config/west.yml` to look something like this:
```
manifest:
  defaults:
    revision: v0.3
  remotes:
    - name: zmkfirmware
      url-base: https://github.com/zmkfirmware
    - name: drewlwhitney
      url-base: https://github.com/drewlwhitney
  projects:
    - name: zmk
      remote: zmkfirmware
      import: app/west.yml
    - name: zmk-keyboards-jak
      remote: drewlwhitney
  self:
    path: config
```
