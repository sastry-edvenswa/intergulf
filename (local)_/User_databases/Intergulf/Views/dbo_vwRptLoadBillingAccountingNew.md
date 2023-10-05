#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwRptLoadBillingAccountingNew

# ![Views](../../../../Images/View32.png) [dbo].[vwRptLoadBillingAccountingNew]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 4:12:31 PM Monday, February 4, 2013 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| ScheduledDate | datetime | 8 |
| TruckId | varchar(50) | 50 |
| Generator Name | varchar(100) | 100 |
| VesselTank | varchar(100) | 100 |
| BillingTime | numeric(18,2) | 9 |
| BillingRate | numeric(18,0) | 9 |
| BillingDepartment | varchar(50) | 50 |
| BillingStatus | varchar(50) | 50 |
| Accountingnotes | varchar(3000) | 3000 |
| UserName | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwRptLoadBillingAccountingNew]
AS
SELECT     TOP 100 PERCENT dbo.Loads.Id, dbo.Loads.ScheduledDate, dbo.Loads.TruckId, dbo.Generator.Name AS [Generator Name], dbo.Loads.VesselTank, 
                      dbo.LoadsBillingSummary.BillingTime, dbo.LoadsBillingSummary.BillingRate, dbo.LoadsBillingSummary.BillingDepartment, 
                      dbo.LoadsBillingSummary.BillingStatus, dbo.Loads.Accountingnotes, dbo.UserMaster.UserName
FROM         dbo.LoadsBillingSummary RIGHT OUTER JOIN
                      dbo.Loads ON dbo.LoadsBillingSummary.LoadId = dbo.Loads.Id LEFT OUTER JOIN
                      dbo.UserMaster RIGHT OUTER JOIN
                      dbo.Profile ON dbo.UserMaster.UserName = dbo.Profile.SalesPersonId LEFT OUTER JOIN
                      dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id ON dbo.Loads.ProfileId = dbo.Profile.Id
ORDER BY dbo.Loads.BillingDepartment, dbo.Loads.ScheduledDate, dbo.Loads.Id

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[LoadsBillingSummary]](../Tables/dbo_LoadsBillingSummary.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[UserMaster]](../Tables/dbo_UserMaster.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

