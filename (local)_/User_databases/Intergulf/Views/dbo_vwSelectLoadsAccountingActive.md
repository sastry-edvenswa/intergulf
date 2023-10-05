#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLoadsAccountingActive

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLoadsAccountingActive]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 10:44:37 PM Friday, August 12, 2011 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| ScheduledDate | datetime | 8 |
| Id | bigint | 8 |
| GeneratorName | varchar(100) | 100 |
| VesselTank | varchar(100) | 100 |
| Destination | nvarchar(100) | 200 |
| DispatchStatus | varchar(50) | 50 |
| AccountingStatus | varchar(40) | 40 |
| AccountingAction | varchar(40) | 40 |
| Accountingnotes | varchar(3000) | 3000 |
| BillingDepartment | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectLoadsAccountingActive]
AS
SELECT     TOP 100 PERCENT fnSelectLoads.ScheduledDate, fnSelectLoads.Id, fnSelectGenerator.Name AS GeneratorName, fnSelectLoads.VesselTank, 
                      fnSelectDestination.Name AS Destination, fnSelectLoads.DispatchStatus, fnSelectLoads.AccountingStatus, fnSelectLoads.AccountingAction, 
                      fnSelectLoads.Accountingnotes, fnSelectLoads.BillingDepartment
FROM         dbo.fnSelectDestination() fnSelectDestination RIGHT OUTER JOIN
                      dbo.fnSelectLoads() fnSelectLoads ON fnSelectDestination.Id = fnSelectLoads.DestinationId LEFT OUTER JOIN
                      dbo.fnSelectGenerator() fnSelectGenerator INNER JOIN
                      dbo.fnSelectProfile() fnSelectProfile ON fnSelectGenerator.Id = fnSelectProfile.GeneratorId ON fnSelectLoads.ProfileId = fnSelectProfile.Id
ORDER BY fnSelectLoads.ScheduledDate, fnSelectLoads.Id

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[fnSelectDestination]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectDestination.md)
* [[dbo].[fnSelectGenerator]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectGenerator.md)
* [[dbo].[fnSelectLoads]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectLoads.md)
* [[dbo].[fnSelectProfile]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectProfile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

