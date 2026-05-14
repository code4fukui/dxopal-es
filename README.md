# dxopal-es

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

Game development framework for [Opal](https://opalrb.com/) with a [DXRuby](http://dxruby.osdn.jp/)-like API, enabling Ruby-based game creation in the browser.

## Demo

- [Triangles Game](https://code4fukui.github.io/dxopal-es/examples/es/triangles.html)
- [JavaScript Interop Example](https://code4fukui.github.io/dxopal-es/examples/es/)

## Features

- **Ruby in the Browser**: Write game logic in Ruby, compiled to JavaScript by Opal.
- **DXRuby-like API**: A familiar API for developers with experience in the popular Japanese game library.
- **2D Rendering**: Draw shapes, images, and text on an HTML5 canvas.
- **Input Handling**: Built-in support for keyboard, mouse, and touch events.
- **Audio**: Play sound files and generate sound effects with the Web Audio API.
- **JavaScript Interop**: Easily call JavaScript functions from your Ruby code.

## Usage

For detailed API documentation, see [yhara.github.io/dxopal](https://yhara.github.io/dxopal/).

Embed the following code in your HTML file to get started:

```html
<canvas id="dxopal-canvas"></canvas>
<script type="module">
import { Opal } from "https://code4fukui.github.io/dxopal-es/build/dxopal.js";
eval(Opal.compile(`require 'dxopal'
Window.load_resources do
  Window.loop do
    x = Window.width / 2
    y = Window.height / 2
    dx = 72
    dy = 50
    Window.draw_triangle_fill(
      x, y - dy,
      x - dx, y + dy,
      x + dx, y + dy,
      [255, 255, 0]
    )
  end
end
`));
</script>
```
([RUN on ES-Jam](https://code4fukui.github.io/htmlprac/?url=https://code4fukui.github.io/dxopal-es/examples/es/simple.html))

## License

MIT (including images and sounds under `examples/`)

## Acknowledgements

- [Opal](https://opalrb.com/)
- [DXRuby](http://dxruby.osdn.jp/)
- [Bxfr](https://www.bfxr.net/): The sound file `examples/apple_catcher/sounds/Explosion2.wav` was created using this tool.

## Contact

This repository is a fork. The original project can be found at: https://github.com/yhara/dxopal