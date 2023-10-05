#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectTanksForSaturn

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectTanksForSaturn]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 4:26:47 PM Thursday, December 15, 2022 |
| Last Modified | 4:26:47 PM Thursday, December 15, 2022 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Description | varchar(50) | 50 |
| Location | varchar(50) | 50 |
| TrackInventory | varchar(3) | 3 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectTanksForSaturn]
AS
SELECT        Description, Location, TrackInventory
FROM            dbo.Tanks
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Tanks]](../Tables/dbo_Tanks.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

