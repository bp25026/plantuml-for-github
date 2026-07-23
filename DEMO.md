# PlantUML for GitHub

## Sequence Diagram

```plantuml
@startuml
left to right direction

actor "一般来場者 / 学生" as Visitor
actor "企画参加団体" as Group
actor "実行委員会" as Admin

rectangle "大宮祭 現行Web/案内システム" {
  ' 来場者向け
  usecase "企画・タイムテーブルを閲覧する" as UC_View
  usecase "キャンパスマップを確認する" as UC_Map
  usecase "整理券・予約を取得する" as UC_Reserve
  usecase "混雑状況・お知らせを確認する" as UC_Notice

  ' 参加団体向け
  usecase "企画情報を登録・更新する" as UC_EditGroup
  usecase "物品・教室使用申請を行う" as UC_Apply

  ' 実行委員会向け
  usecase "企画申請を審査・承認する" as UC_Approve
  usecase "お知らせ・緊急連絡を配信する" as UC_Publish
  usecase "予約・集計データを確認する" as UC_Stats
}

' 関連（線）
Visitor -- UC_View
Visitor -- UC_Map
Visitor -- UC_Reserve
Visitor -- UC_Notice

Group -- UC_EditGroup
Group -- UC_Apply

Admin -- UC_Approve
Admin -- UC_Publish
Admin -- UC_Stats

' システム内での関連
UC_EditGroup ..> UC_Approve : <<申請>>
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
