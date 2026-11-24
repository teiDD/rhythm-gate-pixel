# リズム改札（Pixel Station Edition）

駅の改札で「ピン・ポーン」と鳴ったニセきっぷの乗客を、次の拍でタイミングよくぶっ飛ばすリズムゲームです。  
**外部画像・外部音声・ビルドツール一切なし**の **単一 HTML ファイル（約 65 KB）** で動作します。

- **ブラウザで遊ぶ（GitHub Pages）**: https://teidd.github.io/rhythm-gate-pixel/

## 遊び方

1. 画面をクリック／タップ、または `Space` キーで改札オープン（3・2・1・スタート！）
2. 改札を通る乗客の音と合図を聞きます
   - 通常の乗客：そのまま通過させます
   - **ニセきっぷの乗客**：「ピン・ポーン」と鳴ったら、**次の拍**でタイミングよく入力して撃退！
3. 操作キー：画面タップ / クリック / `Space` / `Enter` / `F` / `J`
4. 右下の `sound on / off` で音声のミュート切替ができます

## ローカルで遊ぶ

`index.html` をそのままブラウザ（Chrome / Edge / Safari / Firefox）で開くだけで遊べます（サーバー不要・オフライン動作対応）。

## 技術構成

- **描画**: HTML5 Canvas 2D API（`putImageData` による CPU ピクセルレンダリング、球体・Z バッファ・ベイヤーディザリングによる疑似 3D ドット絵表現）
- **音・リズム同期**: Web Audio API によるリアルタイム合成音（BGM・効果音）と `AudioContext.currentTime` を基準にしたスケジュール管理
- **構成**: 単一 HTML ファイル完結（`index.html` のみ）

## クレジット・ライセンス

この作品の描画エンジン部分は [pixel-plays](https://github.com/amirmushichge/pixel-plays)（Amir Mushich, MIT License）の `engine.js` / `shell.js` を組み込んで制作しています。

コードは [LICENSE](./LICENSE)（MIT License）のもとで公開しています。
