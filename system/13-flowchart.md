利用される際には ``\`uml 〜 ``` で囲んでください。

```
start
:レジに向かう;
if (並んでいる？)
  :列の最後尾に並ぶ;
  :順番が来るのを待つ;
else (いいえ)
endif
:レジにカゴを置く;
repeat :カゴの商品を出す;
  fork
    :レジ打ちを待つ;
  fork again
    :バッグに入れる;
  end fork
repeat while (まだカゴに商品がある？)
if (1000円以下) then (はい)
  :現金決済;
  note left: 現金がなければQRコード決済
elseif (3万円以下) then (はい)
  :QRコード決済;
else (それ以上)
  :クレジットカード決済;
endif
:自宅に帰る;
stop
```