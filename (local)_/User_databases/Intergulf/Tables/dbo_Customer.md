#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.Customer

# ![Tables](../../../../Images/Table32.png) [dbo].[Customer]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 1757 |
| Created | 6:47:33 PM Monday, January 29, 2007 |
| Last Modified | 4:28:33 PM Thursday, December 17, 2020 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_Customer: Id](../../../../Images/pkcluster.png)](#indexes)[![Indexes hind_2009058193_1A_2A, _dta_stat_2009058193_1_2_15](../../../../Images/Index.png)](#indexes)(2) | Id | numeric(18,0) | 9 | NOT NULL | 1 - 1 |
| [![Indexes hind_2009058193_1A_2A, _dta_stat_2009058193_1_2_15, _dta_stat_2009058193_20_2, _dta_stat_2009058193_2_15](../../../../Images/Index.png)](#indexes)(4) | Name | varchar(100) | 100 | NULL allowed |  |
|  | Address | varchar(3000) | 3000 | NULL allowed |  |
|  | City | varchar(50) | 50 | NULL allowed |  |
|  | State | varchar(50) | 50 | NULL allowed |  |
|  | Zip | varchar(50) | 50 | NULL allowed |  |
|  | BillingName | varchar(100) | 100 | NULL allowed |  |
|  | BillingAddress | varchar(3000) | 3000 | NULL allowed |  |
|  | BillingCity | varchar(50) | 50 | NULL allowed |  |
|  | BillingState | varchar(50) | 50 | NULL allowed |  |
|  | BillingZip | varchar(50) | 50 | NULL allowed |  |
|  | Contact | varchar(50) | 50 | NULL allowed |  |
|  | Phone | varchar(50) | 50 | NULL allowed |  |
|  | Fax | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_stat_2009058193_1_2_15, _dta_stat_2009058193_2_15](../../../../Images/Index.png)](#indexes)(2) | Email | varchar(50) | 50 | NULL allowed |  |
|  | RegistrationNo | varchar(50) | 50 | NULL allowed |  |
|  | EpaIdNo | varchar(50) | 50 | NULL allowed |  |
|  | Type | varchar(50) | 50 | NULL allowed |  |
|  | Classification | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_stat_2009058193_20_2](../../../../Images/Index.png)](#indexes) | MaterialDisbursement | int | 4 | NULL allowed |  |
|  | UpdateDateTime | datetime | 8 | NULL allowed |  |
|  | UpdateUser | varchar(50) | 50 | NULL allowed |  |
|  | UpdateComputer | varchar(50) | 50 | NULL allowed |  |
|  | MaxTCPeriod | varchar(50) | 50 | NULL allowed |  |
|  | MaxTCCount | numeric(18,0) | 9 | NULL allowed |  |
|  | MinTCPeriod | varchar(50) | 50 | NULL allowed |  |
|  | MinTCCount | numeric(18,0) | 9 | NULL allowed |  |
|  | CustomerStop | bit | 1 | NULL allowed |  |
|  | CompanyId | varchar(25) | 25 | NULL allowed |  |
|  | SageCustomerNumber | varchar(20) | 20 | NULL allowed |  |
|  | PoRequired | int | 4 | NULL allowed |  |
|  | PoNumber | varchar(50) | 50 | NULL allowed |  |
|  | PoNumberExpirationDate | date | 3 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_Customer: Id](../../../../Images/pkcluster.png)](#indexes) | PK_Customer | Id | YES |


---

## <a name="#statistics"></a>Statistics

| Name | Key Columns |
|---|---|
| _dta_stat_2009058193_1_2_15 | Id, Name, Email |
| _dta_stat_2009058193_20_2 | MaterialDisbursement, Name |
| _dta_stat_2009058193_2_15 | Name, Email |
| hind_2009058193_1A_2A | Id, Name |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[Customer]
(
[Id] [numeric] (18, 0) NOT NULL IDENTITY(1, 1),
[Name] [varchar] (100) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Address] [varchar] (3000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[City] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[State] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Zip] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[BillingName] [varchar] (100) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[BillingAddress] [varchar] (3000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[BillingCity] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[BillingState] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[BillingZip] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Contact] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Phone] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Fax] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Email] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[RegistrationNo] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[EpaIdNo] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Type] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Classification] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[MaterialDisbursement] [int] NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[MaxTCPeriod] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[MaxTCCount] [numeric] (18, 0) NULL,
[MinTCPeriod] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[MinTCCount] [numeric] (18, 0) NULL,
[CustomerStop] [bit] NULL,
[CompanyId] [varchar] (25) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SageCustomerNumber] [varchar] (20) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PoRequired] [int] NULL,
[PoNumber] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PoNumberExpirationDate] [date] NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[Customer] ADD CONSTRAINT [PK_Customer] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO
CREATE STATISTICS [hind_2009058193_1A_2A] ON [dbo].[Customer] ([Id], [Name])
GO
CREATE STATISTICS [_dta_stat_2009058193_1_2_15] ON [dbo].[Customer] ([Id], [Name], [Email])
GO
CREATE STATISTICS [_dta_stat_2009058193_20_2] ON [dbo].[Customer] ([MaterialDisbursement], [Name])
GO
CREATE STATISTICS [_dta_stat_2009058193_2_15] ON [dbo].[Customer] ([Name], [Email])
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwChooseProfile]](../Views/dbo_vwChooseProfile.md)
* [[dbo].[vwCustomerGeneratorProfileReport]](../Views/dbo_vwCustomerGeneratorProfileReport.md)
* [[dbo].[vwCustomerGeneratorSort]](../Views/dbo_vwCustomerGeneratorSort.md)
* [[dbo].[vwExportLoadLabVolume]](../Views/dbo_vwExportLoadLabVolume.md)
* [[dbo].[vwExportLoadVolume]](../Views/dbo_vwExportLoadVolume.md)
* [[dbo].[vwProfilesActiveNoMSDS]](../Views/dbo_vwProfilesActiveNoMSDS.md)
* [[dbo].[vwRptLabTestForm]](../Views/dbo_vwRptLabTestForm.md)
* [[dbo].[vwRptLoadDriverTimeLog]](../Views/dbo_vwRptLoadDriverTimeLog.md)
* [[dbo].[vwRptLoadRequest]](../Views/dbo_vwRptLoadRequest.md)
* [[dbo].[vwRptLoadsTrailerStorage]](../Views/dbo_vwRptLoadsTrailerStorage.md)
* [[dbo].[vwRptProfileForm]](../Views/dbo_vwRptProfileForm.md)
* [[dbo].[vwRptProfileFormProduct]](../Views/dbo_vwRptProfileFormProduct.md)
* [[dbo].[vwSelectAvailableForScheduledLoadsAll]](../Views/dbo_vwSelectAvailableForScheduledLoadsAll.md)
* [[dbo].[vwSelectAvailableForScheduledLoadsPending]](../Views/dbo_vwSelectAvailableForScheduledLoadsPending.md)
* [[dbo].[vwSelectAvailableForScheduledLoadsScheduled]](../Views/dbo_vwSelectAvailableForScheduledLoadsScheduled.md)
* [[dbo].[vwSelectCustomerAll]](../Views/dbo_vwSelectCustomerAll.md)
* [[dbo].[vwSelectCustomerForSaturn]](../Views/dbo_vwSelectCustomerForSaturn.md)
* [[dbo].[vwSelectCustomerPOInformation]](../Views/dbo_vwSelectCustomerPOInformation.md)
* [[dbo].[vwSelectCustomerStopAssignment]](../Views/dbo_vwSelectCustomerStopAssignment.md)
* [[dbo].[vwSelectCustomerStopInformation]](../Views/dbo_vwSelectCustomerStopInformation.md)
* [[dbo].[vwSelectCustomerStopInformationLoadRequest]](../Views/dbo_vwSelectCustomerStopInformationLoadRequest.md)
* [[dbo].[vwSelectExportLoadLabVolume]](../Views/dbo_vwSelectExportLoadLabVolume.md)
* [[dbo].[vwSelectExportLoadLabVolumeNew]](../Views/dbo_vwSelectExportLoadLabVolumeNew.md)
* [[dbo].[vwSelectExportLoadsForEBE]](../Views/dbo_vwSelectExportLoadsForEBE.md)
* [[dbo].[vwSelectExportLoadsForEBETemp]](../Views/dbo_vwSelectExportLoadsForEBETemp.md)
* [[dbo].[vwSelectExportProfileNewBusiness]](../Views/dbo_vwSelectExportProfileNewBusiness.md)
* [[dbo].[vwSelectExportProfiles]](../Views/dbo_vwSelectExportProfiles.md)
* [[dbo].[vwSelectExportProfilesApprovalDays]](../Views/dbo_vwSelectExportProfilesApprovalDays.md)
* [[dbo].[vwSelectExportProfilesNew]](../Views/dbo_vwSelectExportProfilesNew.md)
* [[dbo].[vwSelectExportToSage]](../Views/dbo_vwSelectExportToSage.md)
* [[dbo].[vwSelectExportToSageAccrual]](../Views/dbo_vwSelectExportToSageAccrual.md)
* [[dbo].[vwSelectExportToSageTest]](../Views/dbo_vwSelectExportToSageTest.md)
* [[dbo].[vwSelectLabTest]](../Views/dbo_vwSelectLabTest.md)
* [[dbo].[vwSelectLoadForSchedule]](../Views/dbo_vwSelectLoadForSchedule.md)
* [[dbo].[vwSelectLoadRequest]](../Views/dbo_vwSelectLoadRequest.md)
* [[dbo].[vwSelectLoads]](../Views/dbo_vwSelectLoads.md)
* [[dbo].[vwSelectLoadsByProfileCreateDate]](../Views/dbo_vwSelectLoadsByProfileCreateDate.md)
* [[dbo].[vwSelectLoadsForBayportCWaste]](../Views/dbo_vwSelectLoadsForBayportCWaste.md)
* [[dbo].[vwSelectLoadsForSaturn]](../Views/dbo_vwSelectLoadsForSaturn.md)
* [[dbo].[vwSelectLoadsInactive]](../Views/dbo_vwSelectLoadsInactive.md)
* [[dbo].[vwSelectMonthlyDischarge]](../Views/dbo_vwSelectMonthlyDischarge.md)
* [[dbo].[vwSelectPendingLoads]](../Views/dbo_vwSelectPendingLoads.md)
* [[dbo].[vwSelectProfileActiveLastLoadDate]](../Views/dbo_vwSelectProfileActiveLastLoadDate.md)
* [[dbo].[vwSelectProfileActiveLastLoadDateNew]](../Views/dbo_vwSelectProfileActiveLastLoadDateNew.md)
* [[dbo].[vwSelectProfileReviewForMarc]](../Views/dbo_vwSelectProfileReviewForMarc.md)
* [[dbo].[vwSelectProfilesInactive]](../Views/dbo_vwSelectProfilesInactive.md)
* [[dbo].[vwSelectProfilesInReviewNextReviewUser]](../Views/dbo_vwSelectProfilesInReviewNextReviewUser.md)
* [[dbo].[vwSelectProfilesInReviewNextUser]](../Views/dbo_vwSelectProfilesInReviewNextUser.md)
* [[dbo].[vwSelectSaturnTransactions]](../Views/dbo_vwSelectSaturnTransactions.md)
* [[dbo].[vwSelectSaturnTransactionsBackup]](../Views/dbo_vwSelectSaturnTransactionsBackup.md)
* [[dbo].[vwSelectScheduledLoads]](../Views/dbo_vwSelectScheduledLoads.md)
* [[dbo].[vwSelectTrailerScheduledLoads]](../Views/dbo_vwSelectTrailerScheduledLoads.md)
* [[dbo].[fnSelectCustomer]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectCustomer.md)
* [[dbo].[fnSelectOneCustomer]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectOneCustomer.md)
* [[dbo].[fnSelectOneLabTest]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectOneLabTest.md)
* [[dbo].[fnSelectScheduledLoads]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectScheduledLoads.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

