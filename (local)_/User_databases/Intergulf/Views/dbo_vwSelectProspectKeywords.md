#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectProspectKeywords

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectProspectKeywords]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 4:41:11 PM Saturday, June 6, 2015 |
| Last Modified | 4:41:11 PM Saturday, June 6, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| KeyWord | varchar(255) | 255 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectProspectKeywords]
AS
SELECT     TOP (100) PERCENT KeyWord
FROM         dbo.ProspectKeywords
ORDER BY KeyWord

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[ProspectKeywords]](../Tables/dbo_ProspectKeywords.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

