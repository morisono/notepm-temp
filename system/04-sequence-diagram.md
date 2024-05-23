利用される際には ``\`uml 〜 ``` で囲んでください。

```
autonumber 10 10
actor Webブラウザ
activate サーバー
Webブラウザ -> サーバー: 認証リクエスト
database データベース as DB

alt 認証成功

    サーバー -> Webブラウザ: 認証成功

else 認証失敗

    サーバー -> Webブラウザ: 認証失敗
    deactivate サーバー
    group サーバー処理
      サーバー -> DB : 失敗回数記録
          loop 3回失敗
              サーバー -> DB: アカウントロック
          end
      サーバー -> Webブラウザ : アカウントロック通知
    end
    note right
      アカウントロックは連続3回認証
      失敗した場合に実行されます
    end note

else 他のシステムエラー

   サーバー -> Webブラウザ: 再度認証実行要求

end
```