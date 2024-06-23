# OIC2024-Front07
# 数当てゲーム課題

## 課題概要
この課題では、学生は数当てゲームを作成します。
コンピュータが1～100の間でランダムに選んだ数値を、10回の試行までに当てるゲームです。
ユーザー関数やクラスを多用した構造化プログラムを作成します。

## ファイル構成
- `index.html`: ゲームのHTMLファイル
- `css/style.css`: ゲームのスタイルシート
- `js/app.js`: ゲームのJavaScriptファイル

## 課題の流れ
1. フローチャートの作成（Excel）
2. プログラミング（HTML, CSS, JavaScript）

## フローチャートの作成
Excelを使用してゲームのロジックをフローチャートで表現します。以下のステップを含めてください。
- スタート
- 1～100のランダムな数値を生成
- ユーザー入力の受け取り
- 入力が正しいかの検証
- 試行回数のカウント
- 当たりの場合、ゲームクリア
- 試行回数が10回に達した場合、ゲームオーバー
- 再試行のオプション

## プログラミング
フローチャートを元に、以下のファイルを作成します。

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
class NumberGuessingGame {
    constructor() {
        this.randomNumber = this.generateRandomNumber();
        this.attemptsRemaining = 10;
        this.initEventListeners();
    }

    generateRandomNumber() {
        return Math.floor(Math.random() * 100) + 1;
    }

    initEventListeners() {
        document.getElementById('guessButton').addEventListener('click', () => this.checkGuess());
        document.getElementById('restartButton').addEventListener('click', () => this.restartGame());
    }

    checkGuess() {
        const userGuess = parseInt(document.getElementById('guessInput').value);
        if (isNaN(userGuess) || userGuess < 1 || userGuess > 100) {
            this.setMessage('1から100の間の数値を入力してください。');
            return;
        }

        this.attemptsRemaining--;

        if (userGuess === this.randomNumber) {
            this.setMessage('おめでとうございます！正解です！');
            this.endGame();
        } else if (this.attemptsRemaining === 0) {
            this.setMessage(`ゲームオーバー！正解は ${this.randomNumber} でした。`);
            this.endGame();
        } else {
            const hint = userGuess < this.randomNumber ? '大きい' : '小さい';
            this.setMessage(`違います！もっと${hint}数です。`);
            this.updateAttempts();
        }
    }

    setMessage(message) {
        document.getElementById('resultMessage').textContent = message;
    }

    updateAttempts() {
        document.getElementById('attemptsRemaining').textContent = `残り試行回数: ${this.attemptsRemaining}`;
    }

    endGame() {
        document.getElementById('guessButton').disabled = true;
        document.getElementById('restartButton').style.display = 'block';
    }

    restartGame() {
        this.randomNumber = this.generateRandomNumber();
        this.attemptsRemaining = 10;
        this.setMessage('');
        this.updateAttempts();
        document.getElementById('guessButton').disabled = false;
        document.getElementById('restartButton').style.display = 'none';
        document.getElementById('guessInput').value = '';
    }
}

document.addEventListener('DOMContentLoaded', () => {
    new NumberGuessingGame();
});
```

## 提出方法
完成したファイルを提出してください。
プログラムとフローチャートを一つのzipファイルに入れてください。
ファイル名は「数当て+出席番号.zip」とする。

## 注意点
- コードは可読性を保ち、コメントを適宜追加してください。
- 変数名や関数名は分かりやすく命名してください。
- エラー処理を適切に行い、ユーザーが使いやすいインターフェースを提供してください。
```

### フローチャート (Excel)
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

このフローチャートをExcelで図示し、説明を加えてください。
