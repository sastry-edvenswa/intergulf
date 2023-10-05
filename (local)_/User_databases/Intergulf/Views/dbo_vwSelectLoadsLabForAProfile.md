#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLoadsLabForAProfile

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLoadsLabForAProfile]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 9:33:09 PM Saturday, August 19, 2017 |
| Last Modified | 9:33:09 PM Saturday, August 19, 2017 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| SalesPersonId | varchar(50) | 50 |
| ScheduledDate | datetime | 8 |
| ProfileNumber | varchar(50) | 50 |
| DocumentNumber | varchar(50) | 50 |
| Quantity | decimal(18,0) | 9 |
| AqueousPH | decimal(18,1) | 9 |
| AqueousAmmonia | decimal(18,0) | 9 |
| Status | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectLoadsLabForAProfile]
AS
SELECT        TOP (100) PERCENT dbo.Loads.Id, dbo.Loads.SalesPersonId, dbo.Loads.ScheduledDate, dbo.Profile.ProfileNumber, dbo.LabTest.DocumentNumber, 
                         dbo.LabTest.Quantity, dbo.LabTest.AqueousPH, dbo.LabTest.AqueousAmmonia, dbo.LabTest.Status
FROM            dbo.Loads LEFT OUTER JOIN
                         dbo.LabTest ON dbo.Loads.LabTestId = dbo.LabTest.Id LEFT OUTER JOIN
                         dbo.Profile ON dbo.Loads.ProfileId = dbo.Profile.Id
WHERE        (dbo.Loads.ScheduledDate >= CONVERT(DATETIME, '2016-01-01 00:00:00', 102) AND dbo.Loads.ScheduledDate <= CONVERT(DATETIME, '2017-12-31 00:00:00', 
                         102)) AND (dbo.Profile.ProfileNumber = '04795')
ORDER BY dbo.Loads.ScheduledDate

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

