# APRS

## direwolf + rtl-sdr

Using `rtl_fm` in 144.930 MHz (APRS Argentina), `-p` for PPM error correction and `direwolf` for decoding using `igate.conf`:

```bash
$ rtl_fm -f 144930000 -M fm -s 200000 -r 32000 -g 30 -p 0 | direwolf -n 1 -r 32000 -b 16 -t 0 -d ddpii -c igate.conf -l . -
```
