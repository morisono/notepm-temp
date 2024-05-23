利用される際には ``\`uml 〜 ``` で囲んでください。

```
package ゼミ登録
package スケジュール
package 学生
package 教授
package 問い合わせ先
package Javaインフラストラクチャー

ゼミ登録 -[dashed]-> スケジュール
ゼミ登録 -[dashed]-> 学生
ゼミ登録 -[dashed]-> Javaインフラストラクチャー : <<import>>
ゼミ登録 -[dashed]-> 教授
教授 -[dashed]-> スケジュール
学生 -[dashed]-> 問い合わせ先
学生 -[dashed]-> Javaインフラストラクチャー : <<import>>
スケジュール -[dashed]-> Javaインフラストラクチャー : <<import>>
問い合わせ先 -[dashed]-> Javaインフラストラクチャー : <<import>>
教授 -[dashed]-> Javaインフラストラクチャー : <<import>>
```