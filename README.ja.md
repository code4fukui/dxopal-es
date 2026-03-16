# DXOpal

Opal言語を使ったゲーム開発フレームワークです。[DXRuby](http://dxruby.osdn.jp/)と似たようなAPIを提供しています。

## デモ

- [Rubyでの三角形ゲーム](https://code4fukui.github.io/dxopal-es/examples/es/triangles.html)
- [RubyからJavaScriptの関数を呼び出す](https://code4fukui.github.io/dxopal-es/examples/es/)

## 機能

- Opal言語を使ったゲーム開発
- DXRubyと似たようなAPIを提供

## 使い方

詳しくは[yhara.github.io/dxopal](https://yhara.github.io/dxopal/)を参照してください。

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

## ライセンス

MIT (examples/以下の画像/サウンドも含む)

## 謝辞

- [Opal](https://opalrb.com/)
- [DXRuby](http://dxruby.osdn.jp/)
- [Bxfr](https://www.bfxr.net/) examples/apple_catcher/sounds/Explosion2.wavはこちらで作成