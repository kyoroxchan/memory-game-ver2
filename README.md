# Memory Game

このプロジェクトは、神経衰弱ゲームを実装したウェブアプリケーションです。ユーザーはカードをめくり、同じカードを見つけることを目指します。

## ファイル構成

- `index.html`: アプリケーションのメインHTMLファイル。ゲームのUIを構成する基本的なHTML要素が含まれています。
- `styles/style.css`: ゲームのスタイルを定義するCSSファイル。カードのデザイン、レイアウト、アニメーションなどのスタイルが含まれています。
- `scripts/app.js`: ゲームのロジックを実装するJavaScriptファイル。カードのクリックイベント、マッチングロジック、ゲームの進行管理などの関数が含まれています。
- `sounds/`: ゲーム内で使用される音声ファイルが含まれています。
  - `clear-sound.mp3`: ゲームクリア時の音声
  - `flip-sound.mp3`: カードをめくるときの音声
  - `match-sound.mp3`: カードが一致したときの音声
  - `start-sound.mp3`: ゲーム開始時の音声
  - `unflip-sound.mp3`: カードを裏向きに戻すときの音声
  - `決定ボタンを押す40.mp3`: 特定のアクション時の音声
- `images/`: ゲーム内で使用される画像ファイルが含まれています。
  - `back-face/`: カードの裏面画像
    - `1.png` から `14.png`: カードの裏面画像
  - `front-face.png`: カードの表面画像

## インストール手順

1. このリポジトリをクローンまたはダウンロードします。
    ```sh
    git clone <リポジトリのURL>
    ```
2. `index.html`ファイルをブラウザで開きます。

## 使用方法

1. ゲームが開始されると、カードが裏向きに配置されます。
2. カードをクリックしてめくり、同じカードを見つけることを目指します。
3. すべてのカードのペアを見つけるとゲームが終了します。

## ゲームのロジック

### カードの生成

`generateCards` 関数は、指定されたペア数のカードを生成し、ゲームボードに追加します。

### カードのシャッフル

`shuffle` 関数は、生成されたカードをランダムに配置します。

### カードのめくり

`flipCard` 関数は、カードをクリックしたときにカードをめくり、音声を再生します。

### カードの一致チェック

`checkForMatch` 関数は、めくった2枚のカードが一致するかどうかをチェックし、一致した場合は `disableCards` 関数を呼び出し、一致しない場合は `unflipCards` 関数を呼び出します。

### ゲームの再スタート

`restartGame` 関数は、ゲームを再スタートし、すべてのカードをリセットします。

## スタイル

`styles/style.css` ファイルには、ゲームの見た目を整えるためのスタイルが含まれています。レスポンシブデザインを採用しており、PCとモバイルの両方で快適にプレイできます。

## 音声ファイル

ゲーム内で使用される音声ファイルは、ユーザーのアクションに応じて再生されます。音声ファイルは `sounds/` ディレクトリに保存されています。

## 画像ファイル

ゲーム内で使用される画像ファイルは、カードの表面と裏面の画像です。画像ファイルは `images/` ディレクトリに保存されています。

## ライセンス

このプロジェクトはMITライセンスの下で公開されています。詳細は `LICENSE` ファイルを参照してください。