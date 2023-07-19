# JavaScriptの学習記録

### truthy falsy
falsy → 真偽値に変換した際に"偽(false)"とみなされる値のこと。
truthy → それ以外

<!-- falsyな値の一覧 -->
false
0 (数字)
0n (big int)
"" (空文字)
null
undefined
NaN (Not a Number)

<!-- 具体的な例 -->
const falsy = 0;
const truthy = 1;
console.log(Boolean(truthy)); // 結果: true
console.log(Boolean(falsy)); // 結果: false

// 論理積 (&&) について
const resultA = "" && "foo";
const resultB = 2 && 1 && 0 && 3;
const resultC = "foo" && 4;

console.log(resultA); // 結果: "" (最初に偽になった値が返される)
console.log(resultB); // 結果: 0 (最初に偽になった値が返される)
console.log(resultC); // 結果: 4 (最後の値が返される)

// 理論和 (||) について
const resultD = "" || "foo";
const resultE = 0 || 2 || 0;
const resultF = "foo" || 4;

console.log(resultD); // 結果: "foo" (最初に真になった値が返される)
console.log(resultE); // 結果: 2 (最初に真になった値が返される)
console.log(resultF); // 結果： "foo" (最初に真になった値が返される)

### 非同期処理（Promise））