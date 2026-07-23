# PlantUML for GitHub

## Sequence Diagram

```plantuml
@startuml
left to right direction

actor "来場者\n(SNSアカウント保持者)" as Visitor
actor "実行委員会" as Admin
actor "既存SNS\n(X / Instagram)" as ExternalSNS

rectangle "現行システム（SNSハッシュタグ投稿企画）" {
  usecase "公式ハッシュタグ(#大宮祭)を\n付けて投稿する" as UC_Post
  usecase "ハッシュタグ投稿を\n手動検索・目視確認する" as UC_Search
  usecase "投稿をリポスト・\n会場へ掲示する" as UC_Repost
}

Visitor -- UC_Post
UC_Post -- ExternalSNS

Admin -- UC_Search
UC_Search -- ExternalSNS

Admin -- UC_Repost
UC_Repost -- ExternalSNS

@enduml
```


## Class Diagram


```plantuml
@startuml
class Aaa {
    -bbb : int
    +ccc : string
    #aa : float
    +void addEntry(mmm : Entry)
    +int setFactory(ddd : string)
}
class Factory {
    #fff : string
}
class Entry {
    -yyy : int
}
class Parent {
}
Aaa *--> "1..100" Entry : -entries
Aaa o--> Factory : #factory
Aaa o--> Parent : +parent
@enduml
```
