# Sequence

* T-SQL supports the standard sequence object as an alternative key-generating mechanism for identity.
* One of the advantages of the sequence object is that, unlike identity, it’s not tied to a particular column in a particular table; rather, it’s an independent object in the database.

```sql
CREATE SEQUENCE [dbo].[SeqMaxOrderId] AS INT
  MINVALUE 1,
  MAXVALUE 10
  CYCLE; -- Reset to min value after max value reached
```

Also supports altering

```sql
ALTER SEQUENCE dbo.SeqOrderIDs
  NO CYCLE;
```