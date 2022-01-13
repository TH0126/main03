# Firebaseを使った課題

## プロダクトの紹介

- 求人サイト的なものを作ってみました。
- 今回はシンプルにいきました。

## 工夫した点、こだわった点

- Whereを使って抽出条件機能を用意しました。
- ソート順もいくつか選べるようにしました。

## 苦戦した点、共有したいハマりポイントなど

- Whereは複数のフィールドを指定するとうまくいかないようで、複数の条件を指定して抽出は
- 現段階だと諦めました。。（複合インデックスを設定するとできるらしい？）
- WhereとorderByも上記といっしょの制限がある模様
- テストでWhereを使用した処理を何度か連続でやると、たまに、抽出結果が２レコードだけな
- のに同じデータが繰り返し、なぜかforEachで取得される現象が発生。（明細結果が２つでは
- なく３や４になる）
- デバックをしてみてもdataの取得件数（length）は間違ってなく、原因がわらなかったので
- if文でlength以上のforEach処理が走らないようにした。。