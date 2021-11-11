# The BULK INSERT statement

You use the BULK INSERT statement to insert into an existing table data originating from a file. 

```sql
BULK INSERT [schema].[SourceTable] FROM 'c:\temp\source.txt'
    WITH (
        DATAFILETYPE    = 'char',
        FIELDTERMINATOR = ',',
        ROWTERMINATOR   = '\n'
    );
```

* Create a simple Car table with type column as varchar, number column as varchar
* Create file cars.txt with conext like:

```
skoda,rlt111
toyouta,mnt233
honda,mrt123
```
* Upload data to your created table