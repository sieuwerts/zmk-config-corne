# Corne keyboard firmware configuration

My personal configuration of the wireless 6-column corne keyboard using
[ZMK](https://zmk.dev/) together with nickcoutsos
[keymap-editor](https://nickcoutsos.github.io/keymap-editor/). Heavily
influenced by [urob](https://github.com/urob/zmk-config)s meticulous
configuration. Latest firmware can be found under
[Actions](https://github.com/sieuwerts/zmk-config-corne/actions/workflows/build.yml).
This keymap is designed to work well for me as a software engineer, primarily
spending my time in neovim on macos.

![corne](./assets/corne.jpg)

## Keymap

I use a regular QWERTY layout with some modification of the symbols placement
on the default layer. The main reason for sticking with a QWERTY layout is
solely for the purpose of not having to configure neovim for another layout. I
know it's very much possible, but I like the mnemonic default mappings of
vim/neovim, and I don't want to mess around too much with it.

### Timer-less home row mods

I have adopted
[urob](https://github.com/urob/zmk-config?tab=readme-ov-file#timeless-homerow-mods)s
configuration for timer-less home row mods, all credit goes to them. See their
config repo for more information.

In short it aims to reduce misfires of home row mods while still being snappy
enough to not feel like you are being slowed down while typing fast. This is
achieved by setting up a `ZMK_HOLD_TAP` behaviour with the `balanced` flavor
and perhaps the most important feature for reducing misfires
`require-prior-idle-ms`. It also enforces some delay when used together with a
key on the same side of the keyboard. This works very well since the home row
mods are mirrored for each hand. See the configuration for more information.

### Combos vs layers

Coming from QMK, not (natively) having the option of requiring some idle time
in between key presses for triggering combos was a deal breaker for me.
Luckily, ZMK solved that by introducing `require-prior-idle-ms`. Before, I used
to have separate layers for a lot of functionality, like a layer for system
operations, Swedish letter keys (`åäö`), another one for symbols or numbers
etc. But it never felt really smooth while having to constantly jump between
momentary layers. So I moved on to trying to really limit the amount of
different layers that I have by replacing a lot of the functionality with
combos instead.

### Combos

- Symbols

- Numbers

- Tab key

- Swedish keys (eurkey)

- Toggle &tog layers (gaming layer).

- vertical vs horisontal combos

### Layers

Although combos are great, layers are still useful. I am very conservative of
adding more layers, and try to keep it to a minimum to keep it simple and
maintain a good flow when typing. I currently have three layers, one default
layer, a momentary system layer and a gaming toggle layer.

#### Default layer

#### System layer

#### Gaming layer

- Shift and control to "normal"
- Disable combos except for numbers
- GUI button / alt
- Still &mo system layer if needed.
- Dedicated tab key

### Smart shift

Also here, I have adopted some behaviour from the fantastic configuration of
[urob](https://github.com/urob/zmk-config?tab=readme-ov-file#capsword). The
middle left thumb key has three different functions:

- `tap`:

  - Sticky shift, will trigger shift behaviour for the next keypress only.

- `hold`:

  - Regular shift behaviour, will stay active until key is released.

- `double tap`:

  - Invoke ZMKs [caps_word](https://zmk.dev/docs/keymaps/behaviors/caps-word)
    behaviour.

The reason for having a dedicated key for shift instead of just relying on the
ones from the home row mods is that although it's convenient to use HRMs, shift
is the one key that's often used while just typing regular text (or when
_writing_ code). While having the required delay for triggering HRMs (and
combos, but we'll get to that later on) is a blessing, it does make it hard to
achieve `shift` functionality while writing fast. So I find that a combination
of the two complements each other really well.

### Hyper key

I have a dedicated `HYPER` key to use together with
[Raycast](https://www.raycast.com/) where I have set up shortcuts for
triggering certain applications or behaviours. e.g. `HYPER` + `B` will
focus/open my browser or `HYPER` + `T` for my terminal emulator.

## Keymap drawing

The current keymap, this image is automatically generated using
[keymap-drawer](https://github.com/caksoylar/keymap-drawer). See the
[workflow](./.github/workflows/draw-keymaps.yml) for more details. It will be
generated everytime there are changes to the `config/corne.keymap` or
`keymap_drawer.config.yaml` files and push a new commit.

![keymap](./keymap-drawer/corne.svg)

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
