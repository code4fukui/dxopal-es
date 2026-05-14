# dxopal-es

[DXRuby](http://dxruby.osdn.jp/)風のAPIを持つ[Opal](https://opalrb.com/)向けゲーム開発フレームワークであり、ブラウザ上でRubyを使ったゲーム制作を可能にします。

## デモ

- [Triangles Game](https://code4fukui.github.io/dxopal-es/examples/es/triangles.html)
- [JavaScript Interop Example](https://code4fukui.github.io/dxopal-es/examples/es/)

## 機能

- **ブラウザ上のRuby**: ゲームロジックをRubyで記述し、OpalによってJavaScriptにコンパイルします。
- **DXRuby風API**: 日本で人気のゲームライブラリの経験がある開発者にとって親しみやすいAPIです。
- **2D描画**: HTML5のCanvas上に図形、画像、テキストを描画します。
- **入力処理**: キーボード、マウス、タッチイベントを標準でサポートしています。
- **音声**: Web Audio APIを使用して、音声ファイルの再生や効果音の生成が可能です。
- **JavaScriptとの相互運用**: RubyコードからJavaScriptの関数を簡単に呼び出すことができます。

## 使い方

詳細なAPIドキュメントについては、[yhara.github.io/dxopal](https://yhara.github.io/dxopal/)を参照してください。

始めるには、HTMLファイルに以下のコードを埋め込んでください:

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
([ES-Jamで実行](https://code4fukui.github.io/htmlprac/?url=https://code4fukui.github.io/dxopal-es/examples/es/simple.html))

## ライセンス

MIT（`examples/`配下の画像や音声ファイルを含む）

## 謝辞

- [Opal](https://opalrb.com/)
- [DXRuby](http://dxruby.osdn.jp/)
- [Bxfr](https://www.bfxr.net/): 音声ファイル `examples/apple_catcher/sounds/Explosion2.wav` はこのツールを使用して作成されました。

## お問い合わせ

このリポジトリはフォークです。オリジナルのプロジェクトは以下にあります: https://github.com/yhara/dxopal
