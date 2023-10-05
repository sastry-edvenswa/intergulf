#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwRptTankTurnLabTest

# ![Views](../../../../Images/View32.png) [dbo].[vwRptTankTurnLabTest]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 11:03:38 PM Tuesday, August 28, 2007 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| Tank | varchar(50) | 50 |
| Turn | varchar(50) | 50 |
| Location | varchar(50) | 50 |
| LabTechId | varchar(50) | 50 |
| TestDate | datetime | 8 |
| PreFlashPoint | varchar(1) | 1 |
| FlashPoint | numeric(18,3) | 9 |
| PreAPI | varchar(1) | 1 |
| API | numeric(18,3) | 9 |
| PreAPITemp | varchar(1) | 1 |
| APITemp | numeric(18,0) | 9 |
| PreAdjAPI | varchar(1) | 1 |
| AdjAPI | numeric(18,3) | 9 |
| PrePcntWater | varchar(1) | 1 |
| PcntWater | numeric(18,3) | 9 |
| PrePcntAsh | varchar(1) | 1 |
| PcntAsh | numeric(18,3) | 9 |
| PreChlordetect | varchar(1) | 1 |
| Chlordetect | numeric(18,3) | 9 |
| PreViscosity | varchar(1) | 1 |
| Viscosity | numeric(18,3) | 9 |
| PreSilicon | varchar(1) | 1 |
| Silicon | numeric(18,3) | 9 |
| PreSodium | varchar(1) | 1 |
| Sodium | numeric(18,3) | 9 |
| PreAluminum | varchar(1) | 1 |
| Aluminum | numeric(18,3) | 9 |
| PreVanadium | varchar(1) | 1 |
| Vanadium | numeric(18,3) | 9 |
| TankLevel | varchar(50) | 50 |
| Comments | varchar(3000) | 3000 |
| ApprovedById | varchar(50) | 50 |
| Status | varchar(50) | 50 |
| LabTech FirstName | varchar(50) | 50 |
| LabTech LastName | varchar(50) | 50 |
| PreSulfur | varchar(1) | 1 |
| Sulfur | numeric(18,3) | 9 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE  View [dbo].[vwRptTankTurnLabTest]
as
SELECT     dbo.TankTest.Id, dbo.TankTest.Tank, dbo.TankTest.Turn, dbo.TankTest.Location, dbo.TankTest.LabTechId, dbo.TankTest.TestDate, 
                      dbo.TankTest.PreFlashPoint, dbo.TankTest.FlashPoint, dbo.TankTest.PreAPI, dbo.TankTest.API, dbo.TankTest.PreAPITemp, dbo.TankTest.APITemp, 
                      dbo.TankTest.PreAdjAPI, dbo.TankTest.AdjAPI, dbo.TankTest.PrePcntWater, dbo.TankTest.PcntWater, dbo.TankTest.PrePcntAsh, dbo.TankTest.PcntAsh, 
                      dbo.TankTest.PreChlordetect, dbo.TankTest.Chlordetect, dbo.TankTest.PreViscosity, dbo.TankTest.Viscosity, dbo.TankTest.PreSilicon, 
                      dbo.TankTest.Silicon, dbo.TankTest.PreSodium, dbo.TankTest.Sodium, dbo.TankTest.PreAluminum, dbo.TankTest.Aluminum, 
                      dbo.TankTest.PreVanadium, dbo.TankTest.Vanadium, dbo.TankTest.TankLevel, dbo.TankTest.Comments, dbo.TankTest.ApprovedById, 
                      dbo.TankTest.Status, dbo.UserMaster.FirstName AS [LabTech FirstName], dbo.UserMaster.LastName AS [LabTech LastName], dbo.TankTest.PreSulfur, 
                      dbo.TankTest.Sulfur
FROM         dbo.TankTest LEFT OUTER JOIN
                      dbo.UserMaster ON dbo.TankTest.LabTechId = dbo.UserMaster.UserName
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[TankTest]](../Tables/dbo_TankTest.md)
* [[dbo].[UserMaster]](../Tables/dbo_UserMaster.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

