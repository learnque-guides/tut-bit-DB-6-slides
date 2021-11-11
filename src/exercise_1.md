# Exercise 1

Execute code

```sql
DROP TABLE IF EXISTS dbo.Customers;

CREATE TABLE dbo.Customers
(
  custid      INT          NOT NULL PRIMARY KEY,
  companyname NVARCHAR(40) NOT NULL,
  country     NVARCHAR(15) NOT NULL,
  region      NVARCHAR(15) NULL,
  city        NVARCHAR(15) NOT NULL
);
```

Insert into the dbo.Customers table a row with the following information:

* custid: 100
* companyname: Coho Winery
* country: USA
* region: WA
* city: Redmond