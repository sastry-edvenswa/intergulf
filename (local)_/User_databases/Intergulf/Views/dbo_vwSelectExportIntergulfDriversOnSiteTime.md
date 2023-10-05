#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectExportIntergulfDriversOnSiteTime

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectExportIntergulfDriversOnSiteTime]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 3:24:39 PM Monday, November 27, 2017 |
| Last Modified | 3:24:39 PM Monday, November 27, 2017 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| ScheduledDate | datetime | 8 |
| TruckId | varchar(50) | 50 |
| Id | bigint | 8 |
| GeneratorName | varchar(100) | 100 |
| Destination | nvarchar(100) | 200 |
| DispatchStatus | varchar(50) | 50 |
| BillingStatus | varchar(50) | 50 |
| TransporterName | varchar(50) | 50 |
| ProfileId | bigint | 8 |
| GeneratorId | bigint | 8 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectExportIntergulfDriversOnSiteTime]
AS
SELECT        TOP (100) PERCENT dbo.Loads.ScheduledDate, dbo.Loads.TruckId, dbo.Loads.Id, dbo.Generator.Name AS GeneratorName, dbo.Destination.Name AS Destination, 
                         dbo.Loads.DispatchStatus, dbo.LoadsBillingSummary.BillingStatus, dbo.Transporter.Name AS TransporterName, dbo.Loads.ProfileId, dbo.Profile.GeneratorId
FROM            dbo.Transporter RIGHT OUTER JOIN
                         dbo.Profile INNER JOIN
                         dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id RIGHT OUTER JOIN
                         dbo.Loads ON dbo.Profile.Id = dbo.Loads.ProfileId ON dbo.Transporter.Id = dbo.Loads.TransporterId LEFT OUTER JOIN
                         dbo.LoadsBillingSummary ON dbo.Loads.Id = dbo.LoadsBillingSummary.LoadId LEFT OUTER JOIN
                         dbo.Destination ON dbo.Loads.DestinationId = dbo.Destination.Id
WHERE        (dbo.Transporter.Name = 'Intergulf Corporation') AND (dbo.Loads.DispatchStatus = 'Complete') AND (dbo.LoadsBillingSummary.BillingStatus = 'Complete')
ORDER BY Destination, dbo.Loads.ScheduledDate, dbo.Loads.TruckId

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Destination]](../Tables/dbo_Destination.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[LoadsBillingSummary]](../Tables/dbo_LoadsBillingSummary.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[Transporter]](../Tables/dbo_Transporter.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

