#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectProfileProduct

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectProfileProduct]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 10:45:45 AM Wednesday, August 27, 2014 |
| Last Modified | 9:02:13 PM Monday, September 12, 2022 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| Id | bigint | 8 | 0 - 0 |
| PMTote | numeric(18,4) | 9 |  |
| PMGallon | numeric(18,4) | 9 |  |
| PMDrum | numeric(18,4) | 9 |  |
| PMBarrel | numeric(18,4) | 9 |  |
| PTHour | numeric(18,4) | 9 |  |
| PTLoad | numeric(18,4) | 9 |  |
| PTGallon | numeric(18,4) | 9 |  |
| PTDemurrage | numeric(18,2) | 9 |  |
| PTFreeTime | numeric(18,0) | 9 |  |
| PTFuelSerCharge | numeric(18,0) | 9 |  |
| PTHourMin | numeric(18,2) | 9 |  |
| PTGallonMin | numeric(18,2) | 9 |  |
| IndexName | varchar(50) | 50 |  |
| IDiscountPcnt | numeric(18,3) | 9 |  |
| IGallon | numeric(18,3) | 9 |  |
| IBarrel | numeric(18,3) | 9 |  |
| EstHours | varchar(50) | 50 |  |
| HTYes | varchar(50) | 50 |  |
| WasteCode | varchar(50) | 50 |  |
| DOTCorrosive | bit | 1 |  |
| EPAWasteCode1 | varchar(10) | 10 |  |
| EPAWasteCode2 | varchar(10) | 10 |  |
| EPAWasteCode3 | varchar(10) | 10 |  |
| EPAWasteCode4 | varchar(10) | 10 |  |
| NESHAP | bit | 1 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectProfileProduct]
AS
SELECT        Id, PMTote, PMGallon, PMDrum, PMBarrel, PTHour, PTLoad, PTGallon, PTDemurrage, PTFreeTime, PTFuelSerCharge, PTHourMin, PTGallonMin, IndexName, IDiscountPcnt, IGallon, IBarrel, EstHours, HTYes, 
                         WasteCode, DOTCorrosive, EPAWasteCode1, EPAWasteCode2, EPAWasteCode3, EPAWasteCode4, NESHAP
FROM            dbo.Profile
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

