#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLastLoadInformation

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLastLoadInformation]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 9:37:14 PM Monday, October 22, 2012 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| ProfileId | bigint | 8 |
| HandlingCode | varchar(10) | 10 |
| GCApprovalDate | datetime | 8 |
| Last Date | datetime | 8 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectLastLoadInformation]
AS
SELECT     TOP 100 PERCENT dbo.Loads.Id, dbo.Loads.ProfileId, dbo.LabTest.HandlingCode, dbo.Profile.GCApprovalDate, MAX(dbo.Loads.ScheduledDate) 
                      AS [Last Date]
FROM         dbo.Loads INNER JOIN
                      dbo.Profile ON dbo.Loads.ProfileId = dbo.Profile.Id LEFT OUTER JOIN
                      dbo.LabTest ON dbo.Loads.LabTestId = dbo.LabTest.Id
GROUP BY dbo.Loads.ProfileId, dbo.LabTest.HandlingCode, dbo.Profile.GCApprovalDate, dbo.Loads.Id
ORDER BY MAX(dbo.Loads.ScheduledDate) DESC

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[LabTest]](../Tables/dbo_LabTest.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

