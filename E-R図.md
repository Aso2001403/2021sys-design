```startuml
@startuml
Entity01 }|..|| Entity02
Entity03 }o..o| Entity04
Entity05 ||--o{ Entity06
Entity07 |o--|| Entity08
@enduml
```

```startuml
@startuml
entity "顧客マスタ" as customer <m_xustomers>
<<M,MASTER_MARK_COLOR>>{
  + customer_code[PK]
  --
  pass
  name
  address
  tel
  mail
  del_flag
  reg_date
}
@enduml
```
