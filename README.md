# React ハンズオン 〜 Todo List チュートリアルよりも、もっと基礎から

React が今、シングル・ページ・アプリケーションの市場で、もっとも使われている技術であることは間違いありません。しかし、実際に React を書けるエンジニアはそう多くはないのか、React 案件の単価は非常に高いものとなっています。

おそらく React 習得が難しいのは、React それ自体ではなく、これに付随する開発環境の構築(Git, Node, Babel, Webpack)や、ES2015 のシンタックスといった広範な知識が必要となるからです。こういった技術に慣れ親しんでいない人は、React を学習する際に、一気にこれらを習得しなくてはいけないので、かなりのハードルとなります。

そこで今回は、環境の構築をせずともすぐに開発が可能なオンラインエディターである「[CodeSandBox](https://codesandbox.io/)」を用いることで、React だけに集中し、学習効率の良いハンズオンを目指します。Git, Node, Babel, Webpack を使ったことがない人でも、React アプリケーションの開発をすぐに始めることができます。

また、前提知識として要求され、あまり解説されない ES2015 のシンタックスについても重点的に解説をします。

例えば Arrow Functin

```javascript
const AddTwo = target => target + 2 
```

他にも 
1. {...arg} という引数の渡し方
2. ({arg1, arg2 }) という受け取り方
3. `${variable1} ${variable2}` という文字列結合

```javascript
import React from 'react'
import { render } from 'react-dom'

const FullName = ({ firstName, lastName }) => {
  const name = `${firstName} ${lastName}`
  return <h1>{name}</h1>
}

const name = {
  firstName: 'Yusuke',
  lastName: 'Nakanishi',
}

render(<FullName {...name} />, document.getElementById('root'))
```

Array.map などの比較的新しいメソッド

```javascript
const nameArray = ['Taka', 'Hiroshi', 'Youji']
const mrName = () => nameArray.map(name => `Mr.${name}`)
```
