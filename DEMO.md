# PlantUML for GitHub

## Sequence Diagram

```plantuml
@startgantt
language ja
printscale weekly
Project starts 2026-08-03

-- 1.0 要件・UI設計 --
[1.1 システム要件定義・仕様書] as [T11] lasts 2 weeks
[1.2 UI/UXデザイン設計] as [T12] lasts 2 weeks
[1.3 実行委協議・申請] as [T13] lasts 3 weeks
[T12] starts at [T11]'s start
[T13] starts at [T11]'s end

-- 2.0 システム開発 --
[2.1 フロントエンド開発] as [T21] lasts 4 weeks
[2.2 バックエンド・DB構築] as [T22] lasts 4 weeks
[2.3 モデレーション機能開発] as [T23] lasts 2 weeks
[2.4 フェイルセーフ機構開発] as [T24] lasts 2 weeks
[T21] starts at [T11]'s end
[T22] starts at [T11]'s end
[T23] starts 2 weeks after [T22]'s start
[T24] starts at [T23]'s end

-- 3.0 モデレーション・テスト --
[3.1 モデレーション機能テスト] as [T31] lasts 1 week
[3.2 負荷・通信テスト] as [T32] lasts 1 week
[3.3 総合リハーサル] as [T33] lasts 1 week
[T31] starts at [T21]'s end
[T32] starts at [T31]'s end
[T33] starts at [T32]'s end

-- 4.0 現地ネットワーク・スクリーン設営 --
[4.1 ネットワーク・回線確保] as [T41] lasts 2 weeks
[4.2 機材・スクリーン設営] as [T42] lasts 3 days
[4.3 案内POP・QRコード掲示] as [T43] lasts 3 days
[T41] starts at [T32]'s end
[T42] starts at [T33]'s end
[T43] starts at [T42]'s start

-- 5.0 当日運用 --
[5.1 当日モニタリング・リアルタイム検閲] as [T51] lasts 2 days
[5.2 障害時対応・非常運用] as [T52] lasts 2 days
[5.3 アーカイブ・振り返り] as [T53] lasts 1 week
[T51] starts at [T42]'s end
[T52] starts at [T51]'s start
[T53] starts at [T51]'s end
@endgantt
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
