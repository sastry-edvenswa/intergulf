#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectProfileOneTimeOnly

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectProfileOneTimeOnly]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 3:12:45 PM Friday, January 31, 2014 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| LoadFrequency | varchar(50) | 50 |
| CreateDate | datetime | 8 |
| Days Old | int | 4 |
| Status | varchar(20) | 20 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectProfileOneTimeOnly]
AS
SELECT     LoadFrequency, CreateDate, DATEDIFF([DAY], CreateDate, GETDATE()) AS [Days Old], Status
FROM         dbo.Profile
WHERE     (Status = 'Active') AND (LoadFrequency = 'One Time') AND (DATEDIFF([DAY], CreateDate, GETDATE()) > 180)

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

