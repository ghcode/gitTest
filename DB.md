### sql执行顺序

```
FROM <left_table>
ON <join_condition>
<join_type> JOIN <right_table>
WHERE <where_condition>
GROUP BY <group_by_list>  --group by 中出现的列必须在select 中，有参数可以控制（系统变量sql_mode中的ONLY_FULL_GROUP_BY去掉），没有在group by 中的列需使用聚会函数

HAVING <having_condition>  -- 只作用后的聚合数据
SELECT 
DISTINCT <select_list>  --会生成临时表，生成唯一索引
ORDER BY <order_by_condition>  --可以使用字段别名
LIMIT <limit_number>
```

