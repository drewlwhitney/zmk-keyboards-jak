# zmk-keyboards-jak
ZMK firmware for the [Jak keyboard](https://github.com/drewlwhitney/jak).

## Usage
To load the module, run 
```
zmk cd
``` 

followed by

```
zmk module add https://github.com/drewlwhitney/zmk-keyboards-jak.git
```

To add the keyboard, run

```
zmk keyboard add
```

and select `jak` for the keyboard. For the controller, select:
- `xiao_ble` for wireless (with the [XIAO-BLE](https://wiki.seeedstudio.com/XIAO_BLE/))

- `xiao_rp2040` for wired (with the [XIAO-RP2040](https://wiki.seeedstudio.com/XIAO-RP2040/)), see below

### Wired
Add

```c++
/ {
    wired_split {
        compatible = "zmk,wired-split";
        device = <&xiao_serial>;
    };
};

&xiao_serial { status = "okay"; };
```

to the bottom of your keymap file to enable split communication, then build with the `xiao_rp2040` as the board.
