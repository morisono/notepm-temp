利用される際には ``\`uml 〜 ``` で囲んでください。

```
component クライアント {
  component Webブラウザ
}
component Webサーバー {
  component nginx
}
component アプリケーションサーバー1 {
  component Docker1 {
    component Railsアプリケーション1
  }
}
component アプリケーションサーバー2 {
  component Docker2 {
    component Railsアプリケーション2
  }
}
component データベースサーバー {
  component Ubuntu {
    database MySQL
  }
}

Webブラウザ--nginx: n TCP/IP 1
nginx--Railsアプリケーション1
nginx--Railsアプリケーション2
Railsアプリケーション1--MySQL
Railsアプリケーション2--MySQL
```