# clickhouse & mysql

clickhouse 支持SQL的语法。

clickhouse在后端进行操作（如，查询）的过程中与前端是发生交互的。

MYSQL完全是后端的数据库，在后端操作时与前端不发生交互。

UNION DISTINCT要求数据表必须字段相同，但是UNION ALL不需要

JOIN 需要修改表名，用法没有UNION ALL方便

GROUP BY的作用
https://www.w3school.com.cn/sql/sql_groupby.asp