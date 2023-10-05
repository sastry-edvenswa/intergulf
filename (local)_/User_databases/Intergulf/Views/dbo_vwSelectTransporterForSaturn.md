#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectTransporterForSaturn

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectTransporterForSaturn]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 4:35:37 PM Thursday, December 15, 2022 |
| Last Modified | 4:35:37 PM Thursday, December 15, 2022 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | numeric(19,0) | 9 |
| Name | varchar(100) | 100 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectTransporterForSaturn]
AS
SELECT        TOP (100) PERCENT Id, Name
FROM            dbo.Transporter
ORDER BY Name
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Transporter]](../Tables/dbo_Transporter.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

