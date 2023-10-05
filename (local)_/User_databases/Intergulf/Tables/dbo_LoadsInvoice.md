#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.LoadsInvoice

# ![Tables](../../../../Images/Table32.png) [dbo].[LoadsInvoice]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 147720 |
| Created | 6:45:02 PM Sunday, September 23, 2018 |
| Last Modified | 1:38:17 PM Friday, June 3, 2022 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_LoadsInvoice: LoadId](../../../../Images/pkcluster.png)](#indexes) | LoadId | bigint | 8 | NOT NULL |
|  | Price | numeric(18,4) | 9 | NULL allowed |
|  | Quantity | numeric(18,2) | 9 | NULL allowed |
|  | Units | varchar(50) | 50 | NULL allowed |
|  | TransPrice | numeric(18,4) | 9 | NULL allowed |
|  | TransQuantity | numeric(18,2) | 9 | NULL allowed |
|  | TransMethod | varchar(50) | 50 | NULL allowed |
|  | SurchargePrice | numeric(18,4) | 9 | NULL allowed |
|  | SurchargeQuantity | numeric(18,2) | 9 | NULL allowed |
|  | CreateDateTime | datetime | 8 | NULL allowed |
|  | CreateUser | varchar(50) | 50 | NULL allowed |
|  | CreateComputer | varchar(50) | 50 | NULL allowed |
|  | UpdateDateTime | datetime | 8 | NULL allowed |
|  | UpdateUser | varchar(50) | 50 | NULL allowed |
|  | UpdateComputer | varchar(50) | 50 | NULL allowed |
|  | OwnerId | varchar(50) | 50 | NULL allowed |
|  | AddFuelSurCharge | varchar(2) | 2 | NULL allowed |
|  | ManifestFee | varchar(2) | 2 | NULL allowed |
|  | AddWashOut | varchar(2) | 2 | NULL allowed |
|  | WashOutFee | numeric(18,2) | 9 | NULL allowed |
|  | OrganicTestType | varchar(10) | 10 | NULL allowed |
|  | OrganicGallons | numeric(18,0) | 9 | NULL allowed |
|  | OrganicValue | numeric(18,0) | 9 | NULL allowed |
|  | OrganicAllowance | numeric(18,2) | 9 | NULL allowed |
|  | OrganicIncrement | numeric(18,2) | 9 | NULL allowed |
|  | OrganicRate | numeric(18,3) | 9 | NULL allowed |
|  | AddOrganic | varchar(2) | 2 | NULL allowed |
|  | SolidsTestType | varchar(10) | 10 | NULL allowed |
|  | SolidsGallons | numeric(18,0) | 9 | NULL allowed |
|  | SolidsValue | numeric(18,0) | 9 | NULL allowed |
|  | SolidsAllowance | numeric(18,2) | 9 | NULL allowed |
|  | SolidsIncrement | numeric(18,2) | 9 | NULL allowed |
|  | SolidsRate | numeric(18,3) | 9 | NULL allowed |
|  | AddSolids | varchar(2) | 2 | NULL allowed |
|  | OrganicOverage | numeric(18,0) | 9 | NULL allowed |
|  | OrganicIncrements | numeric(18,4) | 9 | NULL allowed |
|  | OrganicSurchargeRate | numeric(18,4) | 9 | NULL allowed |
|  | OrganicCharge | numeric(18,2) | 9 | NULL allowed |
|  | SolidsOverage | numeric(18,0) | 9 | NULL allowed |
|  | SolidsIncrements | numeric(18,4) | 9 | NULL allowed |
|  | SolidsSurchargeRate | numeric(18,4) | 9 | NULL allowed |
|  | SolidsCharge | numeric(18,2) | 9 | NULL allowed |
|  | AddThirdPartyTrans | varchar(2) | 2 | NULL allowed |
|  | HydroCarbonTestType | varchar(10) | 10 | NULL allowed |
|  | HydroCarbonGallons | numeric(18,0) | 9 | NULL allowed |
|  | HydroCarbonValue | numeric(18,0) | 9 | NULL allowed |
|  | HydroCarbonAllowance | numeric(18,2) | 9 | NULL allowed |
|  | HydroCarbonIncrement | numeric(18,2) | 9 | NULL allowed |
|  | HydroCarbonRate | numeric(18,3) | 9 | NULL allowed |
|  | AddHydroCarbon | varchar(2) | 2 | NULL allowed |
|  | HydroCarbonOverage | numeric(18,0) | 9 | NULL allowed |
|  | HydroCarbonIncrements | numeric(18,4) | 9 | NULL allowed |
|  | HydroCarbonSurchargeRate | numeric(18,4) | 9 | NULL allowed |
|  | HydroCarbonCharge | numeric(18,2) | 9 | NULL allowed |
|  | ScavengerPrice | numeric(18,2) | 9 | NULL allowed |
|  | ScavengerQuantity | numeric(18,2) | 9 | NULL allowed |
|  | ScavengerCharge | numeric(18,2) | 9 | NULL allowed |
|  | AddScavenger | varchar(2) | 2 | NULL allowed |
|  | DemurragePrice | numeric(18,2) | 9 | NULL allowed |
|  | DemurrageQuantity | numeric(18,2) | 9 | NULL allowed |
|  | DemurrageCharge | numeric(18,2) | 9 | NULL allowed |
|  | AddDemurrage | varchar(2) | 2 | NULL allowed |
|  | AddThirdPartyWashOut | varchar(2) | 2 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_LoadsInvoice: LoadId](../../../../Images/pkcluster.png)](#indexes) | PK_LoadsInvoice | LoadId | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[LoadsInvoice]
(
[LoadId] [bigint] NOT NULL,
[Price] [numeric] (18, 4) NULL,
[Quantity] [numeric] (18, 2) NULL,
[Units] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[TransPrice] [numeric] (18, 4) NULL,
[TransQuantity] [numeric] (18, 2) NULL,
[TransMethod] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SurchargePrice] [numeric] (18, 4) NULL,
[SurchargeQuantity] [numeric] (18, 2) NULL,
[CreateDateTime] [datetime] NULL,
[CreateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[OwnerId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[AddFuelSurCharge] [varchar] (2) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ManifestFee] [varchar] (2) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[AddWashOut] [varchar] (2) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[WashOutFee] [numeric] (18, 2) NULL,
[OrganicTestType] [varchar] (10) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[OrganicGallons] [numeric] (18, 0) NULL,
[OrganicValue] [numeric] (18, 0) NULL,
[OrganicAllowance] [numeric] (18, 2) NULL,
[OrganicIncrement] [numeric] (18, 2) NULL,
[OrganicRate] [numeric] (18, 3) NULL,
[AddOrganic] [varchar] (2) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SolidsTestType] [varchar] (10) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SolidsGallons] [numeric] (18, 0) NULL,
[SolidsValue] [numeric] (18, 0) NULL,
[SolidsAllowance] [numeric] (18, 2) NULL,
[SolidsIncrement] [numeric] (18, 2) NULL,
[SolidsRate] [numeric] (18, 3) NULL,
[AddSolids] [varchar] (2) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[OrganicOverage] [numeric] (18, 0) NULL,
[OrganicIncrements] [numeric] (18, 4) NULL,
[OrganicSurchargeRate] [numeric] (18, 4) NULL,
[OrganicCharge] [numeric] (18, 2) NULL,
[SolidsOverage] [numeric] (18, 0) NULL,
[SolidsIncrements] [numeric] (18, 4) NULL,
[SolidsSurchargeRate] [numeric] (18, 4) NULL,
[SolidsCharge] [numeric] (18, 2) NULL,
[AddThirdPartyTrans] [varchar] (2) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[HydroCarbonTestType] [varchar] (10) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[HydroCarbonGallons] [numeric] (18, 0) NULL,
[HydroCarbonValue] [numeric] (18, 0) NULL,
[HydroCarbonAllowance] [numeric] (18, 2) NULL,
[HydroCarbonIncrement] [numeric] (18, 2) NULL,
[HydroCarbonRate] [numeric] (18, 3) NULL,
[AddHydroCarbon] [varchar] (2) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[HydroCarbonOverage] [numeric] (18, 0) NULL,
[HydroCarbonIncrements] [numeric] (18, 4) NULL,
[HydroCarbonSurchargeRate] [numeric] (18, 4) NULL,
[HydroCarbonCharge] [numeric] (18, 2) NULL,
[ScavengerPrice] [numeric] (18, 2) NULL,
[ScavengerQuantity] [numeric] (18, 2) NULL,
[ScavengerCharge] [numeric] (18, 2) NULL,
[AddScavenger] [varchar] (2) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[DemurragePrice] [numeric] (18, 2) NULL,
[DemurrageQuantity] [numeric] (18, 2) NULL,
[DemurrageCharge] [numeric] (18, 2) NULL,
[AddDemurrage] [varchar] (2) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[AddThirdPartyWashOut] [varchar] (2) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[LoadsInvoice] ADD CONSTRAINT [PK_LoadsInvoice] PRIMARY KEY CLUSTERED ([LoadId]) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwSelectExportToSage]](../Views/dbo_vwSelectExportToSage.md)
* [[dbo].[vwSelectExportToSageAccrual]](../Views/dbo_vwSelectExportToSageAccrual.md)
* [[dbo].[vwSelectExportToSageTest]](../Views/dbo_vwSelectExportToSageTest.md)
* [[dbo].[vwSelectLoadsReadyForAccountingExport]](../Views/dbo_vwSelectLoadsReadyForAccountingExport.md)
* [[dbo].[vwSelectLoadsReadyForAccountingNew]](../Views/dbo_vwSelectLoadsReadyForAccountingNew.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

