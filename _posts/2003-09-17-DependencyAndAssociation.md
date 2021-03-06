---
title: 依存と関連
tags: [uml]
---

http://www.martinfowler.com/bliki/DependencyAndAssociation.html

### 「依存」と「関連」の違いは？

一般に「関連」はクラス内のフィールドのようなものを表す際に用いられる。連携は常に存在していて、顧客（クライアント側？）の要求をいつでも頼むことができる。インターフェイスの見地からモデリングをした場合、フィールドの存在は必要ではない。単に要求の顧客（顧客の要求？）を返すメソッドがあるということを意味することもできる。

『[UML Distilled ３版](http://www.amazon.com/exec/obidos/tg/detail/-/0321193687)』（発刊されたばかり）から引用する。「ある要素の定義を変更したときに（供給側）、もうひとつの要素を変更する必要があるならば（クライアント側）、「依存」はその2つの要素間に存在する」これは非常にあいまいで、一般的な関連である。UMLには異なった形に「依存」を指すステレオタイプがあるからだ。コーディングの上では、パラメータの型を命名したり一時変数内にオブジェクトを作ったりすることは、「依存」を意味する。

UML図にすべての「依存」を表したくないだろう（多すぎる）。精選する必要があるし、コミュニケートする上で重要なものをのみ表す必要がある。私は「依存」にステレオタイプを用いることはあまりしない。ほとんどの場合、私が表したいキーポイントは、「依存」が存在しているということである。その種類はあまり重要ではない。

「関連」も「依存」を表す。2つのクラス間に「関連」があれば、そこには「依存」もある。「依存」を拡張線であらわすという場面を想像できない。「関連」は「汎化」がそうであるように「依存」を表す。

混乱の原因のひとつは、UML 1 での一時リンクの利用である。これらはUML 1 におけるメタモデルの問題に帰すべきである。これらはパラメータなどの関連のステレオタイプとして記されている。私はいつもこれらの関連を外してきた。なぜならパラメータスロットとメソッドの文脈内に存在する関連との違いのほうがよっぽど大事だと思ったからだ。毛かとして、そのような依存につくステレオタイプを関連よりも好んで使うようにしている。UML 2 ではもうこの問題は起きない。メタモデルはメソッドのスコープの関連を操作するのに他の方法を持つからだ。そのようなステレオタイプはUML 2 ではもはやValidではない。
