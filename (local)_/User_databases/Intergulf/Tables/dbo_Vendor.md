#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.Vendor

# ![Tables](../../../../Images/Table32.png) [dbo].[Vendor]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 1121 |
| Created | 11:16:35 AM Friday, February 2, 2007 |
| Last Modified | 12:26:02 PM Tuesday, October 4, 2022 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_Vendor: Id](../../../../Images/pkcluster.png)](#indexes) | Id | bigint | 8 | NOT NULL | 1 - 1 |
|  | Mas90Id | varchar(50) | 50 | NULL allowed |  |
|  | Name | varchar(50) | 50 | NULL allowed |  |
|  | Address | varchar(300) | 300 | NULL allowed |  |
|  | City | varchar(100) | 100 | NULL allowed |  |
|  | State | varchar(50) | 50 | NULL allowed |  |
|  | Zip | varchar(50) | 50 | NULL allowed |  |
|  | PaymentName | varchar(50) | 50 | NULL allowed |  |
|  | PaymentAddress | varchar(300) | 300 | NULL allowed |  |
|  | PaymentCity | varchar(100) | 100 | NULL allowed |  |
|  | PaymentState | varchar(50) | 50 | NULL allowed |  |
|  | PaymentZip | varchar(50) | 50 | NULL allowed |  |
|  | Contact | varchar(50) | 50 | NULL allowed |  |
|  | Phone | varchar(50) | 50 | NULL allowed |  |
|  | Fax | varchar(50) | 50 | NULL allowed |  |
|  | Email | varchar(50) | 50 | NULL allowed |  |
|  | UpdateDateTime | datetime | 8 | NULL allowed |  |
|  | UpdateUser | varchar(50) | 50 | NULL allowed |  |
|  | UpdateComputer | varchar(50) | 50 | NULL allowed |  |
|  | ShortName | varchar(50) | 50 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_Vendor: Id](../../../../Images/pkcluster.png)](#indexes) | PK_Vendor | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[Vendor]
(
[Id] [bigint] NOT NULL IDENTITY(1, 1),
[Mas90Id] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Name] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Address] [varchar] (300) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[City] [varchar] (100) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[State] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Zip] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PaymentName] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PaymentAddress] [varchar] (300) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PaymentCity] [varchar] (100) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PaymentState] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PaymentZip] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Contact] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Phone] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Fax] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Email] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ShortName] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[Vendor] ADD CONSTRAINT [PK_Vendor] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwChooseProfile]](../Views/dbo_vwChooseProfile.md)
* [[dbo].[vwCustomerGeneratorProfileReport]](../Views/dbo_vwCustomerGeneratorProfileReport.md)
* [[dbo].[vwInventoryContracts]](../Views/dbo_vwInventoryContracts.md)
* [[dbo].[vwRptLoadRequest]](../Views/dbo_vwRptLoadRequest.md)
* [[dbo].[vwSaturnTestVendor]](../Views/dbo_vwSaturnTestVendor.md)
* [[dbo].[vwSelectExportProfiles]](../Views/dbo_vwSelectExportProfiles.md)
* [[dbo].[vwSelectExportProfilesNew]](../Views/dbo_vwSelectExportProfilesNew.md)
* [[dbo].[vwSelectInventoryFixedCostContracts]](../Views/dbo_vwSelectInventoryFixedCostContracts.md)
* [[dbo].[vwSelectInventoryRailCarContracts]](../Views/dbo_vwSelectInventoryRailCarContracts.md)
* [[dbo].[vwSelectSaturnTransactions]](../Views/dbo_vwSelectSaturnTransactions.md)
* [[dbo].[vwSelectSaturnTransactionsBackup]](../Views/dbo_vwSelectSaturnTransactionsBackup.md)
* [[dbo].[vwSelectVendorForSaturn]](../Views/dbo_vwSelectVendorForSaturn.md)
* [[dbo].[fnSelectOneVendor]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectOneVendor.md)
* [[dbo].[fnSelectVendor]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectVendor.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

