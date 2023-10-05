#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectProfileWaste

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectProfileWaste]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 10:45:52 AM Wednesday, August 27, 2014 |
| Last Modified | 9:02:24 PM Monday, September 12, 2022 |


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
| PMTestType | varchar(50) | 50 |  |
| PMTestBase | numeric(18,2) | 9 |  |
| PMTestIncrement | numeric(18,2) | 9 |  |
| PMTestTote | numeric(18,3) | 9 |  |
| PMTestGallon | numeric(18,3) | 9 |  |
| PMTestDrum | numeric(18,3) | 9 |  |
| PMTestBarrel | numeric(18,2) | 9 |  |
| PMSolidsTestType | varchar(50) | 50 |  |
| PMSolidsBase | numeric(18,2) | 9 |  |
| PMSolidsIncrement | numeric(18,2) | 9 |  |
| PMSolidsTote | numeric(18,2) | 9 |  |
| PMSolidsGallon | numeric(18,3) | 9 |  |
| PMSolidsDrum | numeric(18,3) | 9 |  |
| PMSolidsBarrel | numeric(18,3) | 9 |  |
| PMMetals | numeric(18,2) | 9 |  |
| PMAmmonia | numeric(18,2) | 9 |  |
| SpecialBilling | bigint | 8 |  |
| EstHours | varchar(50) | 50 |  |
| HTYes | varchar(50) | 50 |  |
| WasteCode | varchar(50) | 50 |  |
| DOTCorrosive | bit | 1 |  |
| PMHydroCarbonTestType | varchar(50) | 50 |  |
| PMHydroCarbonBase | numeric(18,2) | 9 |  |
| PMHydroCarbonIncrement | numeric(18,2) | 9 |  |
| PMHydroCarbonGallon | numeric(18,3) | 9 |  |
| EPAWasteCode1 | varchar(10) | 10 |  |
| EPAWasteCode2 | varchar(10) | 10 |  |
| EPAWasteCode3 | varchar(10) | 10 |  |
| EPAWasteCode4 | varchar(10) | 10 |  |
| NESHAP | bit | 1 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectProfileWaste]
AS
SELECT        Id, PMTote, PMGallon, PMDrum, PMBarrel, PTHour, PTLoad, PTGallon, PTDemurrage, PTFreeTime, PTFuelSerCharge, PTHourMin, PTGallonMin, PMTestType, PMTestBase, PMTestIncrement, PMTestTote, 
                         PMTestGallon, PMTestDrum, PMTestBarrel, PMSolidsTestType, PMSolidsBase, PMSolidsIncrement, PMSolidsTote, PMSolidsGallon, PMSolidsDrum, PMSolidsBarrel, PMMetals, PMAmmonia, SpecialBilling, 
                         EstHours, HTYes, WasteCode, DOTCorrosive, PMHydroCarbonTestType, PMHydroCarbonBase, PMHydroCarbonIncrement, PMHydroCarbonGallon, EPAWasteCode1, EPAWasteCode2, EPAWasteCode3, 
                         EPAWasteCode4, NESHAP
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

