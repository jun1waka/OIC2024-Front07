### 模範解答

#### CHAPTER 1: JavaScriptの基本

##### 記述式問題
**設問1**
JavaScriptで数値の計算を行う方法は、基本的な算術演算子を使用します。以下に加算、減算、乗算、除算の例を示します。
- 加算: `let result = 5 + 3; // resultは8`
- 減算: `let result = 10 - 4; // resultは6`
- 乗算: `let result = 7 * 2; // resultは14`
- 除算: `let result = 20 / 4; // resultは5`

**設問2**
文字列の結合

は`+`演算子を使用します。例として、次のようにして2つの文字列を結合します。
```javascript
let str1 = "Hello";
let str2 = "World";
let result = str1 + " " + str2; // resultは"Hello World"
```

**設問3**
変数の宣言と初期化について説明します。
- `var`: 変数を関数スコープで宣言します。再宣言と再代入が可能です。
- `let`: 変数をブロックスコープで宣言します。再代入が可能ですが、再宣言はできません。
- `const`: 定数をブロックスコープで宣言します。再宣言も再代入もできません。
例:
```javascript
var x = 10;
let y = 20;
const z = 30;
```

**設問4**
関数の定義方法について説明します。例として、2つの引数を受け取り、その合計を返す関数を示します。
```javascript
function add(a, b) {
  return a + b;
}
let result = add(5, 3); // resultは8
```

**設問5**
条件分岐の基本構文である`if`文について説明します。例として、与えられた数値が正の数か負の数かを判定するプログラムを示します。
```javascript
let number = 5;
if (number > 0) {
  console.log("正の数です");
} else if (number < 0) {
  console.log("負の数です");
} else {
  console.log("ゼロです");
}
```

##### 穴埋め式問題
**設問6**
```javascript
let x = 10;
let y = 5;
console.log(x + y); // 15
```

**設問7**
```javascript
let str1 = "Hello";
let str2 = "World";
console.log(str1 + " " + str2); // Hello World
```

**設問8**
修正後のコード:
```javascript
let x = 10;
const y = 20;
console.log(x + y); // 30
```

**設問9**
```javascript
let x = 10;
let y = "10";
console.log(x == y); // true
```

**設問10**
```javascript
let language = "Java";
language += "Script";
console.log(language); // JavaScript
```

##### 多肢選択問題
**設問11**
a) `var`
c) `let`

**設問12**
c) 15

**設問13**
c) `// This is a comment`
d) `/* This is a comment */`

**設問14**
b) `myFunction();`

**設問15**
a) `a is less than b`

#### CHAPTER 2: 基本データ操作

##### 記述式問題
**設問16**
JavaScriptのオブジェクトは、キーと値のペアを格納するコンテナです。例として、`name`と`age`プロパティを持つオブジェクトを定義します。
```javascript
let person = {
  name: "John",
  age: 30
};
```

**設問17**
配列は、複数の値を一つの変数に格納できるデータ構造です。例として、数値の配列を定義し、その配列の各要素に2を掛けるコードを示します。
```javascript
let numbers = [1, 2, 3, 4, 5];
for (let i = 0; i < numbers.length; i++) {
  numbers[i] *= 2;
}
console.log(numbers); // [2, 4, 6, 8, 10]
```

**設問18**
ループ処理は、同じ処理を複数回繰り返すために使用されます。例として、`for`ループを使って1から10までの数を出力するコードを示します。
```javascript
for (let i = 1; i <= 10; i++) {
  console.log(i);
}
```

**設問19**
クラスは、オブジェクトのひな型を定義するための構文です。例として、`Person`クラスを定義し、そのインスタンスを生成するコードを記述します。
```javascript
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
  greet() {
    console.log(`Hello, my name is ${this.name} and I am ${this.age} years old.`);
  }
}

let john = new Person("John", 30);
john.greet(); // Hello, my name is John and I am 30 years old.
```

**設問20**
DOM操作とイベントハンドリングは、ユーザーの操作に応じてページの内容を動的に変更するために使用されます。例として、ボタンがクリックされたときにアラートを表示するコードを示します。
```javascript
document.getElementById("myButton").addEventListener("click", function() {
  alert("Button clicked!");
});
```

##### 穴埋め式問題
**設問21**
```javascript
let person = {
  firstName: "John",
  lastName: "Doe",
  fullName: function() {
    return this.firstName + " " + this.lastName;
  }
};
console.log(person.fullName()); // John Doe
```

**設問22**
```javascript
let fruits = ["Apple", "Banana", "Cherry"];
console.log(fruits.length); // 3
```

**設問23**
```javascript
let numbers = [5, 10, 15, 20];
console.log(numbers[3]); // 20
```

**設問24**
```javascript
for (let i = 1; i <= 5; i++) {
  console.log(i); // 1 2 3 4 5
}
```

**設問25**
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
console.log(dog instanceof Animal); // true
```

##### 多肢選択問題
**設問26**
b) `Array`

**設問27**
b) `Banana`

**設問28**
a) 0 1 2

**設問29**
b) `class MyClass {}`

**設問30**
a) `Button clicked!`とアラートが表示される
