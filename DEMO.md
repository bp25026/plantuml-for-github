# PlantUML for GitHub

## Sequence Diagram

```plantuml
@startwbs
* デジタル寄せ書きシステム構築
** 1.0 要件・UI設計
*** 1.1 システム要件定義・仕様書作成
*** 1.2 UI/UXデザイン設計（投稿画面・画面演出）
*** 1.3 実行委協議・申請（設営場所・電源・回線）
** 2.0 システム開発
*** 2.1 フロントエンド開発（Webフォーム・大画面アニメーション）
*** 2.2 バックエンド・DB構築（データ保存・リアルタイム通信）
*** 2.3 モデレーション機能開発（自動NG辞書＋手動承認UI）
*** 2.4 フェイルセーフ機構開発（オフラインローカルキャッシュ）
** 3.0 モデレーション・テスト
*** 3.1 モデレーション機能テスト（検閲・承認フロー検証）
*** 3.2 負荷・通信テスト（軽量通信100KB以下・同時アクセス耐性）
*** 3.3 総合リハーサル（端末〜大型ビジョン疎通確認）
** 4.0 現地ネットワーク・スクリーン設営
*** 4.1 会場ネットワーク・回線確保（テザリング・予備回線）
*** 4.2 機材・スクリーン設営（再生PC・モニター接続設定）
*** 4.3 案内POP・QRコード掲示（ブース・会場各所設置）
** 5.0 当日運用
*** 5.1 当日モニタリング・リアルタイム検閲（ワンタップ承認）
*** 5.2 障害時対応・フェイルセーフ運用（オフライン表示切替）
*** 5.3 アーカイブ・振り返り（データ保存・引継ぎレポート作成）
@endwbs
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
