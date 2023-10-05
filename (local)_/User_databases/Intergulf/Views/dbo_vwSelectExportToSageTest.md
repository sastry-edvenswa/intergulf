#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectExportToSageTest

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectExportToSageTest]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 9:39:37 PM Monday, April 12, 2021 |
| Last Modified | 9:40:05 PM Monday, April 12, 2021 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| ScheduledDate | datetime | 8 |
| SageCustomerNumber | varchar(20) | 20 |
| GeneratorName | varchar(100) | 100 |
| ProfileNumber | varchar(50) | 50 |
| DocumentNumber | varchar(50) | 50 |
| Notes | varchar(5000) | 5000 |
| SalesPersonId | varchar(50) | 50 |
| SageSalespersonCode | varchar(2) | 2 |
| Price | numeric(18,4) | 9 |
| Quantity | numeric(18,2) | 9 |
| Units | varchar(50) | 50 |
| TransPrice | numeric(18,4) | 9 |
| TransQuantity | numeric(18,2) | 9 |
| TransMethod | varchar(50) | 50 |
| SurchargePrice | numeric(18,4) | 9 |
| SurchargeQuantity | numeric(18,2) | 9 |
| AccountingStatus | varchar(40) | 40 |
| OwnerId | varchar(50) | 50 |
| PTFuelSerCharge | numeric(18,0) | 9 |
| BillingDepartment | varchar(50) | 50 |
| ServiceTypeId | varchar(2) | 2 |
| ServiceType | varchar(50) | 50 |
| WCEndIn | varchar(1) | 1 |
| AddFuelSurCharge | varchar(2) | 2 |
| CustomerPickupDelivery | varchar(3) | 3 |
| LenEPACode | int | 4 |
| SageCostCenter | varchar(5) | 5 |
| HTYes | varchar(50) | 50 |
| WasteCode | varchar(50) | 50 |
| ProfileType | varchar(50) | 50 |
| Direction | varchar(50) | 50 |
| EPAWasteCode1 | varchar(10) | 10 |
| EPAWasteCode2 | varchar(10) | 10 |
| EPAWasteCode3 | varchar(10) | 10 |
| EPAWasteCode4 | varchar(10) | 10 |
| ProfileId | bigint | 8 |
| ManifestFee | varchar(2) | 2 |
| CustomerPoNumber | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectExportToSageTest]
AS
SELECT        dbo.Loads.Id, dbo.Loads.ScheduledDate, dbo.Customer.SageCustomerNumber, dbo.Generator.Name AS GeneratorName, dbo.Profile.ProfileNumber, dbo.LabTest.DocumentNumber, dbo.LabTest.Notes, 
                         dbo.Loads.SalesPersonId, dbo.UserMaster.SageSalespersonCode, dbo.LoadsInvoice.Price, dbo.LoadsInvoice.Quantity, dbo.LoadsInvoice.Units, dbo.LoadsInvoice.TransPrice, dbo.LoadsInvoice.TransQuantity, 
                         dbo.LoadsInvoice.TransMethod, dbo.LoadsInvoice.SurchargePrice, dbo.LoadsInvoice.SurchargeQuantity, dbo.Loads.AccountingStatus, dbo.LoadsInvoice.OwnerId, dbo.Profile.PTFuelSerCharge, 
                         dbo.Loads.BillingDepartment, dbo.BillingDepartments.ServiceTypeId, dbo.ServiceTypes.ServiceType, RIGHT(dbo.Profile.WasteCode, 1) AS WCEndIn, dbo.LoadsInvoice.AddFuelSurCharge, 
                         dbo.Loads.CustomerPickupDelivery, LEN(dbo.Profile.EPAWasteCode1 + dbo.Profile.EPAWasteCode2 + dbo.Profile.EPAWasteCode3 + dbo.Profile.EPAWasteCode4) AS LenEPACode, 
                         dbo.BillingDepartments.SageCostCenter, dbo.Profile.HTYes, dbo.Profile.WasteCode, dbo.Profile.ProfileType, dbo.Profile.Direction, dbo.Profile.EPAWasteCode1, dbo.Profile.EPAWasteCode2, 
                         dbo.Profile.EPAWasteCode3, dbo.Profile.EPAWasteCode4, dbo.Profile.Id AS ProfileId, dbo.LoadsInvoice.ManifestFee, dbo.Loads.CustomerPoNumber
FROM            dbo.Loads LEFT OUTER JOIN
                         dbo.LoadsBillingSummary INNER JOIN
                         dbo.BillingDepartments ON dbo.LoadsBillingSummary.BillingDepartment = dbo.BillingDepartments.Description INNER JOIN
                         dbo.ServiceTypes ON dbo.BillingDepartments.ServiceTypeId = dbo.ServiceTypes.Id ON dbo.Loads.Id = dbo.LoadsBillingSummary.LoadId LEFT OUTER JOIN
                         dbo.LoadsInvoice ON dbo.Loads.Id = dbo.LoadsInvoice.LoadId LEFT OUTER JOIN
                         dbo.UserMaster ON dbo.Loads.SalesPersonId = dbo.UserMaster.UserName LEFT OUTER JOIN
                         dbo.LabTest ON dbo.Loads.LabTestId = dbo.LabTest.Id LEFT OUTER JOIN
                         dbo.Customer ON dbo.Loads.CustomerId = dbo.Customer.Id FULL OUTER JOIN
                         dbo.Generator INNER JOIN
                         dbo.Profile ON dbo.Generator.Id = dbo.Profile.GeneratorId ON dbo.Loads.ProfileId = dbo.Profile.Id
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[BillingDepartments]](../Tables/dbo_BillingDepartments.md)
* [[dbo].[Customer]](../Tables/dbo_Customer.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[LabTest]](../Tables/dbo_LabTest.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[LoadsBillingSummary]](../Tables/dbo_LoadsBillingSummary.md)
* [[dbo].[LoadsInvoice]](../Tables/dbo_LoadsInvoice.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[ServiceTypes]](../Tables/dbo_ServiceTypes.md)
* [[dbo].[UserMaster]](../Tables/dbo_UserMaster.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

