#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectWashoutAllTables

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectWashoutAllTables]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 9:45:55 PM Wednesday, June 1, 2016 |
| Last Modified | 9:45:55 PM Wednesday, June 1, 2016 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| LoadId | bigint | 8 | 0 - 0 |
| WashOutRequired | varchar(50) | 50 |  |
| WashOutPerformed | varchar(50) | 50 |  |
| WashOut | varchar(50) | 50 |  |
| AddWashOut | bit | 1 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectWashoutAllTables]
AS
SELECT     dbo.Loads.Id AS LoadId, dbo.Loads.WashOutRequired, dbo.Loads.WashOutPerformed, dbo.LabTest.WashOut, dbo.LoadsBillingSummary.AddWashOut
FROM         dbo.Loads LEFT OUTER JOIN
                      dbo.LoadsBillingSummary ON dbo.Loads.Id = dbo.LoadsBillingSummary.LoadId LEFT OUTER JOIN
                      dbo.LabTest ON dbo.Loads.Id = dbo.LabTest.LoadId

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[LabTest]](../Tables/dbo_LabTest.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[LoadsBillingSummary]](../Tables/dbo_LoadsBillingSummary.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

