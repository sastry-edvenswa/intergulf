#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectExportLoadsForEBETemp

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectExportLoadsForEBETemp]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 9:17:47 PM Thursday, May 9, 2019 |
| Last Modified | 10:47:09 AM Monday, May 13, 2019 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Load No | bigint | 8 |
| Generator | varchar(100) | 100 |
| Customer | varchar(50) | 50 |
| SageCustomerNumber | varchar(20) | 20 |
| ProfileNumber | varchar(50) | 50 |
| ScheduledDate | datetime | 8 |
| DocumentType | varchar(50) | 50 |
| Document No | varchar(50) | 50 |
| Driver Name | varchar(101) | 101 |
| TruckId | varchar(50) | 50 |
| TrailerId | varchar(50) | 50 |
| Destination | nvarchar(100) | 200 |
| Facility | varchar(50) | 50 |
| BillingDepartment | varchar(50) | 50 |
| SalesPersonId | varchar(50) | 50 |
| DeliveryReleaseNumber | varchar(50) | 50 |
| DestinationId | bigint | 8 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectExportLoadsForEBETemp]
AS
SELECT        dbo.Loads.Id AS [Load No], dbo.Generator.Name AS Generator, dbo.Customer.Name AS Customer, dbo.Customer.SageCustomerNumber, dbo.Profile.ProfileNumber, dbo.Loads.ScheduledDate, 
                         dbo.Profile.DocumentType, dbo.LabTest.DocumentNumber AS [Document No], LTRIM(RTRIM(dbo.Driver.FirstName)) + ' ' + LTRIM(RTRIM(dbo.Driver.LastName)) AS [Driver Name], dbo.Loads.TruckId, 
                         dbo.Loads.TrailerId, dbo.Destination.Name AS Destination, dbo.Generator.Facility, dbo.Loads.BillingDepartment, dbo.Loads.SalesPersonId, dbo.Loads.DeliveryReleaseNumber, dbo.Loads.DestinationId
FROM            dbo.Driver RIGHT OUTER JOIN
                         dbo.Loads ON dbo.Driver.Id = dbo.Loads.DriverId LEFT OUTER JOIN
                         dbo.Customer ON dbo.Loads.CustomerId = dbo.Customer.Id LEFT OUTER JOIN
                         dbo.Destination ON dbo.Loads.DestinationId = dbo.Destination.Id LEFT OUTER JOIN
                         dbo.LabTest ON dbo.Loads.LabTestId = dbo.LabTest.Id LEFT OUTER JOIN
                         dbo.Generator RIGHT OUTER JOIN
                         dbo.Profile ON dbo.Generator.Id = dbo.Profile.GeneratorId ON dbo.Loads.ProfileId = dbo.Profile.Id
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Customer]](../Tables/dbo_Customer.md)
* [[dbo].[Destination]](../Tables/dbo_Destination.md)
* [[dbo].[Driver]](../Tables/dbo_Driver.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[LabTest]](../Tables/dbo_LabTest.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

