#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectExportToSage

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectExportToSage]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 3:16:12 PM Monday, October 1, 2018 |
| Last Modified | 9:56:53 PM Thursday, October 13, 2022 |


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
| AddWashOut | varchar(2) | 2 |
| WashOutFee | numeric(18,2) | 9 |
| OrganicTestType | varchar(10) | 10 |
| OrganicGallons | numeric(18,0) | 9 |
| OrganicValue | numeric(18,0) | 9 |
| OrganicAllowance | numeric(18,2) | 9 |
| OrganicIncrement | numeric(18,2) | 9 |
| OrganicRate | numeric(18,3) | 9 |
| AddOrganic | varchar(2) | 2 |
| SolidsTestType | varchar(10) | 10 |
| SolidsGallons | numeric(18,0) | 9 |
| SolidsValue | numeric(18,0) | 9 |
| SolidsAllowance | numeric(18,2) | 9 |
| SolidsIncrement | numeric(18,2) | 9 |
| SolidsRate | numeric(18,3) | 9 |
| AddSolids | varchar(2) | 2 |
| OrganicOverage | numeric(18,0) | 9 |
| OrganicIncrements | numeric(18,4) | 9 |
| OrganicSurchargeRate | numeric(18,4) | 9 |
| OrganicCharge | numeric(18,2) | 9 |
| SolidsOverage | numeric(18,0) | 9 |
| SolidsIncrements | numeric(18,4) | 9 |
| SolidsSurchargeRate | numeric(18,4) | 9 |
| SolidsCharge | numeric(18,2) | 9 |
| AddThirdPartyTrans | varchar(2) | 2 |
| HydroCarbonTestType | varchar(10) | 10 |
| HydroCarbonGallons | numeric(18,0) | 9 |
| HydroCarbonValue | numeric(18,0) | 9 |
| HydroCarbonAllowance | numeric(18,2) | 9 |
| HydroCarbonIncrement | numeric(18,2) | 9 |
| HydroCarbonRate | numeric(18,3) | 9 |
| AddHydroCarbon | varchar(2) | 2 |
| HydroCarbonOverage | numeric(18,0) | 9 |
| HydroCarbonIncrements | numeric(18,4) | 9 |
| HydroCarbonSurchargeRate | numeric(18,4) | 9 |
| HydroCarbonCharge | numeric(18,2) | 9 |
| ScavengerPrice | numeric(18,2) | 9 |
| ScavengerQuantity | numeric(18,2) | 9 |
| ScavengerCharge | numeric(18,2) | 9 |
| AddScavenger | varchar(2) | 2 |
| DemurragePrice | numeric(18,2) | 9 |
| DemurrageQuantity | numeric(18,2) | 9 |
| DemurrageCharge | numeric(18,2) | 9 |
| AddDemurrage | varchar(2) | 2 |
| AddThirdPartyWashOut | varchar(2) | 2 |
| Facility | varchar(50) | 50 |
| MaterialClassification | varchar(200) | 200 |
| SalespersonName | varchar(101) | 101 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectExportToSage]
AS
SELECT        dbo.Loads.Id, dbo.Loads.ScheduledDate, dbo.Customer.SageCustomerNumber, dbo.Generator.Name AS GeneratorName, dbo.Profile.ProfileNumber, dbo.LabTest.DocumentNumber, dbo.LabTest.Notes, 
                         dbo.Loads.SalesPersonId, dbo.UserMaster.SageSalespersonCode, dbo.LoadsInvoice.Price, dbo.LoadsInvoice.Quantity, dbo.LoadsInvoice.Units, dbo.LoadsInvoice.TransPrice, dbo.LoadsInvoice.TransQuantity, 
                         dbo.LoadsInvoice.TransMethod, dbo.LoadsInvoice.SurchargePrice, dbo.LoadsInvoice.SurchargeQuantity, dbo.Loads.AccountingStatus, dbo.LoadsInvoice.OwnerId, dbo.Profile.PTFuelSerCharge, 
                         dbo.Loads.BillingDepartment, dbo.BillingDepartments.ServiceTypeId, dbo.ServiceTypes.ServiceType, RIGHT(dbo.Profile.WasteCode, 1) AS WCEndIn, dbo.LoadsInvoice.AddFuelSurCharge, 
                         dbo.Loads.CustomerPickupDelivery, LEN(dbo.Profile.EPAWasteCode1 + dbo.Profile.EPAWasteCode2 + dbo.Profile.EPAWasteCode3 + dbo.Profile.EPAWasteCode4) AS LenEPACode, 
                         dbo.BillingDepartments.SageCostCenter, dbo.Profile.HTYes, dbo.Profile.WasteCode, dbo.Profile.ProfileType, dbo.Profile.Direction, dbo.Profile.EPAWasteCode1, dbo.Profile.EPAWasteCode2, 
                         dbo.Profile.EPAWasteCode3, dbo.Profile.EPAWasteCode4, dbo.Profile.Id AS ProfileId, dbo.LoadsInvoice.ManifestFee, dbo.Loads.CustomerPoNumber, dbo.LoadsInvoice.AddWashOut, 
                         dbo.LoadsInvoice.WashOutFee, dbo.LoadsInvoice.OrganicTestType, dbo.LoadsInvoice.OrganicGallons, dbo.LoadsInvoice.OrganicValue, dbo.LoadsInvoice.OrganicAllowance, dbo.LoadsInvoice.OrganicIncrement, 
                         dbo.LoadsInvoice.OrganicRate, dbo.LoadsInvoice.AddOrganic, dbo.LoadsInvoice.SolidsTestType, dbo.LoadsInvoice.SolidsGallons, dbo.LoadsInvoice.SolidsValue, dbo.LoadsInvoice.SolidsAllowance, 
                         dbo.LoadsInvoice.SolidsIncrement, dbo.LoadsInvoice.SolidsRate, dbo.LoadsInvoice.AddSolids, dbo.LoadsInvoice.OrganicOverage, dbo.LoadsInvoice.OrganicIncrements, dbo.LoadsInvoice.OrganicSurchargeRate,
                          dbo.LoadsInvoice.OrganicCharge, dbo.LoadsInvoice.SolidsOverage, dbo.LoadsInvoice.SolidsIncrements, dbo.LoadsInvoice.SolidsSurchargeRate, dbo.LoadsInvoice.SolidsCharge, 
                         dbo.LoadsInvoice.AddThirdPartyTrans, dbo.LoadsInvoice.HydroCarbonTestType, dbo.LoadsInvoice.HydroCarbonGallons, dbo.LoadsInvoice.HydroCarbonValue, dbo.LoadsInvoice.HydroCarbonAllowance, 
                         dbo.LoadsInvoice.HydroCarbonIncrement, dbo.LoadsInvoice.HydroCarbonRate, dbo.LoadsInvoice.AddHydroCarbon, dbo.LoadsInvoice.HydroCarbonOverage, dbo.LoadsInvoice.HydroCarbonIncrements, 
                         dbo.LoadsInvoice.HydroCarbonSurchargeRate, dbo.LoadsInvoice.HydroCarbonCharge, dbo.LoadsInvoice.ScavengerPrice, dbo.LoadsInvoice.ScavengerQuantity, dbo.LoadsInvoice.ScavengerCharge, 
                         dbo.LoadsInvoice.AddScavenger, dbo.LoadsInvoice.DemurragePrice, dbo.LoadsInvoice.DemurrageQuantity, dbo.LoadsInvoice.DemurrageCharge, dbo.LoadsInvoice.AddDemurrage, 
                         dbo.LoadsInvoice.AddThirdPartyWashOut, dbo.Destination.Facility, dbo.Profile.MaterialClassification, Trim(dbo.UserMaster.FirstName + ' ' + dbo.UserMaster.LastName) AS SalespersonName
FROM            dbo.Loads LEFT OUTER JOIN
                         dbo.Destination ON dbo.Loads.DestinationId = dbo.Destination.Id LEFT OUTER JOIN
                         dbo.LoadsBillingSummary INNER JOIN
                         dbo.BillingDepartments ON dbo.LoadsBillingSummary.BillingDepartment = dbo.BillingDepartments.Description INNER JOIN
                         dbo.ServiceTypes ON dbo.BillingDepartments.ServiceTypeId = dbo.ServiceTypes.Id ON dbo.Loads.Id = dbo.LoadsBillingSummary.LoadId LEFT OUTER JOIN
                         dbo.LoadsInvoice ON dbo.Loads.Id = dbo.LoadsInvoice.LoadId LEFT OUTER JOIN
                         dbo.UserMaster ON dbo.Loads.SalesPersonId = dbo.UserMaster.UserName LEFT OUTER JOIN
                         dbo.LabTest ON dbo.Loads.LabTestId = dbo.LabTest.Id LEFT OUTER JOIN
                         dbo.Customer ON dbo.Loads.CustomerId = dbo.Customer.Id FULL OUTER JOIN
                         dbo.Generator INNER JOIN
                         dbo.Profile ON dbo.Generator.Id = dbo.Profile.GeneratorId ON dbo.Loads.ProfileId = dbo.Profile.Id
WHERE        (dbo.Loads.AccountingStatus = 'Ready To Bill') OR
                         (dbo.Loads.AccountingStatus = 'Internal Ready To Bill')
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[BillingDepartments]](../Tables/dbo_BillingDepartments.md)
* [[dbo].[Customer]](../Tables/dbo_Customer.md)
* [[dbo].[Destination]](../Tables/dbo_Destination.md)
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

