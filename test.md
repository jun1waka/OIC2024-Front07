### 期末試験対策問題

#### CHAPTER 1: JavaScriptの基本

##### 記述式問題
**設問1**
JavaScriptで数値の計算を行う方法を説明してください。また、加算、減算、乗算、除算の例をそれぞれ挙げてください。

**設問2**
文字列の結合について説明してください。例を挙げて、`+`演算子を使って2つの文字列を結合する方法を示してください。

**設問3**
変数の宣言と初期化について説明してください。また、`var`、`let`、`const`の違いについても述べてください。

**設問4**
関数の定義方法について説明してください。例として、2つの引数を受け取り、その合計を返す関数を記述してください。

**設問5**
条件分岐の基本構文である`if`文について説明してください。例を挙げて、与えられた数値が正の数か負の数かを判定するプログラムを示してください。

##### 穴埋め式問題
**設問6**
次のコードは何を出力しますか？適切な値を答えてください。
```javascript
let x = 10;
let y = 5;
console.log(x + y); // _______
```

**設問7**
次のコードは何を出力しますか？適切な値を答えてください。
```javascript
let str1 = "Hello";
let str2 = "World";
console.log(str1 + " " + str2); // _______
```

**設問8**
次のコードにおけるエラーを修正してください。
```javascript
let x = 10;
const y;
y = 20;
console.log(x + y);
```

**設問9**
次のコードで`true`が出力されるようにするには、`______`に何を入れればよいですか？
```javascript
let x = 10;
let y = "10";
console.log(x == ______); // true
```

**設問10**
次のコードで`JavaScript`という文字列を出力するためには、`______`に何を入れればよいですか？
```javascript
let language = "Java";
language += ______;
console.log(language); // JavaScript
```

##### 多肢選択問題
**設問11**
次の中で、JavaScriptの変数宣言に使われるキーワードはどれですか？
a) `var`
b) `int`
c) `let`
d) `double`

**設問12**
次のコードの出力はどれですか？
```javascript
let num = 10;
num += 5;
console.log(num);
```
a) 5
b) 10
c) 15
d) 20

**設問13**
次のうち、JavaScriptの正しいコメントの書き方はどれですか？
a) `<!-- This is a comment -->`
b) `# This is a comment`
c) `// This is a comment`
d) `/* This is a comment */`

**設問14**
次のうち、関数を呼び出す正しい方法はどれですか？
a) `function myFunction();`
b) `myFunction();`
c) `call myFunction();`
d) `invoke myFunction();`

**設問15**
次のコードの出力はどれですか？
```javascript
let a = 3;
let b = 7;
if (a < b) {
  console.log("a is less than b");
} else {
  console.log("a is greater than or equal to b");
}
```
a) `a is less than b`
b) `a is greater than or equal to b`
c) `Syntax error`
d) `Type error`

#### CHAPTER 2: 基本データ操作

##### 記述式問題
**設問16**
JavaScriptのオブジェクトについて説明してください。例として、`name`と`age`プロパティを持つオブジェクトを定義してください。

**設問17**
配列の定義と操作方法について説明してください。例として、数値の配列を定義し、その配列の各要素に2を掛けるコードを記述してください。

**設問18**
ループ処理の基本的な使い方について説明してください。例として、`for`ループを使って1から10までの数を出力するコードを示してください。

**設問19**
クラスの定義方法について説明してください。例として、`Person`クラスを定義し、そのインスタンスを生成するコードを記述してください。

**設問20**
DOM操作とイベントハンドリングについて説明してください。例として、ボタンがクリックされたときにアラートを表示するコードを記述してください。

##### 穴埋め式問題
**設問21**
次のコードで`"John Doe"`を出力するには、`______`に何を入れればよいですか？
```javascript
let person = {
  firstName: "John",
  lastName: "Doe",
  fullName: function() {
    return this.firstName + " " + this.lastName;
  }
};
console.log(person.______()); // John Doe
```

**設問22**
次のコードで配列の長さを出力するには、`______`に何を入れればよいですか？
```javascript
let fruits = ["Apple", "Banana", "Cherry"];
console.log(fruits.______); // 3
```

**設問23**
次のコードで`20`を出力するには、`______`に何を入れればよいですか？
```javascript
let numbers = [5, 10, 15, 20];
console.log(numbers[______]); // 20
```

**設問24**
次のコードで1から5までの数を順に出力するには、`______`に何を入れればよいですか？
```javascript
for (let i = 1; i <= 5; i++) {
  console.log(______); // 1 2 3 4 5
}
```

**設問25**
次のコードで`true`が出力されるようにするには、`______`に何を入れればよいですか？
```javascript
class Animal {
  constructor(name) {
    this.name = name;
  }
  speak() {
    console.log(this.name + " makes a noise.");
  }
}

class Dog extends Animal {
  speak() {
    console.log(this.name + " barks.");
  }
}

let dog = new Dog("Rex");
dog.speak();
console.log(dog instanceof ______); // true
```

##### 多肢選択問題
**設問26**
次の中で、JavaScriptのビルトインオブジェクトはどれですか？
a) `Document`
b) `Array`
c) `Screen`
d) `Cookie`

**設問27**
次のコードの出力はどれですか？
```javascript
let fruits = ["Apple", "Banana", "Cherry"];
console.log(fruits[1]);
```
a) `Apple`
b) `Banana`
c) `Cherry`
d) `undefined`

**設問28**
次のコードの出力はどれですか？
```javascript
let i = 0;
while (i < 3) {
  console.log(i);
  i++;
}
```
a) 0 1 2
b) 1 2 3
c) 0 1 2 3
d) 1 2

**設問29**
次のうち、クラスの定義として正しいものはどれですか？
a) `class myClass {}`
b) `class MyClass {}`
c) `function MyClass {}`
d) `function class MyClass {}`

**設問30**
次のコードの出力はどれですか？
```javascript
document.getElementById("myButton").addEventListener("click", function() {
  alert("Button clicked!");
});
```
a) `Button clicked!`とアラートが表示される
b) コンソールに`Button clicked!`と表示される
c) 何も起こらない
d) エラーが発生する
