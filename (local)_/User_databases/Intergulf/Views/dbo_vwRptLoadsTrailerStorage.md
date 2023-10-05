#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwRptLoadsTrailerStorage

# ![Views](../../../../Images/View32.png) [dbo].[vwRptLoadsTrailerStorage]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 11:01:28 PM Monday, May 6, 2013 |
| Last Modified | 10:43:12 PM Monday, June 26, 2017 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| LoadId | bigint | 8 |
| TrailerId | varchar(50) | 50 |
| GeneratorName | varchar(100) | 100 |
| CustomerName | varchar(50) | 50 |
| MaterialDescription | varchar(3000) | 3000 |
| ScheduledDate | datetime | 8 |
| DispatchStatus | varchar(50) | 50 |
| BillingStatus | varchar(50) | 50 |
| BillingDepartment | varchar(50) | 50 |
| StartDate | datetime | 8 |
| EndDate | datetime | 8 |
| Days | int | 4 |
| UserName | varchar(50) | 50 |
| SalesPersonId | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwRptLoadsTrailerStorage]
AS
SELECT        TOP (100) PERCENT dbo.LoadsTrailerStorageReport.LoadId, dbo.LoadsTrailerStorageReport.TrailerId, dbo.Generator.Name AS GeneratorName, 
                         dbo.Customer.Name AS CustomerName, dbo.Profile.MaterialDescription, dbo.Loads.ScheduledDate, dbo.Loads.DispatchStatus, 
                         dbo.LoadsBillingSummary.BillingStatus, dbo.LoadsBillingSummary.BillingDepartment, dbo.LoadsTrailerStorageReport.StartDate, 
                         dbo.LoadsTrailerStorageReport.EndDate, DATEDIFF(DAY, dbo.LoadsTrailerStorageReport.StartDate, dbo.LoadsTrailerStorageReport.EndDate) AS Days, 
                         dbo.LoadsTrailerStorageReport.UserName, dbo.Loads.SalesPersonId
FROM            dbo.LoadsTrailerStorageReport LEFT OUTER JOIN
                         dbo.LoadsBillingSummary ON dbo.LoadsTrailerStorageReport.LoadId = dbo.LoadsBillingSummary.LoadId LEFT OUTER JOIN
                         dbo.Loads LEFT OUTER JOIN
                         dbo.Customer ON dbo.Loads.CustomerId = dbo.Customer.Id LEFT OUTER JOIN
                         dbo.Profile LEFT OUTER JOIN
                         dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id ON dbo.Loads.ProfileId = dbo.Profile.Id ON 
                         dbo.LoadsTrailerStorageReport.LoadId = dbo.Loads.Id
WHERE        (NOT (dbo.LoadsBillingSummary.BillingStatus = 'Canceled'))
ORDER BY dbo.Loads.ScheduledDate

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Customer]](../Tables/dbo_Customer.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[LoadsBillingSummary]](../Tables/dbo_LoadsBillingSummary.md)
* [[dbo].[LoadsTrailerStorageReport]](../Tables/dbo_LoadsTrailerStorageReport.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

