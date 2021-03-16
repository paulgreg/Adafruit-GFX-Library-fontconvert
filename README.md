# Adafruit-GFX-Library-fontconvert

That repository is an extract from [Adafruit-GFX-Library](https://github.com/adafruit/Adafruit-GFX-Library).

 It contains only the fontconvert directory with a few fonts in `fontconvert/in`. The fonts have been modified to have the € sign at position 0x80.

 Some generated fonts have been generated in different size in `fontconvert/out` directory.

## To generate a font with € sign

  * install [fontforge](https://fontforge.org)
  * go to the  € character at position 0x20AC, copy it to 0x80
  * generate the font (ignore warnings)
  * use fontconvert program like `./fontconvert font-with-euro-sign-at-0x80.otf 9 32 255 > font.h` to generate a 9pt font size with characters from 32 to 255 (€ will be at 0x80)

### Usage exemple

  ./fontconvert in/NotoMono-Regular-euro.ttf 14 32 255 > out/NotoMono_Regular_euro14pt8b.h

## Resources

- https://learn.adafruit.com/adafruit-gfx-graphics-library/using-fonts
- https://forum.arduino.cc/index.php?topic=418598.45
- https://www.sigmdel.ca/michel/program/misc/gfxfont_8bit_02_fr.html

## License

- fontconvert fron Adafruit-GFX-Library : https://github.com/Adafruit/Adafruit-GFX-Library/tree/master/license.txt
- fonts from debian packages : https://packages.debian.org/fr/stable/fonts-cantarell, https://packages.debian.org/fr/buster/fonts-noto-mono
