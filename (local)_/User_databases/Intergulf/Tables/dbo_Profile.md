#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.Profile

# ![Tables](../../../../Images/Table32.png) [dbo].[Profile]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 10784 |
| Created | 2:46:29 PM Monday, March 19, 2007 |
| Last Modified | 1:20:42 PM Monday, October 3, 2022 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_Profile: Id](../../../../Images/pkcluster.png)](#indexes)[![Indexes _dta_index_Profile_5_2098106515__K4_K1_96_100, Profile25, _dta_stat_2098106515_4_2_1_5, _dta_stat_2098106515_4_1_2, _dta_stat_2098106515_1_123_2_3, _dta_stat_2098106515_1_4_2_6_3_9_123_155, _dta_stat_2098106515_1_4_123_2_3, hind_2098106515_1A_4A_5A_40A, _dta_stat_2098106515_1_3_4, _dta_stat_2098106515_5_1_93](../../../../Images/Index.png)](#indexes)(10) | Id | bigint | 8 | NOT NULL | 1 - 1 |
| [![Indexes _dta_stat_2098106515_2_3, _dta_stat_2098106515_123_2_3_4, _dta_stat_2098106515_4_2_1_5, _dta_stat_2098106515_4_1_2, _dta_stat_2098106515_4_3_2_5, _dta_stat_2098106515_1_123_2_3, _dta_stat_2098106515_1_4_2_6_3_9_123_155, _dta_stat_2098106515_1_4_123_2_3, _dta_stat_2098106515_5_4_2, _dta_stat_2098106515_96_4_3_2, _dta_stat_2098106515_96_3_2](../../../../Images/Index.png)](#indexes)(11) | CustomerId | bigint | 8 | NULL allowed |  |
| [![Indexes _dta_stat_2098106515_2_3, _dta_stat_2098106515_123_2_3_4, _dta_stat_2098106515_4_3_2_5, _dta_stat_2098106515_1_123_2_3, _dta_stat_2098106515_1_4_2_6_3_9_123_155, _dta_stat_2098106515_1_4_123_2_3, _dta_stat_2098106515_1_3_4, _dta_stat_2098106515_96_4_3_2, _dta_stat_2098106515_96_3_2](../../../../Images/Index.png)](#indexes)(9) | VendorId | bigint | 8 | NULL allowed |  |
| [![Indexes _dta_index_Profile_5_2098106515__K4_K1_96_100, Profile25, _dta_stat_2098106515_123_2_3_4, _dta_stat_2098106515_4_2_1_5, _dta_stat_2098106515_4_1_2, _dta_stat_2098106515_4_3_2_5, _dta_stat_2098106515_1_4_2_6_3_9_123_155, _dta_stat_2098106515_1_4_123_2_3, hind_2098106515_1A_4A_5A_40A, _dta_stat_2098106515_1_3_4, _dta_stat_2098106515_5_4_2, _dta_stat_2098106515_96_4_3_2](../../../../Images/Index.png)](#indexes)(12) | GeneratorId | bigint | 8 | NULL allowed |  |
| [![Indexes _dta_stat_2098106515_4_2_1_5, _dta_stat_2098106515_4_3_2_5, hind_2098106515_1A_4A_5A_40A, _dta_stat_2098106515_5_4_2, _dta_stat_2098106515_5_1_93](../../../../Images/Index.png)](#indexes)(5) | ProfileNumber | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_stat_2098106515_1_4_2_6_3_9_123_155](../../../../Images/Index.png)](#indexes) | TransporterId | bigint | 8 | NULL allowed |  |
|  | LabTestSampleId | bigint | 8 | NULL allowed |  |
|  | WasteCode | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_stat_2098106515_1_4_2_6_3_9_123_155](../../../../Images/Index.png)](#indexes) | MaterialCodeId | int | 4 | NULL allowed |  |
|  | ProductCategory | varchar(50) | 50 | NULL allowed |  |
|  | MaterialDescription | varchar(3000) | 3000 | NULL allowed |  |
|  | ProcessDescription | varchar(3000) | 3000 | NULL allowed |  |
|  | MaterialClassification | varchar(200) | 200 | NULL allowed |  |
|  | StateWasteCode | varchar(50) | 50 | NULL allowed |  |
|  | SICCode | varchar(50) | 50 | NULL allowed |  |
|  | Volume | varchar(50) | 50 | NULL allowed |  |
|  | LoadFrequency | varchar(50) | 50 | NULL allowed |  |
|  | Viscosity | varchar(50) | 50 | NULL allowed |  |
|  | PhRange | varchar(50) | 50 | NULL allowed |  |
|  | SpecificGravity | varchar(50) | 50 | NULL allowed |  |
|  | FlashPoint | varchar(50) | 50 | NULL allowed |  |
|  | Phase | varchar(50) | 50 | NULL allowed |  |
|  | ViscosityOther | varchar(50) | 50 | NULL allowed |  |
|  | PhRangeOther | varchar(50) | 50 | NULL allowed |  |
|  | SpecificGravityOther | varchar(50) | 50 | NULL allowed |  |
|  | FlashPointOther | varchar(50) | 50 | NULL allowed |  |
|  | PhaseOther | varchar(50) | 50 | NULL allowed |  |
|  | OtherComments | varchar(50) | 50 | NULL allowed |  |
|  | ShippingName | varchar(1000) | 1000 | NULL allowed |  |
|  | ShippingMethod | varchar(50) | 50 | NULL allowed |  |
|  | SpecialEquipment | varchar(3000) | 3000 | NULL allowed |  |
|  | SpecialInstructions | varchar(3000) | 3000 | NULL allowed |  |
|  | DispatchNotes | varchar(6000) | 6000 | NULL allowed |  |
|  | DocumentType | varchar(50) | 50 | NULL allowed |  |
|  | Approval | varchar(50) | 50 | NULL allowed |  |
|  | ApprovalBy | varchar(50) | 50 | NULL allowed |  |
|  | ApprovalDate | datetime | 8 | NULL allowed |  |
|  | HazMat | varchar(50) | 50 | NULL allowed |  |
|  | Placards | varchar(50) | 50 | NULL allowed |  |
| [![Indexes hind_2098106515_1A_4A_5A_40A](../../../../Images/Index.png)](#indexes) | ProfileType | varchar(50) | 50 | NULL allowed |  |
|  | PMTote | numeric(18,4) | 9 | NULL allowed |  |
|  | PMGallon | numeric(18,4) | 9 | NULL allowed |  |
|  | PMDrum | numeric(18,4) | 9 | NULL allowed |  |
|  | PMBarrel | numeric(18,4) | 9 | NULL allowed |  |
|  | PTHour | numeric(18,4) | 9 | NULL allowed |  |
|  | PTLoad | numeric(18,4) | 9 | NULL allowed |  |
|  | PTGallon | numeric(18,4) | 9 | NULL allowed |  |
|  | PTDemurrage | numeric(18,2) | 9 | NULL allowed |  |
|  | PTFreeTime | numeric(18,0) | 9 | NULL allowed |  |
|  | PTFuelSerCharge | numeric(18,0) | 9 | NULL allowed |  |
|  | PTHourMin | numeric(18,2) | 9 | NULL allowed |  |
|  | PTGallonMin | numeric(18,2) | 9 | NULL allowed |  |
|  | PMTestType | varchar(50) | 50 | NULL allowed |  |
|  | PMTestBase | numeric(18,2) | 9 | NULL allowed |  |
|  | PMTestIncrement | numeric(18,2) | 9 | NULL allowed |  |
|  | PMTestTote | numeric(18,3) | 9 | NULL allowed |  |
|  | PMTestGallon | numeric(18,3) | 9 | NULL allowed |  |
|  | PMTestDrum | numeric(18,3) | 9 | NULL allowed |  |
|  | PMTestBarrel | numeric(18,2) | 9 | NULL allowed |  |
|  | PMSolidsTestType | varchar(50) | 50 | NULL allowed |  |
|  | PMSolidsBase | numeric(18,2) | 9 | NULL allowed |  |
|  | PMSolidsIncrement | numeric(18,2) | 9 | NULL allowed |  |
|  | PMSolidsTote | numeric(18,2) | 9 | NULL allowed |  |
|  | PMSolidsGallon | numeric(18,3) | 9 | NULL allowed |  |
|  | PMSolidsDrum | numeric(18,3) | 9 | NULL allowed |  |
|  | PMSolidsBarrel | numeric(18,3) | 9 | NULL allowed |  |
|  | PMMetals | numeric(18,2) | 9 | NULL allowed |  |
|  | PMAmmonia | numeric(18,2) | 9 | NULL allowed |  |
|  | HTYes | varchar(50) | 50 | NULL allowed |  |
|  | HTNo | varchar(50) | 50 | NULL allowed |  |
|  | HTPK | varchar(50) | 50 | NULL allowed |  |
|  | HTAD | varchar(50) | 50 | NULL allowed |  |
|  | MinFlashPoint | numeric(18,0) | 9 | NULL allowed |  |
|  | MaxCentrifugeSolidsPcnt | numeric(18,0) | 9 | NULL allowed |  |
|  | MaxFreePhaseWaterPcnt | numeric(18,0) | 9 | NULL allowed |  |
|  | MaxFreePhaseOrganicPcnt | numeric(18,0) | 9 | NULL allowed |  |
|  | MaxWaterByHach | numeric(18,0) | 9 | NULL allowed |  |
|  | MaxChlordetect | numeric(18,0) | 9 | NULL allowed |  |
|  | MaxViscosity | numeric(18,0) | 9 | NULL allowed |  |
|  | MaxTotalAcid | numeric(18,0) | 9 | NULL allowed |  |
|  | MinAPIGravity | numeric(18,0) | 9 | NULL allowed |  |
|  | MaxWaterByDistillationPcnt | numeric(18,0) | 9 | NULL allowed |  |
|  | MaxAshWtPcnt | numeric(18,0) | 9 | NULL allowed |  |
|  | MaxPPMP | numeric(18,0) | 9 | NULL allowed |  |
|  | MaxSulfur | numeric(18,0) | 9 | NULL allowed |  |
|  | Compatibility | varchar(3000) | 3000 | NULL allowed |  |
|  | ProductComments | varchar(3000) | 3000 | NULL allowed |  |
|  | MaxSilicone | numeric(18,0) | 9 | NULL allowed |  |
|  | MaxSodium | numeric(18,0) | 9 | NULL allowed |  |
|  | MaxVanadium | numeric(18,0) | 9 | NULL allowed |  |
|  | MaxAluminum | numeric(18,0) | 9 | NULL allowed |  |
|  | Notes | varchar(5000) | 5000 | NULL allowed |  |
| [![Indexes _dta_stat_2098106515_5_1_93](../../../../Images/Index.png)](#indexes) | SalesPersonId | varchar(50) | 50 | NULL allowed |  |
|  | Direction | varchar(50) | 50 | NULL allowed |  |
|  | Type | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_Profile_5_2098106515__K4_K1_96_100, _dta_stat_2098106515_96_4_3_2, _dta_stat_2098106515_96_3_2](../../../../Images/Index.png)](#indexes)(3) | Status | varchar(20) | 20 | NULL allowed |  |
|  | StatusDescription | varchar(2000) | 2000 | NULL allowed |  |
|  | SpecialBilling | bigint | 8 | NULL allowed |  |
|  | OldProfileId | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_Profile_5_2098106515__K4_K1_96_100](../../../../Images/Index.png)](#indexes) | EffectiveDate | datetime | 8 | NULL allowed |  |
|  | IndexName | varchar(50) | 50 | NULL allowed |  |
|  | IDiscountPcnt | numeric(18,3) | 9 | NULL allowed |  |
|  | IGallon | numeric(18,3) | 9 | NULL allowed |  |
|  | IBarrel | numeric(18,3) | 9 | NULL allowed |  |
|  | ContactName | varchar(50) | 50 | NULL allowed |  |
|  | ContactEmail | varchar(50) | 50 | NULL allowed |  |
|  | ContactPhone | varchar(50) | 50 | NULL allowed |  |
|  | ContactFax | varchar(50) | 50 | NULL allowed |  |
|  | DeepWell | varchar(50) | 50 | NULL allowed |  |
|  | ReviewedBySales | int | 4 | NULL allowed |  |
|  | ReviewedByDispatch | int | 4 | NULL allowed |  |
|  | BillingDepartment | varchar(100) | 100 | NULL allowed |  |
|  | UpdateDateTime | datetime | 8 | NULL allowed |  |
|  | UpdateUser | varchar(50) | 50 | NULL allowed |  |
|  | UpdateComputer | varchar(50) | 50 | NULL allowed |  |
|  | AirPermitTracking | varchar(3) | 3 | NULL allowed |  |
|  | MSDSFileName | varchar(600) | 600 | NULL allowed |  |
|  | MSDSUpdateUser | varchar(50) | 50 | NULL allowed |  |
|  | MSDSUpdateComputer | varchar(50) | 50 | NULL allowed |  |
|  | MSDSUpdateDateTime | datetime | 8 | NULL allowed |  |
|  | UOM | varchar(1) | 1 | NULL allowed |  |
|  | LinkProfileId | bigint | 8 | NULL allowed |  |
| [![Indexes _dta_stat_2098106515_123_2_3_4, _dta_stat_2098106515_1_123_2_3, _dta_stat_2098106515_1_4_2_6_3_9_123_155, _dta_stat_2098106515_1_4_123_2_3](../../../../Images/Index.png)](#indexes)(4) | DestinationId | bigint | 8 | NULL allowed |  |
|  | InactiveReviewed | bit | 1 | NULL allowed |  |
|  | InactiveExclude | bit | 1 | NULL allowed |  |
|  | CreateDate | datetime | 8 | NULL allowed |  |
|  | EPAWasteCode1 | varchar(10) | 10 | NULL allowed |  |
|  | EPAWasteCode2 | varchar(10) | 10 | NULL allowed |  |
|  | EPAWasteCode3 | varchar(10) | 10 | NULL allowed |  |
|  | EPAWasteCode4 | varchar(10) | 10 | NULL allowed |  |
|  | IndustrialCategory | varchar(20) | 20 | NULL allowed |  |
|  | GCApprovalDate | datetime | 8 | NULL allowed |  |
|  | LinkDirection | varchar(10) | 10 | NULL allowed |  |
|  | NewParkOnly | bit | 1 | NULL allowed |  |
|  | LandfillOnly | bit | 1 | NULL allowed |  |
|  | Clordtect | bit | 1 | NULL allowed |  |
|  | StatusChangeDate | datetime | 8 | NULL allowed |  |
|  | EstHours | varchar(50) | 50 | NULL allowed |  |
|  | DOTCorrosive | bit | 1 | NULL allowed |  |
|  | RiskFactor | int | 4 | NULL allowed |  |
|  | CreateUser | varchar(50) | 50 | NULL allowed |  |
|  | CreateDateTime | datetime | 8 | NULL allowed |  |
|  | CreateComputer | varchar(50) | 50 | NULL allowed |  |
|  | CSUCommercial | bit | 1 | NULL allowed |  |
|  | CSUOilBearing | bit | 1 | NULL allowed |  |
|  | CSUUsedOil | bit | 1 | NULL allowed |  |
|  | VaporPressure | varchar(50) | 50 | NULL allowed |  |
|  | VaporPressureOther | varchar(50) | 50 | NULL allowed |  |
|  | Benzene | varchar(50) | 50 | NULL allowed |  |
|  | BenzeneOther | varchar(50) | 50 | NULL allowed |  |
|  | TrailerLastLoadDescription | varchar(1000) | 1000 | NULL allowed |  |
|  | SageCustomerNo | varchar(20) | 20 | NULL allowed |  |
| [![Indexes _dta_stat_2098106515_1_4_2_6_3_9_123_155](../../../../Images/Index.png)](#indexes) | ServiceTypeId | bigint | 8 | NULL allowed |  |
|  | CompanyProfileNumber | varchar(100) | 100 | NULL allowed |  |
|  | CSRPersonId | varchar(50) | 50 | NULL allowed |  |
|  | WasteClass | varchar(3) | 3 | NULL allowed |  |
|  | EPAManifestFee | numeric(18,2) | 9 | NULL allowed |  |
|  | ManifestFee | numeric(18,2) | 9 | NULL allowed |  |
|  | PoNumber | varchar(50) | 50 | NULL allowed |  |
|  | PoNumberExpirationDate | date | 3 | NULL allowed |  |
|  | PMHydroCarbonTestType | varchar(50) | 50 | NULL allowed |  |
|  | PMHydroCarbonBase | numeric(18,2) | 9 | NULL allowed |  |
|  | PMHydroCarbonIncrement | numeric(18,2) | 9 | NULL allowed |  |
|  | PMHydroCarbonGallon | numeric(18,3) | 9 | NULL allowed |  |
|  | NESHAP | bit | 1 | NULL allowed |  |
|  | Product | varchar(20) | 20 | NULL allowed |  |
|  | ContractNumber | varchar(20) | 20 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Included Columns | Unique |
|---|---|---|---|---|
| [![Cluster Primary Key PK_Profile: Id](../../../../Images/pkcluster.png)](#indexes) | PK_Profile | Id |  | YES |
|  | Profile25 | Id, GeneratorId |  |  |
|  | _dta_index_Profile_5_2098106515__K4_K1_96_100 | GeneratorId, Id | Status, EffectiveDate |  |


---

## <a name="#statistics"></a>Statistics

| Name | Key Columns |
|---|---|
| _dta_stat_2098106515_123_2_3_4 | DestinationId, CustomerId, VendorId, GeneratorId |
| _dta_stat_2098106515_1_123_2_3 | Id, DestinationId, CustomerId, VendorId |
| _dta_stat_2098106515_1_3_4 | Id, VendorId, GeneratorId |
| _dta_stat_2098106515_1_4_123_2_3 | Id, GeneratorId, DestinationId, CustomerId, VendorId |
| _dta_stat_2098106515_1_4_2_6_3_9_123_155 | Id, GeneratorId, CustomerId, TransporterId, VendorId, MaterialCodeId, DestinationId, ServiceTypeId |
| _dta_stat_2098106515_2_3 | CustomerId, VendorId |
| _dta_stat_2098106515_4_1_2 | GeneratorId, Id, CustomerId |
| _dta_stat_2098106515_4_2_1_5 | GeneratorId, CustomerId, Id, ProfileNumber |
| _dta_stat_2098106515_4_3_2_5 | GeneratorId, VendorId, CustomerId, ProfileNumber |
| _dta_stat_2098106515_5_1_93 | ProfileNumber, Id, SalesPersonId |
| _dta_stat_2098106515_5_4_2 | ProfileNumber, GeneratorId, CustomerId |
| _dta_stat_2098106515_96_3_2 | Status, VendorId, CustomerId |
| _dta_stat_2098106515_96_4_3_2 | Status, GeneratorId, VendorId, CustomerId |
| hind_2098106515_1A_4A_5A_40A | Id, GeneratorId, ProfileNumber, ProfileType |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[Profile]
(
[Id] [bigint] NOT NULL IDENTITY(1, 1),
[CustomerId] [bigint] NULL,
[VendorId] [bigint] NULL,
[GeneratorId] [bigint] NULL,
[ProfileNumber] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[TransporterId] [bigint] NULL,
[LabTestSampleId] [bigint] NULL,
[WasteCode] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[MaterialCodeId] [int] NULL,
[ProductCategory] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[MaterialDescription] [varchar] (3000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ProcessDescription] [varchar] (3000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[MaterialClassification] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[StateWasteCode] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SICCode] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Volume] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[LoadFrequency] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Viscosity] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PhRange] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SpecificGravity] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[FlashPoint] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Phase] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ViscosityOther] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PhRangeOther] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SpecificGravityOther] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[FlashPointOther] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PhaseOther] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[OtherComments] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ShippingName] [varchar] (1000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ShippingMethod] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SpecialEquipment] [varchar] (3000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SpecialInstructions] [varchar] (3000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[DispatchNotes] [varchar] (6000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[DocumentType] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Approval] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ApprovalBy] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ApprovalDate] [datetime] NULL,
[HazMat] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Placards] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ProfileType] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PMTote] [numeric] (18, 4) NULL,
[PMGallon] [numeric] (18, 4) NULL,
[PMDrum] [numeric] (18, 4) NULL,
[PMBarrel] [numeric] (18, 4) NULL,
[PTHour] [numeric] (18, 4) NULL,
[PTLoad] [numeric] (18, 4) NULL,
[PTGallon] [numeric] (18, 4) NULL,
[PTDemurrage] [numeric] (18, 2) NULL,
[PTFreeTime] [numeric] (18, 0) NULL,
[PTFuelSerCharge] [numeric] (18, 0) NULL,
[PTHourMin] [numeric] (18, 2) NULL,
[PTGallonMin] [numeric] (18, 2) NULL,
[PMTestType] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PMTestBase] [numeric] (18, 2) NULL,
[PMTestIncrement] [numeric] (18, 2) NULL,
[PMTestTote] [numeric] (18, 3) NULL,
[PMTestGallon] [numeric] (18, 3) NULL,
[PMTestDrum] [numeric] (18, 3) NULL,
[PMTestBarrel] [numeric] (18, 2) NULL,
[PMSolidsTestType] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PMSolidsBase] [numeric] (18, 2) NULL,
[PMSolidsIncrement] [numeric] (18, 2) NULL,
[PMSolidsTote] [numeric] (18, 2) NULL,
[PMSolidsGallon] [numeric] (18, 3) NULL,
[PMSolidsDrum] [numeric] (18, 3) NULL,
[PMSolidsBarrel] [numeric] (18, 3) NULL,
[PMMetals] [numeric] (18, 2) NULL,
[PMAmmonia] [numeric] (18, 2) NULL,
[HTYes] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[HTNo] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[HTPK] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[HTAD] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[MinFlashPoint] [numeric] (18, 0) NULL,
[MaxCentrifugeSolidsPcnt] [numeric] (18, 0) NULL,
[MaxFreePhaseWaterPcnt] [numeric] (18, 0) NULL,
[MaxFreePhaseOrganicPcnt] [numeric] (18, 0) NULL,
[MaxWaterByHach] [numeric] (18, 0) NULL,
[MaxChlordetect] [numeric] (18, 0) NULL,
[MaxViscosity] [numeric] (18, 0) NULL,
[MaxTotalAcid] [numeric] (18, 0) NULL,
[MinAPIGravity] [numeric] (18, 0) NULL,
[MaxWaterByDistillationPcnt] [numeric] (18, 0) NULL,
[MaxAshWtPcnt] [numeric] (18, 0) NULL,
[MaxPPMP] [numeric] (18, 0) NULL,
[MaxSulfur] [numeric] (18, 0) NULL,
[Compatibility] [varchar] (3000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ProductComments] [varchar] (3000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[MaxSilicone] [numeric] (18, 0) NULL,
[MaxSodium] [numeric] (18, 0) NULL,
[MaxVanadium] [numeric] (18, 0) NULL,
[MaxAluminum] [numeric] (18, 0) NULL,
[Notes] [varchar] (5000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SalesPersonId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Direction] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Type] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Status] [varchar] (20) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[StatusDescription] [varchar] (2000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SpecialBilling] [bigint] NULL,
[OldProfileId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[EffectiveDate] [datetime] NULL,
[IndexName] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[IDiscountPcnt] [numeric] (18, 3) NULL,
[IGallon] [numeric] (18, 3) NULL,
[IBarrel] [numeric] (18, 3) NULL,
[ContactName] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ContactEmail] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ContactPhone] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ContactFax] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[DeepWell] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ReviewedBySales] [int] NULL,
[ReviewedByDispatch] [int] NULL,
[BillingDepartment] [varchar] (100) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[AirPermitTracking] [varchar] (3) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[MSDSFileName] [varchar] (600) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[MSDSUpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[MSDSUpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[MSDSUpdateDateTime] [datetime] NULL,
[UOM] [varchar] (1) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[LinkProfileId] [bigint] NULL,
[DestinationId] [bigint] NULL,
[InactiveReviewed] [bit] NULL,
[InactiveExclude] [bit] NULL,
[CreateDate] [datetime] NULL,
[EPAWasteCode1] [varchar] (10) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[EPAWasteCode2] [varchar] (10) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[EPAWasteCode3] [varchar] (10) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[EPAWasteCode4] [varchar] (10) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[IndustrialCategory] [varchar] (20) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[GCApprovalDate] [datetime] NULL,
[LinkDirection] [varchar] (10) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[NewParkOnly] [bit] NULL,
[LandfillOnly] [bit] NULL,
[Clordtect] [bit] NULL,
[StatusChangeDate] [datetime] NULL,
[EstHours] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[DOTCorrosive] [bit] NULL,
[RiskFactor] [int] NULL,
[CreateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateDateTime] [datetime] NULL,
[CreateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CSUCommercial] [bit] NULL,
[CSUOilBearing] [bit] NULL,
[CSUUsedOil] [bit] NULL,
[VaporPressure] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[VaporPressureOther] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Benzene] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[BenzeneOther] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[TrailerLastLoadDescription] [varchar] (1000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SageCustomerNo] [varchar] (20) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ServiceTypeId] [bigint] NULL,
[CompanyProfileNumber] [varchar] (100) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CSRPersonId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[WasteClass] [varchar] (3) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[EPAManifestFee] [numeric] (18, 2) NULL,
[ManifestFee] [numeric] (18, 2) NULL,
[PoNumber] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PoNumberExpirationDate] [date] NULL,
[PMHydroCarbonTestType] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PMHydroCarbonBase] [numeric] (18, 2) NULL,
[PMHydroCarbonIncrement] [numeric] (18, 2) NULL,
[PMHydroCarbonGallon] [numeric] (18, 3) NULL,
[NESHAP] [bit] NULL,
[Product] [varchar] (20) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ContractNumber] [varchar] (20) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[Profile] ADD CONSTRAINT [PK_Profile] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO
CREATE NONCLUSTERED INDEX [_dta_index_Profile_5_2098106515__K4_K1_96_100] ON [dbo].[Profile] ([GeneratorId], [Id]) INCLUDE ([Status], [EffectiveDate]) ON [PRIMARY]
GO
CREATE NONCLUSTERED INDEX [Profile25] ON [dbo].[Profile] ([Id], [GeneratorId]) ON [PRIMARY]
GO
CREATE STATISTICS [_dta_stat_2098106515_2_3] ON [dbo].[Profile] ([CustomerId], [VendorId])
GO
CREATE STATISTICS [_dta_stat_2098106515_123_2_3_4] ON [dbo].[Profile] ([DestinationId], [CustomerId], [VendorId], [GeneratorId])
GO
CREATE STATISTICS [_dta_stat_2098106515_4_2_1_5] ON [dbo].[Profile] ([GeneratorId], [CustomerId], [Id], [ProfileNumber])
GO
CREATE STATISTICS [_dta_stat_2098106515_4_1_2] ON [dbo].[Profile] ([GeneratorId], [Id], [CustomerId])
GO
CREATE STATISTICS [_dta_stat_2098106515_4_3_2_5] ON [dbo].[Profile] ([GeneratorId], [VendorId], [CustomerId], [ProfileNumber])
GO
CREATE STATISTICS [_dta_stat_2098106515_1_123_2_3] ON [dbo].[Profile] ([Id], [DestinationId], [CustomerId], [VendorId])
GO
CREATE STATISTICS [_dta_stat_2098106515_1_4_2_6_3_9_123_155] ON [dbo].[Profile] ([Id], [GeneratorId], [CustomerId], [TransporterId], [VendorId], [MaterialCodeId], [DestinationId], [ServiceTypeId])
GO
CREATE STATISTICS [_dta_stat_2098106515_1_4_123_2_3] ON [dbo].[Profile] ([Id], [GeneratorId], [DestinationId], [CustomerId], [VendorId])
GO
CREATE STATISTICS [hind_2098106515_1A_4A_5A_40A] ON [dbo].[Profile] ([Id], [GeneratorId], [ProfileNumber], [ProfileType])
GO
CREATE STATISTICS [_dta_stat_2098106515_1_3_4] ON [dbo].[Profile] ([Id], [VendorId], [GeneratorId])
GO
CREATE STATISTICS [_dta_stat_2098106515_5_4_2] ON [dbo].[Profile] ([ProfileNumber], [GeneratorId], [CustomerId])
GO
CREATE STATISTICS [_dta_stat_2098106515_5_1_93] ON [dbo].[Profile] ([ProfileNumber], [Id], [SalesPersonId])
GO
CREATE STATISTICS [_dta_stat_2098106515_96_4_3_2] ON [dbo].[Profile] ([Status], [GeneratorId], [VendorId], [CustomerId])
GO
CREATE STATISTICS [_dta_stat_2098106515_96_3_2] ON [dbo].[Profile] ([Status], [VendorId], [CustomerId])
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwChooseProfile]](../Views/dbo_vwChooseProfile.md)
* [[dbo].[vwCustomerGeneratorProfileReport]](../Views/dbo_vwCustomerGeneratorProfileReport.md)
* [[dbo].[vwCustomerGeneratorSort]](../Views/dbo_vwCustomerGeneratorSort.md)
* [[dbo].[vwExportLoadLabVolume]](../Views/dbo_vwExportLoadLabVolume.md)
* [[dbo].[vwExportLoadVolume]](../Views/dbo_vwExportLoadVolume.md)
* [[dbo].[vwGeneratorProfileSort]](../Views/dbo_vwGeneratorProfileSort.md)
* [[dbo].[vwLoadRequestProfileSalespersonFix]](../Views/dbo_vwLoadRequestProfileSalespersonFix.md)
* [[dbo].[vwProfileGrid]](../Views/dbo_vwProfileGrid.md)
* [[dbo].[vwProfilesActiveNoMSDS]](../Views/dbo_vwProfilesActiveNoMSDS.md)
* [[dbo].[vwRptLabTestForm]](../Views/dbo_vwRptLabTestForm.md)
* [[dbo].[vwRptLoadAccounting]](../Views/dbo_vwRptLoadAccounting.md)
* [[dbo].[vwRptLoadBillingAccounting]](../Views/dbo_vwRptLoadBillingAccounting.md)
* [[dbo].[vwRptLoadBillingAccountingNew]](../Views/dbo_vwRptLoadBillingAccountingNew.md)
* [[dbo].[vwRptLoadBillingDetail]](../Views/dbo_vwRptLoadBillingDetail.md)
* [[dbo].[vwRptLoadBOL]](../Views/dbo_vwRptLoadBOL.md)
* [[dbo].[vwRptLoadDriverTimeLog]](../Views/dbo_vwRptLoadDriverTimeLog.md)
* [[dbo].[vwRptLoadInternalTruck]](../Views/dbo_vwRptLoadInternalTruck.md)
* [[dbo].[vwRptLoadInternalTruckNew]](../Views/dbo_vwRptLoadInternalTruckNew.md)
* [[dbo].[vwRptLoadInventoryDetails]](../Views/dbo_vwRptLoadInventoryDetails.md)
* [[dbo].[vwRptLoadLabPadTimes]](../Views/dbo_vwRptLoadLabPadTimes.md)
* [[dbo].[vwRptLoadManifest]](../Views/dbo_vwRptLoadManifest.md)
* [[dbo].[vwRptLoadMaterialDestination]](../Views/dbo_vwRptLoadMaterialDestination.md)
* [[dbo].[vwRptLoadMaterialGenerator]](../Views/dbo_vwRptLoadMaterialGenerator.md)
* [[dbo].[vwRptLoadMaterialGeneratorKStarks]](../Views/dbo_vwRptLoadMaterialGeneratorKStarks.md)
* [[dbo].[vwRptLoadMaterialGeneratorKStarksProfileNo]](../Views/dbo_vwRptLoadMaterialGeneratorKStarksProfileNo.md)
* [[dbo].[vwRptLoadRequest]](../Views/dbo_vwRptLoadRequest.md)
* [[dbo].[vwRptLoadSchedule]](../Views/dbo_vwRptLoadSchedule.md)
* [[dbo].[vwRptLoadScheduleByPump]](../Views/dbo_vwRptLoadScheduleByPump.md)
* [[dbo].[vwRptLoadScheduleNew]](../Views/dbo_vwRptLoadScheduleNew.md)
* [[dbo].[vwRptLoadsTrailerStorage]](../Views/dbo_vwRptLoadsTrailerStorage.md)
* [[dbo].[vwRptLoadTCEQ]](../Views/dbo_vwRptLoadTCEQ.md)
* [[dbo].[vwRptProfileBol]](../Views/dbo_vwRptProfileBol.md)
* [[dbo].[vwRptProfileForm]](../Views/dbo_vwRptProfileForm.md)
* [[dbo].[vwRptProfileFormProduct]](../Views/dbo_vwRptProfileFormProduct.md)
* [[dbo].[vwRptProfileManifest]](../Views/dbo_vwRptProfileManifest.md)
* [[dbo].[vwRptProfileTCEQ]](../Views/dbo_vwRptProfileTCEQ.md)
* [[dbo].[vwRptSelectSchedulePumpTimes]](../Views/dbo_vwRptSelectSchedulePumpTimes.md)
* [[dbo].[vwRptSelectScheduleTimes]](../Views/dbo_vwRptSelectScheduleTimes.md)
* [[dbo].[vwRptWasteLoads]](../Views/dbo_vwRptWasteLoads.md)
* [[dbo].[vwSaturnTestProfile]](../Views/dbo_vwSaturnTestProfile.md)
* [[dbo].[vwSelectAvailableForScheduledLoadsAll]](../Views/dbo_vwSelectAvailableForScheduledLoadsAll.md)
* [[dbo].[vwSelectAvailableForScheduledLoadsPending]](../Views/dbo_vwSelectAvailableForScheduledLoadsPending.md)
* [[dbo].[vwSelectAvailableForScheduledLoadsScheduled]](../Views/dbo_vwSelectAvailableForScheduledLoadsScheduled.md)
* [[dbo].[vwSelectCustomerStopInformation]](../Views/dbo_vwSelectCustomerStopInformation.md)
* [[dbo].[vwSelectCustomerStopInformationLoadRequest]](../Views/dbo_vwSelectCustomerStopInformationLoadRequest.md)
* [[dbo].[vwSelectEManifest]](../Views/dbo_vwSelectEManifest.md)
* [[dbo].[vwSelectEmergencyContactNumber]](../Views/dbo_vwSelectEmergencyContactNumber.md)
* [[dbo].[vwSelectEquipmentLastLoadDescription]](../Views/dbo_vwSelectEquipmentLastLoadDescription.md)
* [[dbo].[vwSelectExportBayportTimes]](../Views/dbo_vwSelectExportBayportTimes.md)
* [[dbo].[vwSelectExportIntergulfDriversOnSiteTime]](../Views/dbo_vwSelectExportIntergulfDriversOnSiteTime.md)
* [[dbo].[vwSelectExportLoadLabVolume]](../Views/dbo_vwSelectExportLoadLabVolume.md)
* [[dbo].[vwSelectExportLoadLabVolumeNew]](../Views/dbo_vwSelectExportLoadLabVolumeNew.md)
* [[dbo].[vwSelectExportLoadsForEBE]](../Views/dbo_vwSelectExportLoadsForEBE.md)
* [[dbo].[vwSelectExportLoadsForEBETemp]](../Views/dbo_vwSelectExportLoadsForEBETemp.md)
* [[dbo].[vwSelectExportLoadsForSchedule]](../Views/dbo_vwSelectExportLoadsForSchedule.md)
* [[dbo].[vwSelectExportLoadsForSteers]](../Views/dbo_vwSelectExportLoadsForSteers.md)
* [[dbo].[vwSelectExportProfileNewBusiness]](../Views/dbo_vwSelectExportProfileNewBusiness.md)
* [[dbo].[vwSelectExportProfiles]](../Views/dbo_vwSelectExportProfiles.md)
* [[dbo].[vwSelectExportProfilesApprovalDays]](../Views/dbo_vwSelectExportProfilesApprovalDays.md)
* [[dbo].[vwSelectExportProfilesNew]](../Views/dbo_vwSelectExportProfilesNew.md)
* [[dbo].[vwSelectExportProfileVolume]](../Views/dbo_vwSelectExportProfileVolume.md)
* [[dbo].[vwSelectExportStrangTimes]](../Views/dbo_vwSelectExportStrangTimes.md)
* [[dbo].[vwSelectExportToSage]](../Views/dbo_vwSelectExportToSage.md)
* [[dbo].[vwSelectExportToSageAccrual]](../Views/dbo_vwSelectExportToSageAccrual.md)
* [[dbo].[vwSelectExportToSageTest]](../Views/dbo_vwSelectExportToSageTest.md)
* [[dbo].[vwSelectGeneratorProfilePricing]](../Views/dbo_vwSelectGeneratorProfilePricing.md)
* [[dbo].[vwSelectLabTest]](../Views/dbo_vwSelectLabTest.md)
* [[dbo].[vwSelectLastLoadInformation]](../Views/dbo_vwSelectLastLoadInformation.md)
* [[dbo].[vwSelectLoadCTCount]](../Views/dbo_vwSelectLoadCTCount.md)
* [[dbo].[vwSelectLoadForSchedule]](../Views/dbo_vwSelectLoadForSchedule.md)
* [[dbo].[vwSelectLoadLabCopper06087]](../Views/dbo_vwSelectLoadLabCopper06087.md)
* [[dbo].[vwSelectLoadPadTimesForExport]](../Views/dbo_vwSelectLoadPadTimesForExport.md)
* [[dbo].[vwSelectLoadProfileMaterialCode]](../Views/dbo_vwSelectLoadProfileMaterialCode.md)
* [[dbo].[vwSelectLoadRequest]](../Views/dbo_vwSelectLoadRequest.md)
* [[dbo].[vwSelectLoadRequestForOverage]](../Views/dbo_vwSelectLoadRequestForOverage.md)
* [[dbo].[vwSelectLoadRequestForSchedule]](../Views/dbo_vwSelectLoadRequestForSchedule.md)
* [[dbo].[vwSelectLoadRequestProfileMaterialCode]](../Views/dbo_vwSelectLoadRequestProfileMaterialCode.md)
* [[dbo].[vwSelectLoadRequestsLeadTimes]](../Views/dbo_vwSelectLoadRequestsLeadTimes.md)
* [[dbo].[vwSelectLoadRequestSP]](../Views/dbo_vwSelectLoadRequestSP.md)
* [[dbo].[vwSelectLoads]](../Views/dbo_vwSelectLoads.md)
* [[dbo].[vwSelectLoads4thQtrBayportLoadTimes]](../Views/dbo_vwSelectLoads4thQtrBayportLoadTimes.md)
* [[dbo].[vwSelectLoadsByProfileCreateDate]](../Views/dbo_vwSelectLoadsByProfileCreateDate.md)
* [[dbo].[vwSelectLoadsCount]](../Views/dbo_vwSelectLoadsCount.md)
* [[dbo].[vwSelectLoadsEManifestCheck]](../Views/dbo_vwSelectLoadsEManifestCheck.md)
* [[dbo].[vwSelectLoadsFor225ByMonth]](../Views/dbo_vwSelectLoadsFor225ByMonth.md)
* [[dbo].[vwSelectLoadsForBayportCWaste]](../Views/dbo_vwSelectLoadsForBayportCWaste.md)
* [[dbo].[vwSelectLoadsForBayportTurnTimes]](../Views/dbo_vwSelectLoadsForBayportTurnTimes.md)
* [[dbo].[vwSelectLoadsForSaturn]](../Views/dbo_vwSelectLoadsForSaturn.md)
* [[dbo].[vwSelectLoadsInactive]](../Views/dbo_vwSelectLoadsInactive.md)
* [[dbo].[vwSelectLoadsLabForAProfile]](../Views/dbo_vwSelectLoadsLabForAProfile.md)
* [[dbo].[vwSelectLoadsMotiva20121001]](../Views/dbo_vwSelectLoadsMotiva20121001.md)
* [[dbo].[vwSelectLoadsScheduled]](../Views/dbo_vwSelectLoadsScheduled.md)
* [[dbo].[vwSelectLoadsScheduledForChart]](../Views/dbo_vwSelectLoadsScheduledForChart.md)
* [[dbo].[vwSelectLoadsScheduleForExport]](../Views/dbo_vwSelectLoadsScheduleForExport.md)
* [[dbo].[vwSelectLoadsWithProfileExpDateToMarkInactive]](../Views/dbo_vwSelectLoadsWithProfileExpDateToMarkInactive.md)
* [[dbo].[vwSelectMonthlyDischarge]](../Views/dbo_vwSelectMonthlyDischarge.md)
* [[dbo].[vwSelectPendingLoads]](../Views/dbo_vwSelectPendingLoads.md)
* [[dbo].[vwSelectProfileActiveLastLoadDate]](../Views/dbo_vwSelectProfileActiveLastLoadDate.md)
* [[dbo].[vwSelectProfileActiveLastLoadDateNew]](../Views/dbo_vwSelectProfileActiveLastLoadDateNew.md)
* [[dbo].[vwSelectProfileBlinds]](../Views/dbo_vwSelectProfileBlinds.md)
* [[dbo].[vwSelectProfileBlindsBothSides]](../Views/dbo_vwSelectProfileBlindsBothSides.md)
* [[dbo].[vwSelectProfileFixExpirationDate]](../Views/dbo_vwSelectProfileFixExpirationDate.md)
* [[dbo].[vwSelectProfileForSales]](../Views/dbo_vwSelectProfileForSales.md)
* [[dbo].[vwSelectProfileInformation]](../Views/dbo_vwSelectProfileInformation.md)
* [[dbo].[vwSelectProfileManifestFee]](../Views/dbo_vwSelectProfileManifestFee.md)
* [[dbo].[vwSelectProfileOneTimeOnly]](../Views/dbo_vwSelectProfileOneTimeOnly.md)
* [[dbo].[vwSelectProfilePOInformation]](../Views/dbo_vwSelectProfilePOInformation.md)
* [[dbo].[vwSelectProfilePrePrint]](../Views/dbo_vwSelectProfilePrePrint.md)
* [[dbo].[vwSelectProfileProduct]](../Views/dbo_vwSelectProfileProduct.md)
* [[dbo].[vwSelectProfileProperShippingName]](../Views/dbo_vwSelectProfileProperShippingName.md)
* [[dbo].[vwSelectProfileRecertificationDays]](../Views/dbo_vwSelectProfileRecertificationDays.md)
* [[dbo].[vwSelectProfileReviewForMarc]](../Views/dbo_vwSelectProfileReviewForMarc.md)
* [[dbo].[vwSelectProfilesInactive]](../Views/dbo_vwSelectProfilesInactive.md)
* [[dbo].[vwSelectProfilesInReviewNextReviewUser]](../Views/dbo_vwSelectProfilesInReviewNextReviewUser.md)
* [[dbo].[vwSelectProfilesInReviewNextUser]](../Views/dbo_vwSelectProfilesInReviewNextUser.md)
* [[dbo].[vwSelectProfilesWithErrors]](../Views/dbo_vwSelectProfilesWithErrors.md)
* [[dbo].[vwSelectProfileVolumeQuantity]](../Views/dbo_vwSelectProfileVolumeQuantity.md)
* [[dbo].[vwSelectProfileVolumeTest]](../Views/dbo_vwSelectProfileVolumeTest.md)
* [[dbo].[vwSelectProfileWaste]](../Views/dbo_vwSelectProfileWaste.md)
* [[dbo].[vwSelectRequestedLoads]](../Views/dbo_vwSelectRequestedLoads.md)
* [[dbo].[vwSelectReviewProfileProperShippingName]](../Views/dbo_vwSelectReviewProfileProperShippingName.md)
* [[dbo].[vwSelectSaturnTransactions]](../Views/dbo_vwSelectSaturnTransactions.md)
* [[dbo].[vwSelectSaturnTransactionsBackup]](../Views/dbo_vwSelectSaturnTransactionsBackup.md)
* [[dbo].[vwSelectSaturnTransactionsLoads]](../Views/dbo_vwSelectSaturnTransactionsLoads.md)
* [[dbo].[vwSelectScheduledLoads]](../Views/dbo_vwSelectScheduledLoads.md)
* [[dbo].[vwSelectTrailerLastLoad]](../Views/dbo_vwSelectTrailerLastLoad.md)
* [[dbo].[vwSelectTrailerScheduledLoads]](../Views/dbo_vwSelectTrailerScheduledLoads.md)
* [[dbo].[vwSteersTest]](../Views/dbo_vwSteersTest.md)
* [[dbo].[fnSelectCustomerActiveProfile]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnSelectCustomerActiveProfile.md)
* [[dbo].[fnSelectOneLabTest]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectOneLabTest.md)
* [[dbo].[fnSelectOneProfile]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectOneProfile.md)
* [[dbo].[fnSelectProfile]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectProfile.md)
* [[dbo].[fnSelectScheduledLoads]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectScheduledLoads.md)
* [[dbo].[fnTrailerLastLoadDescription]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnTrailerLastLoadDescription.md)
* [[dbo].[fnTrailerLastLoadId]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnTrailerLastLoadId.md)
* [[dbo].[fnTrailerTest]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnTrailerTest.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

