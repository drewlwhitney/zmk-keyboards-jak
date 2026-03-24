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

<br>

To add the keyboard, run

```
zmk keyboard add
```

and select `jak` for the keyboard. For the controller, select:
- `seeeduino_xiao_ble` for wireless

- `seeeduino_xiao_rp2040` for wired
