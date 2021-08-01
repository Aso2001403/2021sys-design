# DB定義書
## ER図
[ER図はこちら](https://github.com/Aso2001403/2021sys-design/blob/main/%E3%82%B5%E3%83%B3%E3%83%97%E3%83%AB%E3%82%B5%E3%82%A4%E3%83%88/%E7%AC%AC%EF%BC%92%EF%BC%93%E5%9B%9E%E3%83%AC%E3%83%9D%E3%83%BC%E3%83%88%EF%BC%88%E3%82%B5%E3%83%B3%E3%83%97%E3%83%AB%E3%82%B5%E3%82%A4%E3%83%88%E3%81%AEER%E5%9B%B3%EF%BC%89/ER%E5%9B%B3.md "ER図はこちら" ）

# DBテーブルカラム詳細一覧


### 顧客テーブル　（d_purchase）
|和名|項目名（カラム名）|型|PK|FK|NN|
|-----|-----|---|:---:|:---:|:---:|
|オーダーID|order_id|bigint(20)|○||○|
|顧客コード|customer_code|varchar(50)|||○|
|購入日|purchase_data|data|||○|
|総額|total_price|int(11)|||○|

### 購入詳細テーブル（d_purchase_detail）
|和名|項目名（カラム名）|型|PK|FK|NN|
|-----|-----|---|:---:|:---:|:---:|
|オーダー購入詳細ID|detail_id|bigint(20)|○||○|
|オーダーID|order_id|bigint(20)|○|○|○|
|商品コード|item_code|int(11)|||○|
|価格|price|int(11)|||○|
|数量|num|int(11)|||○|

### 顧客マスタ（m_customers）
|和名|項目名（カラム名）|型|PK|FK|NN|
|-----|-----|---|:---:|:---:|:---:|
|顧客コード|customer_code|varchar(50)|○||○|
|パスワード|pasu|varchar(50)|○|○|○|
|氏名|name|varchar(20)|||○|
|住所|address|varchar(100)|||○|
|電話番号|tel|varchar(20)|||○|
|メールアドレス|mail|varchar(100)|||○|
|削除フラグ|del_flag|int(1)||||
|登録日|reg_date|date|||○|

### カテゴリマスタ（m_category）
|和名|項目名（カラム名）|型|PK|FK|NN|
|-----|-----|---|:---:|:---:|:---:|
|カテゴリID|category_id|int(11)|○||○|
|カテゴリ名|name|varchar(20)|||○|
|登録日|reg_date|date|||○|


### 商品マスタ（m_items）
|和名|項目名（カラム名）|型|PK|FK|NN|
|-----|-----|---|:---:|:---:|:---:|
|商品コード|item_code|int(11)|○||○|
|商品名|item_name|varchar(50)|||○|
|価格|price|int(11)|||○|
|カテゴリID|category_id|int(11)||○|○|
|画像ファイル名|image|varchar(200)|||○|
|商品詳細説明|detail|varchar(500)||||
|削除フラグ|del_flag|int(11)||||
|登録日|reg_date|date|||○|
