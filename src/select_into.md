# The SELECT INTO statement

* The SELECT INTO statement is a nonstandard (not a part of ISO and ANSI SQL standart) T-SQL statement that creates a target table and populates it with the result set of a query.

```sql
SELECT [Column1], [Column2]
    INTO [SchemaName].[ToTableName]
    FROM [SchemaName].[FromTableName];
```

Think about SELECT INTO like a `copy paste`

The target table’s structure and data are based on the source table. The SELECT INTO statement copies from the source the base structure (such as column names, types, nullability, and identity property) and the data. It does not copy from the source constraints, indexes, triggers and ect.