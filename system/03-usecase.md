利用される際には ``\`uml 〜 ``` で囲んでください。

```
left to right direction
actor ゲスト as g <<レビューする>>
note right of g : お客様
package スタッフ {
  actor シェフ as c <<レビューされる>>
  actor 給仕係 as fc <<レビューされる>>
}
package レストラン {
  usecase 食事を食べる as UC1
  usecase 支払う as UC2
  usecase 飲む as UC3
  usecase レビューする as UC4
  usecase お金を受け取る as UC5
  usecase 給仕する as UC6
  usecase 料理を作る as UC7
}

note right of UC4 : 後で行う

g ..> UC5
g --> UC1
g --> UC2
g --> UC3
fc --> UC6
c --> UC7
UC5 --> fc
```