# Elemental-swordtail
Come to me beautiful sinner

![buh](https://github.com/nicolasbaez/Spice-salmonberry/blob/main/xp044.gif)
```javascript
setup = (_) => createCanvas((w = 500), w, WEBGL);
h = 255;
draw = (_) => {
  colorMode(HSB, h);
  rotateX(1);
  rotateZ(w);
  clear();
  noFill();
  for (i = -h; i < h; i += 4) {
    for (j = -h; j < h; j += 9) {
      x = map(i, -h, h, -9, 9);
      y = map(j, -h, h, -9, 9);
      stroke(abs(i), abs(j), w);
      point(i, j, map(sin(x * y) / (x * y), -2, 2, -h, h));
    }
  }
  if (w == 500) saveGif("xp044.gif", 157, { delay: 0, units: "frames" });
  w -= 0.04;
};
