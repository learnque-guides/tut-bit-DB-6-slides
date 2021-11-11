# Exercise 6

Run the following query against dbo.Customers, and notice that some rows have a NULL in the region column:

```sql
SELECT * FROM dbo.Customers;
```

The output from this query is as follows:

```sql
custid      companyname      country         region     city
----------- ---------------- --------------- ---------- ---------------
1           Customer NRZBB   Germany         NULL       Berlin
2           Customer MLTDN   Mexico          NULL       México D.F.
3           Customer KBUDE   Mexico          NULL       México D.F.
4           Customer HFBZG   UK              NULL       London
5           Customer HGVLZ   Sweden          NULL       Luleå
6           Customer XHXJV   Germany         NULL       Mannheim
7           Customer QXVLA   France          NULL       Strasbourg
8           Customer QUHWH   Spain           NULL       Madrid
9           Customer RTXGC   France          NULL       Marseille
10          Customer EEALV   Canada          BC         Tsawassen
...

(90 row(s) affected)
```

Update the dbo.Customers table, and change all NULL region values to <None>. Use the OUTPUT clause to show the custid, oldregion, and newregion:

Desired output:

```
custid      oldregion       newregion
----------- --------------- ---------------
1           NULL            <None>
2           NULL            <None>
3           NULL            <None>
4           NULL            <None>
5           NULL            <None>
6           NULL            <None>
7           NULL            <None>
8           NULL            <None>
9           NULL            <None>
11          NULL            <None>
12          NULL            <None>
13          NULL            <None>
14          NULL            <None>
16          NULL            <None>
17          NULL            <None>
18          NULL            <None>
19          NULL            <None>
20          NULL            <None>
23          NULL            <None>
24          NULL            <None>
25          NULL            <None>
26          NULL            <None>
27          NULL            <None>
28          NULL            <None>
29          NULL            <None>
30          NULL            <None>
39          NULL            <None>
40          NULL            <None>
41          NULL            <None>
44          NULL            <None>
49          NULL            <None>
50          NULL            <None>
52          NULL            <None>
53          NULL            <None>
54          NULL            <None>
56          NULL            <None>
58          NULL            <None>
59          NULL            <None>
60          NULL            <None>
63          NULL            <None>
64          NULL            <None>
66          NULL            <None>
68          NULL            <None>
69          NULL            <None>
70          NULL            <None>
72          NULL            <None>
73          NULL            <None>
74          NULL            <None>
76          NULL            <None>
79          NULL            <None>
80          NULL            <None>
83          NULL            <None>
84          NULL            <None>
85          NULL            <None>
86          NULL            <None>
87          NULL            <None>
90          NULL            <None>
91          NULL            <None>

(58 row(s) affected)
```