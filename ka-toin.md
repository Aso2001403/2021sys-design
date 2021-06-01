```uml
@startuml
opt なし
 ユーザー -> webサーバー : カートの中クリック
 webサーバー -> DBサーバー : ユーザー登録
 DBサーバー -> DBサーバー : 登録処理
 DBサーバー -> webサーバー : 登録結果

 alt 詳細へ
 webサーバー -> ユーザー : 登録メッセージを表示
 else 削除
 webサーバー -> ユーザー : 失敗メッセージを表示
 end
end

@enduml
```
