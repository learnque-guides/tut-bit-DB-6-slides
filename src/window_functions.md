# Window functions

A window function is a function that, for each row, computes a scalar result value based on a calculation against a subset of the rows from the underlying query.

```sql
SELECT empid, ordermonth, val,
  SUM(val) OVER(PARTITION BY empid
                ORDER BY ordermonth) AS runval
FROM Sales.EmpOrders;
```

```sql
SELECT empid, ordermonth, val, SUM(val), AVG(val)
FROM Sales.EmpOrders
GROUP BY empid, ordermonth, val
ORDER BY ordermonth;
```

One of the great advantages of window functions is that they don’t hide the detail. This means you can write expressions that mix detail and aggregates. The next example demonstrates this:

```sql
SELECT orderid, custid, val,
  100 * val / SUM(val) OVER() AS pctall,
  100 * val / SUM(val) OVER(PARTITION BY custid) AS pctcust
FROM Sales.OrderValues;
```

More details: 
[https://www.sqlshack.com/sql-partition-by-clause-overview/](https://www.sqlshack.com/sql-partition-by-clause-overview/)
