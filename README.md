# OIC2024-Front07
# 数当てゲーム課題

# 数当てゲーム

## 概要
このプロジェクトは、ユーザーが1から100の間でランダムに生成された数値を10回以内に当てる数当てゲームです。
- コンピュータが1～100の間でランダムに選んだ数値を、ユーザーが10回以内に当てるゲームです。
- プログラムは構造化する。
- コメントを多用し、コードの各部分の説明を行う。
- 言語は日本語（utf-8）で記述する。
- ユーザー定義関数とクラスを使用する。
- 3項演算子は使用しない。

## 提出方法
完成したファイルを提出してください。
プログラムをzipファイルに入れてください。
ファイル名は「数当て+出席番号.zip」とする。

## ファイル構成
- **index.html**: ゲームのHTML構造
- **css/style.css**: ゲームのスタイル設定
- **js/app.js**: ゲームのロジックを含むJavaScriptファイル

## 使用方法
1. index.htmlをブラウザで開く。
2. 表示された入力フィールドに1から100の間の数値を入力し、「送信」ボタンを押す。
3. ゲームからのフィードバックに従って、数値を当てる。

### フローチャート 
フローチャートは以下の手順で作成します。

1. **スタート**
2. **ランダムな数値を生成**: 1～100の間でランダムな数値を生成する
3. **ユーザー入力を受け取る**: ユーザーが数値を入力する
4. **入力値が1～100の範囲かをチェック**: 
   - 範囲外の場合: メッセージを表示し、再度入力を促す
5. **試行回数のカウントを更新**: 試行回数を減らす
6. **入力値が正解かをチェック**: 
   - 正解の場合: おめでとうメッセージを表示し、ゲームを終了
   - 不正解の場合: 残り試行回数をチェック
7. **試行回数が0かをチェック**: 
   - 試行回数が残っている場合: ヒントを表示し、再度入力を促す
   - 試行回数が0の場合: ゲームオーバーメッセージを表示し、ゲームを終了
8. **再スタートオプションを表示**: ゲーム終了後、再スタートボタンを表示


## プロジェクトの設定
このプロジェクトは、以下のディレクトリ構造を持ちます。
```
/数当て
│
├── index.html
├── css/
│   └── style.css
└── js/
    └── app.js
```

## プログラミング例
フローチャートを元に、以下のファイルを作成します。
JavaScriptのソースにはロジックが入っていません。

### index.html
```html
<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>数当てゲーム</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <div class="game-container">
        <h1>数当てゲーム</h1>
        <p>1～100の間の数を当ててください。10回まで挑戦できます。</p>
        <input type="number" id="guessInput" placeholder="1～100の数値を入力">
        <button id="guessButton">試行</button>
        <p id="resultMessage"></p>
        <p id="attemptsRemaining">残り試行回数: 10</p>
        <button id="restartButton" style="display: none;">再スタート</button>
    </div>
    <script src="js/app.js"></script>
</body>
</html>
```

### css/style.css
```css
body {
    font-family: Arial, sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
    background-color: #f0f0f0;
}

.game-container {
    text-align: center;
    background-color: #fff;
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

input {
    margin: 10px 0;
    padding: 10px;
    font-size: 16px;
    width: calc(100% - 24px);
}

button {
    padding: 10px 20px;
    font-size: 16px;
    cursor: pointer;
}

#resultMessage {
    margin: 20px 0;
    font-size: 18px;
}

#attemptsRemaining {
    font-size: 16px;
}
```

### js/app.js
```javascript
// 数当てゲームクラスの定義
class GuessingGame {
    constructor() {
        // ゲームを初期化する
        this.initializeGame();
    }

    // ゲームの初期化メソッド
    initializeGame() {
        // ランダムな数値を生成してプロパティに格納
        // 試行回数の初期化
        // 最大試行回数の設定
        // 初期メッセージを表示
    }

    // 1から100のランダムな数値を生成するメソッド
    generateRandomNumber() {
        // Math.random()で0から1のランダムな数値を生成し、100を掛けて1を加える
    }

    // ユーザーが数値を入力した際に呼び出されるメソッド
    makeGuess() {
        // ユーザーの入力を取得し、整数に変換
        // 入力値が有効かどうかをチェック
        // 試行回数をカウント
        // ユーザーの入力値と正解値を比較
    }

    // メッセージを更新するメソッド
    updateMessage(message) {
        // メッセージを表示する要素を取得し、テキストを更新
    }
}

// ゲームのインスタンスを生成
const game = new GuessingGame();

```

## 注意点
- コードは可読性を保ち、コメントを適宜追加してください。
- 変数名や関数名は分かりやすく命名してください。
- エラー処理を適切に行い、ユーザーが使いやすいインターフェースを提供してください。

