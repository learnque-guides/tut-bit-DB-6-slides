# Exercise 4

Delete from the dbo.Orders table orders that were placed before August 2014. Use the OUTPUT clause to return the orderid and orderdate values of the deleted orders:

Desired output:

```
orderid     orderdate
----------- -----------
10248       2014-07-04
10249       2014-07-05
10250       2014-07-08
10251       2014-07-08
10252       2014-07-09
10253       2014-07-10
10254       2014-07-11
10255       2014-07-12
10256       2014-07-15
10257       2014-07-16
10258       2014-07-17
10259       2014-07-18
10260       2014-07-19
10261       2014-07-19
10262       2014-07-22
10263       2014-07-23
10264       2014-07-24
10265       2014-07-25
10266       2014-07-26
10267       2014-07-29
10268       2014-07-30
10269       2014-07-31

(22 row(s) affected)
```