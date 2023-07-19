# Reactの学習記録

### 基礎知識
・JSX記法を用いて記述したものをJavaScriptのオブジェクトに変換する際、
Babelというソフトウェアを用いているので、読み込みが必要！


### renderメソッド、その他Reactの動き確認
`const appEl1 = document.querySelector("#app");`
`const root = ReactDOM.createRoot(appEl1);`
`root.render(<h1>Hello World</h1>);`
上記書き方は、React ver18以降に推奨されている書き方<br>
以前は、下記のようだったが、今は非推奨
`ReactDOM.render(<h1>Hello World</h1>, appEl1)`

## コンポーネント
・画面の各構成要素をReactで定義したもの

＜メリット＞
・再利用性の向上（コードが使いまわせる）
・可読性の向上（コードが整理される）
・疎結合になる（バグを減らせる）

コンポーネントはJavaScriptの関数として定義する
`function Welcome() { return (<h1>ようこそ！</h1>); // コンポーネントはJSXを返す }`
`<Welcome />`

☆ポイント
・関数名の最初の文字は必ず大文字で作成する（babelの決まり上、先頭が大文字でないと関数だと認識しない）

## インストール
npm i -g create-react-app

## create-react-appドキュメント
npm docs create-react-app

## プロジェクトの作成方法
create-react-app {フォルダ名}


## useStateについて
const [state, setState] = useState(initialState)
* state
    * 現在のstate
* setState
    * stateを更新するためのset関数
    * 引数は以下の２通り
        * 更新後のstate
        * 更新用関数
            * 引数に　直前のstateをとり、更新後のstateを返すコールバック関数
* initialState
    * stateの初期値

> 引用元：https://qiita.com/washogo/items/509c8d98d7b7f2c9b700


