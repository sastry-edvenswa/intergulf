#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectSaturnTransactionsLoads

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectSaturnTransactionsLoads]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 4:58:36 PM Tuesday, July 18, 2023 |
| Last Modified | 4:58:36 PM Tuesday, July 18, 2023 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| ScheduledDate | datetime | 8 |
| LabTestId | bigint | 8 |
| TrackInventory | varchar(3) | 3 |
| ContractNumber | varchar(50) | 50 |
| ProfileNumber | varchar(50) | 50 |
| Profile Contract | varchar(20) | 20 |
| Product | varchar(20) | 20 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectSaturnTransactionsLoads]
AS
SELECT        dbo.Loads.Id, dbo.Loads.ScheduledDate, dbo.Loads.LabTestId, dbo.Tanks.TrackInventory, dbo.Loads.ContractNumber, dbo.Profile.ProfileNumber, dbo.Profile.ContractNumber AS [Profile Contract], 
                         dbo.Profile.Product
FROM            dbo.Profile RIGHT OUTER JOIN
                         dbo.Loads ON dbo.Profile.Id = dbo.Loads.ProfileId LEFT OUTER JOIN
                         dbo.LabTestDisbursement LEFT OUTER JOIN
                         dbo.Tanks ON dbo.LabTestDisbursement.Tank = dbo.Tanks.Description RIGHT OUTER JOIN
                         dbo.LabTest ON dbo.LabTestDisbursement.LabTestId = dbo.LabTest.Id ON dbo.Loads.LabTestId = dbo.LabTest.Id
WHERE        (dbo.Tanks.TrackInventory = 'Yes') AND (dbo.Loads.ScheduledDate >= CONVERT(DATETIME, '2023-04-01 00:00:00', 102)) AND (dbo.Loads.ContractNumber = '0000-0000')
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[LabTest]](../Tables/dbo_LabTest.md)
* [[dbo].[LabTestDisbursement]](../Tables/dbo_LabTestDisbursement.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[Tanks]](../Tables/dbo_Tanks.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

