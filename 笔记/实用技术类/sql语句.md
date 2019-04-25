#SQL语句学习笔记
##联合查询
1. 联合查询分类
   + 内连接：inner Join 或 Join  
     >内连接仅显示两个表中匹配行，即两表中都有才显示示例：。
     ><div>
     select A.id AS AID,<br/>
            B.id AS BID <br/>
     from A INNER JOIN B ON (A.id=B.id)     
     </div>

   + 外链接：outer Join
      + 左外链接：left outer Join 或 left Join
        >左外连接：左表有就显示，不论右表。
      + 右外连接：right outer Join 或 right Join
        >右外连接：右表有就显示，不论左表。
      + 全外链接：full outer Join 或 full Join
        >全外连接：左表/右表，有一个有就显示
   + 交叉连接：cross Join
        >交叉连接是对A\B量表进行笛卡尔积的结果查询出来，即A的每条记录都有和B中所有记录相对应的信息。
        > select * from A CROSS JOIN B;
   + 结果集连接：union 和 union all
        >SQL Union用于将多个select结果集进行合并。值得注意的是，UNION 内部的 SELECT 语句必须拥有相同数量的列。列也必须拥有相似的数据类型。同时，每条 SELECT 语句中的列的顺序必须相同。
        >SELECT * FROM A UNION SELECT * from B；
