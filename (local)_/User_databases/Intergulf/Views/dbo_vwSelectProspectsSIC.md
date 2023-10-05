#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectProspectsSIC

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectProspectsSIC]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 10:17:31 PM Friday, January 8, 2010 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| SIC | varchar(10) | 10 |
| SICDescription | varchar(2000) | 2000 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectProspectsSIC]
AS
SELECT DISTINCT TOP 100 PERCENT SIC, SICDescription
FROM         dbo.Prospect
ORDER BY SICDescription

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Prospect]](../Tables/dbo_Prospect.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

