# Corne keyboard firmware configuration

My configuration of the wireless 6-column corne keyboard using
[ZMK](https://zmk.dev/) together with nickcoutsos
[keymap-editor](https://nickcoutsos.github.io/keymap-editor/). Heavily
influenced by [urob](https://github.com/urob/zmk-config)s meticulous
configuration. Latest firmware can be found under
[Actions](https://github.com/sieuwerts/zmk-config-corne/actions/workflows/build.yml).

![corne](./assets/corne.jpg)

## Hardware

| **Component** | **Type** | **Model** | **Amount** | **Vendor** |
|---------------|-------------------|-----------------------------|-----------:|-----------------|
| PCB | 6-column Wireless | Choc v1 low profile | 1 set | typeractive.xyz |
| Case | Premium Aluminum | Midnight | 1 set | typeractive.xyz |
| Controller | nice!nano | v2.0 | 2 pcs | typeractive.xyz |
| Display | nice!view | With headers | 2 pcs | typeractive.xyz |
| Display cover | Acrylic | Clear | 1 set | typeractive.xyz |
| Sockets | EZ-Solder | Machine sockets and headers | 2 set | typeractive.xyz |
| Keycaps | Hypersonic | Blue | 1 set | typeractive.xyz |
| Switches | Ambient Silent | Twilight | 42 pcs | splitkb.com |
| Battery | 110mAh Li-Po | 3.7V | 2 pcs | aliexpress.com |
| Firmware | ZMK | Latest | N/A | N/A |

## Keymap

The current keymap, this image is automatically generated using
[keymap-drawer](https://github.com/caksoylar/keymap-drawer). See the
[workflow](./.github/workflows/draw-keymaps.yml) for more details. It will be
generated everytime there are changes to the `config/corne.keymap` or
`keymap_drawer.config.yaml` files and push a new commit.

![keymap](./keymap-drawer/corne.svg)
