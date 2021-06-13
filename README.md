# rime-colemak

## About

This implements the Colemak layout under Rime. The primary use case is to type plain text in Colemak, but be able to use QWERTY shortcuts.

## Installing

First ensure you have plum installed. For macOS this would be:

```bash
cd ~/Library/Rime
wget https://git.io/rime-install
```

For Linux this would be:

```bash
cd ~/.config/fcitx/rime
wget https://git.io/rime-install
```

Then install `gkovacs/rime-colemak` using plum:

```bash
bash rime-install gkovacs/rime-colemak
```

Finally edit `default.custom.yaml` and add `colemak` to the schema list:

```bash
patch:
  schema_list:
    - schema: colemak
```

If you wish to change the hotkey for changing keyboard layout or the layout that it switches to, create a file `colemak.custom.yaml` and add the following, substituting your desired shortcut:

```bash
patch:
  key_binder:
    import_preset: default
    bindings:
      - {accept: "Control+space", select: td_pinyin_flypy_extra, when: always}
```