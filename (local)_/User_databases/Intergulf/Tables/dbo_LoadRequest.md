#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.LoadRequest

# ![Tables](../../../../Images/Table32.png) [dbo].[LoadRequest]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 109805 |
| Created | 2:25:41 PM Monday, March 26, 2007 |
| Last Modified | 7:08:08 PM Wednesday, June 7, 2023 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_LoadRequest: Id](../../../../Images/pkcluster.png)](#indexes)[![Indexes _dta_index_LoadRequest_5_238623893__K24_K5_K2_K9_K10_1_6_7_11_13_20_32, _dta_index_LoadRequest_5_238623893__K25_K26_1, hind_238623893_9A, hind_238623893_10A, hind_238623893_5A_24A_9A_10A_1A_6A_7A_11A_13A_20A](../../../../Images/Index.png)](#indexes)(5) | Id | bigint | 8 | NOT NULL | 1 - 1 |
| [![Indexes _dta_index_LoadRequest_5_238623893__K24_K5_K2_K9_K10_1_6_7_11_13_20_32, _dta_stat_238623893_9_10_2_24, _dta_stat_238623893_24_2, _dta_stat_238623893_2_5_24_9_10](../../../../Images/Index.png)](#indexes)(4) | SalesPersonId | varchar(50) | 50 | NULL allowed |  |
|  | CustomerId | bigint | 8 | NULL allowed |  |
|  | VendorId | bigint | 8 | NULL allowed |  |
| [![Indexes _dta_index_LoadRequest_5_238623893__K24_K5_K2_K9_K10_1_6_7_11_13_20_32, hind_238623893_5A_24A_9A_10A_1A_6A_7A_11A_13A_20A, _dta_stat_238623893_2_5_24_9_10](../../../../Images/Index.png)](#indexes)(3) | ProfileId | bigint | 8 | NULL allowed |  |
| [![Indexes _dta_index_LoadRequest_5_238623893__K24_K5_K2_K9_K10_1_6_7_11_13_20_32, hind_238623893_5A_24A_9A_10A_1A_6A_7A_11A_13A_20A](../../../../Images/Index.png)](#indexes)(2) | ContactName | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LoadRequest_5_238623893__K24_K5_K2_K9_K10_1_6_7_11_13_20_32, hind_238623893_5A_24A_9A_10A_1A_6A_7A_11A_13A_20A](../../../../Images/Index.png)](#indexes)(2) | ContactPhone | varchar(50) | 50 | NULL allowed |  |
|  | PickupLocation | varchar(200) | 200 | NULL allowed |  |
| [![Indexes _dta_index_LoadRequest_5_238623893__K24_K5_K2_K9_K10_1_6_7_11_13_20_32, hind_238623893_9A, _dta_stat_238623893_9_10_2_24, hind_238623893_5A_24A_9A_10A_1A_6A_7A_11A_13A_20A, _dta_stat_238623893_2_5_24_9_10](../../../../Images/Index.png)](#indexes)(5) | LoadRequestDate | datetime | 8 | NULL allowed |  |
| [![Indexes _dta_index_LoadRequest_5_238623893__K24_K5_K2_K9_K10_1_6_7_11_13_20_32, _dta_stat_238623893_9_10_2_24, hind_238623893_10A, hind_238623893_5A_24A_9A_10A_1A_6A_7A_11A_13A_20A, _dta_stat_238623893_2_5_24_9_10](../../../../Images/Index.png)](#indexes)(5) | LoadRequestTime | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LoadRequest_5_238623893__K24_K5_K2_K9_K10_1_6_7_11_13_20_32, hind_238623893_5A_24A_9A_10A_1A_6A_7A_11A_13A_20A](../../../../Images/Index.png)](#indexes)(2) | NoLoads | decimal(18,0) | 9 | NULL allowed |  |
|  | EstQuantity | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LoadRequest_5_238623893__K24_K5_K2_K9_K10_1_6_7_11_13_20_32, hind_238623893_5A_24A_9A_10A_1A_6A_7A_11A_13A_20A](../../../../Images/Index.png)](#indexes)(2) | EquipmentType | varchar(50) | 50 | NULL allowed |  |
|  | SubOk | varchar(50) | 50 | NULL allowed |  |
|  | DocumentType | varchar(50) | 50 | NULL allowed |  |
|  | SpecialRequirements | varchar(3000) | 3000 | NULL allowed |  |
|  | DestinationId | bigint | 8 | NULL allowed |  |
|  | WashOutRequired | varchar(50) | 50 | NULL allowed |  |
|  | WeightTicket | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LoadRequest_5_238623893__K24_K5_K2_K9_K10_1_6_7_11_13_20_32, hind_238623893_5A_24A_9A_10A_1A_6A_7A_11A_13A_20A](../../../../Images/Index.png)](#indexes)(2) | VesselTank | varchar(100) | 100 | NULL allowed |  |
|  | CreateUser | varchar(50) | 50 | NULL allowed |  |
|  | CreateDate | datetime | 8 | NULL allowed |  |
|  | CreateTime | datetime | 8 | NULL allowed |  |
| [![Indexes _dta_index_LoadRequest_5_238623893__K24_K5_K2_K9_K10_1_6_7_11_13_20_32, _dta_stat_238623893_9_10_2_24, _dta_stat_238623893_24_2, hind_238623893_5A_24A_9A_10A_1A_6A_7A_11A_13A_20A, _dta_stat_238623893_2_5_24_9_10](../../../../Images/Index.png)](#indexes)(5) | Processed | int | 4 | NULL allowed |  |
| [![Indexes _dta_index_LoadRequest_5_238623893__K25_K26_1, _dta_stat_238623893_25_26](../../../../Images/Index.png)](#indexes)(2) | UpdateDateTime | datetime | 8 | NULL allowed |  |
| [![Indexes _dta_index_LoadRequest_5_238623893__K25_K26_1, _dta_stat_238623893_25_26](../../../../Images/Index.png)](#indexes)(2) | UpdateUser | varchar(50) | 50 | NULL allowed |  |
|  | UpdateComputer | varchar(50) | 50 | NULL allowed |  |
|  | LoadType | varchar(10) | 10 | NULL allowed |  |
|  | ProjectNumber | varchar(50) | 50 | NULL allowed |  |
|  | TankNumber | varchar(50) | 50 | NULL allowed |  |
|  | DeliveryReleaseNumber | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LoadRequest_5_238623893__K24_K5_K2_K9_K10_1_6_7_11_13_20_32](../../../../Images/Index.png)](#indexes) | CustomerPickupDelivery | varchar(3) | 3 | NULL allowed |  |
|  | PickupAnytime | varchar(3) | 3 | NULL allowed |  |
|  | CustomerPoNumber | varchar(50) | 50 | NULL allowed |  |
|  | CustomerPoNumberExpirationDate | date | 3 | NULL allowed |  |
|  | ContractNumber | varchar(50) | 50 | NULL allowed |  |
|  | TransactionType | varchar(20) | 20 | NULL allowed |  |
|  | OAEmailDateTime | datetime | 8 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Included Columns | Unique |
|---|---|---|---|---|
| [![Cluster Primary Key PK_LoadRequest: Id](../../../../Images/pkcluster.png)](#indexes) | PK_LoadRequest | Id |  | YES |
|  | _dta_index_LoadRequest_5_238623893__K24_K5_K2_K9_K10_1_6_7_11_13_20_32 | Processed, ProfileId, SalesPersonId, LoadRequestDate, LoadRequestTime | Id, ContactName, ContactPhone, NoLoads, EquipmentType, VesselTank, CustomerPickupDelivery |  |
|  | _dta_index_LoadRequest_5_238623893__K25_K26_1 | UpdateDateTime, UpdateUser | Id |  |


---

## <a name="#statistics"></a>Statistics

| Name | Key Columns |
|---|---|
| _dta_stat_238623893_24_2 | Processed, SalesPersonId |
| _dta_stat_238623893_25_26 | UpdateDateTime, UpdateUser |
| _dta_stat_238623893_2_5_24_9_10 | SalesPersonId, ProfileId, Processed, LoadRequestDate, LoadRequestTime |
| _dta_stat_238623893_9_10_2_24 | LoadRequestDate, LoadRequestTime, SalesPersonId, Processed |
| hind_238623893_10A | LoadRequestTime, Id |
| hind_238623893_5A_24A_9A_10A_1A_6A_7A_11A_13A_20A | ProfileId, Processed, LoadRequestDate, LoadRequestTime, Id, ContactName, ContactPhone, NoLoads, EquipmentType, VesselTank |
| hind_238623893_9A | LoadRequestDate, Id |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[LoadRequest]
(
[Id] [bigint] NOT NULL IDENTITY(1, 1),
[SalesPersonId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CustomerId] [bigint] NULL,
[VendorId] [bigint] NULL,
[ProfileId] [bigint] NULL,
[ContactName] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ContactPhone] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PickupLocation] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[LoadRequestDate] [datetime] NULL,
[LoadRequestTime] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[NoLoads] [decimal] (18, 0) NULL,
[EstQuantity] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[EquipmentType] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SubOk] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[DocumentType] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SpecialRequirements] [varchar] (3000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[DestinationId] [bigint] NULL,
[WashOutRequired] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[WeightTicket] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[VesselTank] [varchar] (100) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateDate] [datetime] NULL,
[CreateTime] [datetime] NULL,
[Processed] [int] NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[LoadType] [varchar] (10) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ProjectNumber] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[TankNumber] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[DeliveryReleaseNumber] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CustomerPickupDelivery] [varchar] (3) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PickupAnytime] [varchar] (3) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CustomerPoNumber] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CustomerPoNumberExpirationDate] [date] NULL,
[ContractNumber] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[TransactionType] [varchar] (20) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[OAEmailDateTime] [datetime] NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[LoadRequest] ADD CONSTRAINT [PK_LoadRequest] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO
CREATE NONCLUSTERED INDEX [_dta_index_LoadRequest_5_238623893__K24_K5_K2_K9_K10_1_6_7_11_13_20_32] ON [dbo].[LoadRequest] ([Processed], [ProfileId], [SalesPersonId], [LoadRequestDate], [LoadRequestTime]) INCLUDE ([Id], [ContactName], [ContactPhone], [NoLoads], [EquipmentType], [VesselTank], [CustomerPickupDelivery]) ON [PRIMARY]
GO
CREATE NONCLUSTERED INDEX [_dta_index_LoadRequest_5_238623893__K25_K26_1] ON [dbo].[LoadRequest] ([UpdateDateTime], [UpdateUser]) INCLUDE ([Id]) ON [PRIMARY]
GO
CREATE STATISTICS [hind_238623893_9A] ON [dbo].[LoadRequest] ([LoadRequestDate], [Id])
GO
CREATE STATISTICS [_dta_stat_238623893_9_10_2_24] ON [dbo].[LoadRequest] ([LoadRequestDate], [LoadRequestTime], [SalesPersonId], [Processed])
GO
CREATE STATISTICS [hind_238623893_10A] ON [dbo].[LoadRequest] ([LoadRequestTime], [Id])
GO
CREATE STATISTICS [_dta_stat_238623893_24_2] ON [dbo].[LoadRequest] ([Processed], [SalesPersonId])
GO
CREATE STATISTICS [hind_238623893_5A_24A_9A_10A_1A_6A_7A_11A_13A_20A] ON [dbo].[LoadRequest] ([ProfileId], [Processed], [LoadRequestDate], [LoadRequestTime], [Id], [ContactName], [ContactPhone], [NoLoads], [EquipmentType], [VesselTank])
GO
CREATE STATISTICS [_dta_stat_238623893_2_5_24_9_10] ON [dbo].[LoadRequest] ([SalesPersonId], [ProfileId], [Processed], [LoadRequestDate], [LoadRequestTime])
GO
CREATE STATISTICS [_dta_stat_238623893_25_26] ON [dbo].[LoadRequest] ([UpdateDateTime], [UpdateUser])
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwLoadRequestProfileSalespersonFix]](../Views/dbo_vwLoadRequestProfileSalespersonFix.md)
* [[dbo].[vwSelectCustomerStopInformationLoadRequest]](../Views/dbo_vwSelectCustomerStopInformationLoadRequest.md)
* [[dbo].[vwSelectLoadRequest]](../Views/dbo_vwSelectLoadRequest.md)
* [[dbo].[vwSelectLoadRequestForOverage]](../Views/dbo_vwSelectLoadRequestForOverage.md)
* [[dbo].[vwSelectLoadRequestForSchedule]](../Views/dbo_vwSelectLoadRequestForSchedule.md)
* [[dbo].[vwSelectLoadRequestLoadTimes]](../Views/dbo_vwSelectLoadRequestLoadTimes.md)
* [[dbo].[vwSelectLoadRequestProfileMaterialCode]](../Views/dbo_vwSelectLoadRequestProfileMaterialCode.md)
* [[dbo].[vwSelectLoadRequestsLeadTimes]](../Views/dbo_vwSelectLoadRequestsLeadTimes.md)
* [[dbo].[vwSelectLoadRequestSP]](../Views/dbo_vwSelectLoadRequestSP.md)
* [[dbo].[vwSelectLoadsScheduleCreateUser]](../Views/dbo_vwSelectLoadsScheduleCreateUser.md)
* [[dbo].[vwSelectRequestedLoads]](../Views/dbo_vwSelectRequestedLoads.md)
* [[dbo].[vwSelectSaturnTransactions]](../Views/dbo_vwSelectSaturnTransactions.md)
* [[dbo].[vwSelectSaturnTransactionsBackup]](../Views/dbo_vwSelectSaturnTransactionsBackup.md)
* [[dbo].[fnSelectLoadRequest]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectLoadRequest.md)
* [[dbo].[fnSelectOneLoadRequest]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectOneLoadRequest.md)
* [[dbo].[fnSelectOpenLoadRequests]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectOpenLoadRequests.md)
* [[dbo].[fnSelectRequestedLoads]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectRequestedLoads.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

