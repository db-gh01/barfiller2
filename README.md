## barfiller2

Windowerアドオンのbarfiller（作者Morath86さん）に以下の機能を追加したものです。

- バーの長さを任意に設定可能
- リミットポイント, メリットポイントの表示に対応（数字のみ）

設定情報の構造が変わっているのでbarfillerのsettings.xmlをそのまま使うことはできません。barfiller2を一度ロードすることで自動生成される data/settings.xml を編集してリロードすることで設定を行ってください。

設定情報のbarfillerからの変更箇所は以下のとおりです。
```
<Pos>
    <Bottom>true</Bottom>
    <Right>true</Right>
    <X>-585</X>
    <Y>-22</Y>
</Pos>
<Images>
    <Width>400</Width>
</Images>
<ShowDetails>
    <LimitPoints>true</LimitPoints>
    <MeritPoints>true</MeritPoints>
</ShowDetails>
```

- `Pos > X` `Pos > Y`

バー表示の基準座標。バーの枠を除いた本体部分の左上座標。

- `Pos > Bottom` `Pos > Right`

バーの座標指定を画面下/画面右を基準とするかをtrue/falseで指定。

- `Images > Width`

バーの長さ（枠を除いた本体部分の長さ）を指定。

- `ShowDetails > LimitPoints` `ShowDetails > MeritPoints`

リミポメリポの数値を表示するかどうかの指定
