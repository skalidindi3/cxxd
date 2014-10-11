About
=====

`cxxd` is a colorized drop-in for `xxd` intended to greatly increase the ease of visual pattern recognition in hexdumps. This effect is achieved by calling `xxd` in a subprocess and colorizing the output. It will, by default, use ansi color codes to color a byte based on it's value. This utility should support all xxd functionality, with the inclusion of 3 extra optargs:

```
-x, --pixelate          replace hex values with colored blocks
-d, --display_palette   display colors with the byte range covered
-R, --rotate_colors     circularly rotate color gradient base index
```

Take it for a spin:
```bash
for i in {0..255}; do printf `printf "\\\\\x%02x" $i`; done | ./cxxd
```

TODO
====
* Tests
