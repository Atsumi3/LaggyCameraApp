# LaggyCameraApp

Android12 で WebView上のカメラ映像表示がおかしくなる問題があったので、その検証アプリ

アプリサイズを小さくするためにJavaで最小構成で設定

## ダウンロード
[app-release.apk](https://github.com/Atsumi3/LaggyCameraApp/releases/download/1.0/app-release.apk)

## 検証用サイト
https://practice-75a12.web.app/

```js
import React, { Component } from 'react'
import {QrReader} from "react-qr-reader";

class App extends Component {
  render() {
    return (
      <div>
        <QrReader
          delay={100}
          style={{ width: '100%' }}
        />
      </div>
    )
  }
}
export default App;
```
