# Design source

`icon.svg` is the source for the favicon set in `static/`. It is a placeholder
monogram, not a real logo.

To regenerate after editing it (macOS, no ImageMagick required):

```sh
qlmanage -t -s 512 -o . icon.svg          # -> icon.svg.png at 512x512
for s in 180 32 16; do cp icon.svg.png i$s.png; sips -z $s $s i$s.png; done
# favicon.ico is a PNG-payload ICO built from i16.png and i32.png
```

Not under `static/`, so it is not published with the site.
