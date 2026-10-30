<p align="center">
  <a href="README.md">한국어</a> · <a href="README.en.md">English</a> · <a href="README.zh-CN.md">简体中文</a> · <b>日本語</b>
</p>

<p align="center">
  <img src="docs/icon.png" width="128" alt="Audio Mixer">
</p>

<h1 align="center">Audio Mixer</h1>

<p align="center">
  macOS メニューバーのオーディオミキサー · アプリ別音量 · イコライザ · AutoEQ<br>
  <a href="https://github.com/jayusop/Audio-Mixer/releases/latest"><b>⬇ 最新版をダウンロード</b></a> ·
  <a href="https://jayusop.github.io/Audio-Mixer/?lang=ja">紹介ページ</a>
</p>

<p align="center">
  <img alt="macOS 14.2+" src="https://img.shields.io/badge/macOS-14.2%2B-8f7dff">
  <img alt="Apple Silicon / Intel" src="https://img.shields.io/badge/Apple%20Silicon%20%2F%20Intel-supported-ff6fb6">
  <img alt="Release" src="https://img.shields.io/github/v/release/jayusop/Audio-Mixer?color=5fe1f2">
</p>

---

メニューバーに常駐し、**アプリ別音量**、**入出力デバイスの音量**、**グラフィック/パラメトリックイコライザ**、**AutoEQ ヘッドホン補正プロファイル**を提供する macOS アプリです。仮想オーディオドライバのインストールは不要です。

> 動作環境: macOS 14.2 以降（Apple シリコン / Intel）<br>
> 🌐 アプリの言語は macOS のシステム言語（英語、韓国語、中国語、日本語）に従い、それ以外の言語では英語で表示されます。

## インストール

1. [Releases](https://github.com/jayusop/Audio-Mixer/releases/latest) から `AudioMixer.zip` をダウンロードして展開し、`AudioMixer.app` を**アプリケーション**フォルダへ移動します。
2. 初めて開くと「開発元を確認できません」という警告が表示されます（Apple の公証を受けていない個人配布アプリのため）。**完了**をクリックしたあと、**システム設定 › プライバシーとセキュリティ**の下のほうにある**このまま開く**をクリックしてください。ターミナルを使う場合:
   ```bash
   xattr -dr com.apple.quarantine /Applications/AudioMixer.app
   ```
3. メニューバーにフェーダーのアイコンが表示され、初めてオーディオを処理するときに**「システムオーディオ録音」**の許可を求められます → **許可**。（見逃した場合は システム設定 › プライバシーとセキュリティ › 画面収録とシステムオーディオ録音 でオンにしてください。）

> アップデート後にまた許可を求められた場合は、許可の一覧から古い Audio Mixer の項目を削除して、もう一度許可してください。

## 機能

| 項目 | 機能 |
|---|---|
| ミキサー | 出力/入力デバイスの選択、ハードウェア音量・消音、ハードウェア音量のないデバイス（HDMI など）はソフトウェア音量 |
| アプリ別音量 | 再生中のアプリを自動検出、0–100%（オプションで 200%）、消音、レベルメーター、アプリごとの設定を記憶、処理対象外の指定 |
| イコライザ | 10バンドのグラフィック EQ（±12 dB）、最大 32 個のパラメトリックフィルタ（PK/LSC/HSC/LP/HP/NO）、周波数特性カーブ、ドラッグ編集 |
| AutoEQ | AutoEQ データベース（約 8,800 機種のヘッドホン/イヤホン）をオンラインで検索・適用、ParametricEQ.txt の読み込み/書き出し |
| プリセット | 内蔵 17 種類 + ユーザープリセットの保存/上書き/削除、**出力デバイスごとのプリセット自動切り替え** |
| 音質の保護 | 自動プリアンプ（最大ブースト分を減衰）、ピークリミッター、ハードクリップ保護、L/R バランス |
| その他 | ログイン時に起動、処理全体のオン/オフ、韓国語 · 英語 · 中国語 · 日本語 UI |

## 安心してお使いいただけます

- **録音しません**: 音声はリアルタイムで処理されるだけで、保存や外部への送信は一切されません。
- **終了しても音はそのまま**: Audio Mixer が終了（異常終了を含む）すると、すべてのアプリの音がすぐに元どおりに戻ります。
- **自動復旧**: 出力デバイスの変更やスリープ/復帰のあとも自動で再接続します。
- **干渉しません**: 別のオーディオデバイスへ直接出力しているアプリ（例: オーディオインターフェースを使う DAW）には手を加えません。

## 注意事項 / 制限

- 許可しない場合、アプリ別音量と EQ は動作せず（音は通常どおり再生されます）、デバイス音量の操作のみ可能です。
- アプリが再生を始めた直後は、ごく短い間だけ処理前の音が聞こえることがあります。

## クレジット & お問い合わせ

- EQ プロファイルデータ: [AutoEq](https://github.com/jaakkopasanen/AutoEq) (jaakkopasanen)
- バグ報告: [Issues](https://github.com/jayusop/Audio-Mixer/issues) · メール jayusop@gmail.com
