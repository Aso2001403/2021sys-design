# DB定義書
## ER図
[ER図はこちら](https://github.com/Aso2001403/2021sys-design/blob/main/%E3%82%B5%E3%83%B3%E3%83%97%E3%83%AB%E3%82%B5%E3%82%A4%E3%83%88/%E7%AC%AC%EF%BC%92%EF%BC%93%E5%9B%9E%E3%83%AC%E3%83%9D%E3%83%BC%E3%83%88%EF%BC%88%E3%82%B5%E3%83%B3%E3%83%97%E3%83%AB%E3%82%B5%E3%82%A4%E3%83%88%E3%81%AEER%E5%9B%B3%EF%BC%89/ER%E5%9B%B3.md "ER図はこちら" ）

# DBテーブルカラム詳細一覧

# データベース詳細

d_purchase
|項目名|型|PK|FK|NN|
|-----|--|--|--|--|
|order_id|bigint(20)|○||○|
|customer_code|varchar(50)|||○|
|purchase_data|data|||○|
|total_price|int(11)|||○|

d_purchase_detail
|項目名|型|PK|FK|NN|
|-----|--|--|--|--|
|detail_id|bigint(20)|○||○|
|order_id|bigint(20)|○|○|○|
|item_code|int(11)|||○|
|price|int(11)|||○|
|num|int(11)|||○|

m_customers
|項目名|型|PK|FK|NN|
|-----|--|--|--|--|
|customer_code|varchar(50)|○||○|
|pasu|varchar(50)|○|○|○|
|name|varchar(20)|||○|
|address|varchar(100)|||○|
|tel|varchar(20)|||○|
|mail|varchar(100)|||○|
|del_flag|int(1)||||
|reg_date|date|||○|

m_category
|項目名|型|PK|FK|NN|
|-----|--|--|--|--|
|category_id|int(11)|○||○|
|name|varchar(20)|||○|
|reg_date|date|||○|


m_items
|項目名|型|PK|FK|NN|
|-----|--|--|--|--|
|item_code|int(11)|○||○|
|item_name|varchar(50)|||○|
|price|int(11)|||○|
|category_id|int(11)||○|○|
|image|varchar(200)|||○|
|detail|varchar(500)||||
|del_flag|int(11)||||
|reg_date|date|||○|
