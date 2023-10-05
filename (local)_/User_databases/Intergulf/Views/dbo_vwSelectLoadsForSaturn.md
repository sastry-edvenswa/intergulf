#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLoadsForSaturn

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLoadsForSaturn]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 9:46:26 PM Tuesday, March 29, 2022 |
| Last Modified | 10:20:02 AM Friday, April 1, 2022 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| Generator | varchar(100) | 100 |
| Customer | varchar(100) | 100 |
| DriverId | bigint | 8 |
| FirstName | varchar(50) | 50 |
| LastName | varchar(50) | 50 |
| ScheduledDate | datetime | 8 |
| ScheduledTime | datetime | 8 |
| Destination | nvarchar(100) | 200 |
| DispatchStatus | varchar(50) | 50 |
| AccountingAction | varchar(40) | 40 |
| AccountingStatus | varchar(40) | 40 |
| CustomerPoNumber | varchar(50) | 50 |
| CustomerPoNumberExpirationDate | date | 3 |
| ContractNumber | varchar(50) | 50 |
| TankNumber | varchar(50) | 50 |
| DeliveryReleaseNumber | varchar(50) | 50 |
| LabTestId | bigint | 8 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectLoadsForSaturn]
AS
SELECT        dbo.Loads.Id, dbo.Generator.Name AS Generator, dbo.Customer.Name AS Customer, dbo.Driver.DriverId, dbo.Driver.FirstName, dbo.Driver.LastName, dbo.Loads.ScheduledDate, dbo.Loads.ScheduledTime, 
                         dbo.Destination.Name AS Destination, dbo.Loads.DispatchStatus, dbo.Loads.AccountingAction, dbo.Loads.AccountingStatus, dbo.Loads.CustomerPoNumber, dbo.Loads.CustomerPoNumberExpirationDate, 
                         dbo.Loads.ContractNumber, dbo.Loads.TankNumber, dbo.Loads.DeliveryReleaseNumber, dbo.Loads.LabTestId
FROM            dbo.Destination RIGHT OUTER JOIN
                         dbo.Loads LEFT OUTER JOIN
                         dbo.Customer ON dbo.Loads.CustomerId = dbo.Customer.Id ON dbo.Destination.Id = dbo.Loads.DestinationId LEFT OUTER JOIN
                         dbo.Profile LEFT OUTER JOIN
                         dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id ON dbo.Loads.ProfileId = dbo.Profile.Id LEFT OUTER JOIN
                         dbo.Driver ON dbo.Loads.DriverId = dbo.Driver.Id
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Customer]](../Tables/dbo_Customer.md)
* [[dbo].[Destination]](../Tables/dbo_Destination.md)
* [[dbo].[Driver]](../Tables/dbo_Driver.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

