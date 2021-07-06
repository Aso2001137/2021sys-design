```uml
@startuml
entity "購入テーブル" as customer <d_purchase> {
+ order_id [PK]
--
order_id
customer_code
purchase_date
total_price
}

entity"購入テーブル詳細"as  customer <d_purchase_detail> {
+ detail_id,order_id [PK]
--
detail_id
order_id
item_code
price
num
}

entity"ユーザーテーブル"as  customer <m_customers>{
+ customer_code [PK]
--
customer_code
pass
name
address
tel
mail
del_flag
reg_date
}

entity"カテゴリテーブル"as  customer <m_category>{
+ category_id [PK]
--
category_id 
name
reg_date
}

entity"商品テーブル"as  customer <m_items>{
+ item_code [PK]
--
item_code
item_name
price
category_id
image
detail
del_flag
reg_date
}
@enduml
```
