#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwRptLabTestForm

# ![Views](../../../../Images/View32.png) [dbo].[vwRptLabTestForm]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 9:56:51 PM Tuesday, August 7, 2012 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| TestDate | datetime | 8 |
| LoadId | decimal(18,0) | 9 |
| Customer Name | varchar(50) | 50 |
| Generator Name | varchar(100) | 100 |
| Profile Number | varchar(50) | 50 |
| DocumentNumber | varchar(50) | 50 |
| DocumentType | varchar(50) | 50 |
| TruckNumber | varchar(50) | 50 |
| Transporter Name | varchar(50) | 50 |
| Driver FName | varchar(50) | 50 |
| Driver LName | varchar(50) | 50 |
| Lab FName | varchar(50) | 50 |
| Lab Lname | varchar(50) | 50 |
| StartTime | datetime | 8 |
| EndTime | datetime | 8 |
| GrossWeight | decimal(18,0) | 9 |
| TareWeight | decimal(18,0) | 9 |
| Quantity | decimal(18,0) | 9 |
| Units | varchar(50) | 50 |
| WeightTicketNumber | varchar(50) | 50 |
| PreAdjAPI | varchar(5) | 5 |
| AdjAPI | decimal(18,1) | 9 |
| PreFlashPoint | varchar(5) | 5 |
| FlashPoint | decimal(18,0) | 9 |
| PreAPI | varchar(5) | 5 |
| API | decimal(18,1) | 9 |
| PreTemperature | varchar(50) | 50 |
| Temperature | decimal(18,0) | 9 |
| WashOut | varchar(50) | 50 |
| Compatibility | varchar(50) | 50 |
| PcntOil | decimal(18,0) | 9 |
| PcntWater | decimal(18,0) | 9 |
| PcntSolids | decimal(18,0) | 9 |
| PrePetroleumFlashPoint | varchar(5) | 5 |
| PetroleumFlashPoint | decimal(18,0) | 9 |
| PrePetroleumAPI | varchar(5) | 5 |
| PetroleumAPI | decimal(18,1) | 9 |
| PrePetroleumTemp | varchar(5) | 5 |
| PetroleumTemp | decimal(18,0) | 9 |
| PrePetroleumChlordetect | varchar(5) | 5 |
| PetroleumChlordetect | decimal(18,0) | 9 |
| PrePetroleumAsh | varchar(5) | 5 |
| PetroleumAsh | decimal(18,4) | 9 |
| PrePetroleumPcntWater | varchar(5) | 5 |
| PetroleumPcntWater | decimal(18,1) | 9 |
| PreAqueousCOD | varchar(5) | 5 |
| AqueousCOD | decimal(18,0) | 9 |
| PreAqueousAPI | varchar(5) | 5 |
| AqueousAPI | decimal(18,1) | 9 |
| PreAqueousTemp | varchar(5) | 5 |
| AqueousTemp | decimal(18,0) | 9 |
| PreAqueousPH | varchar(5) | 5 |
| AqueousPH | decimal(18,1) | 9 |
| PreAqueousAmmonia | varchar(5) | 5 |
| AqueousAmmonia | decimal(18,0) | 9 |
| PreAqueousZinc | varchar(5) | 5 |
| AqueousZinc | decimal(18,0) | 9 |
| PreAqueousCopper | varchar(50) | 50 |
| AqueousCopper | decimal(18,0) | 9 |
| Notes | varchar(5000) | 5000 |
| Status | varchar(50) | 50 |
| StatusDescription | varchar(2000) | 2000 |
| ReportTo | varchar(50) | 50 |
| PrePetroleumAdjAPI | varchar(5) | 5 |
| PetroleumAdjAPI | decimal(18,1) | 9 |
| PreAqueousFlashPoint | varchar(5) | 5 |
| AqueousFlashPoint | decimal(18,0) | 9 |
| PreAqueousAdjAPI | varchar(5) | 5 |
| AqueousAdjAPI | decimal(18,1) | 9 |
| Location | varchar(50) | 50 |
| Destination | varchar(50) | 50 |
| AirPermitTracking | varchar(3) | 3 |
| HandlingCode | varchar(10) | 10 |
| PcntRags | decimal(18,0) | 9 |
| PrePetroleumPour | varchar(5) | 5 |
| PetroleumPour | decimal(18,0) | 9 |
| PreAqueousToc | varchar(5) | 5 |
| AqueousToc | decimal(18,0) | 9 |
| Hazard | varchar(3) | 3 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwRptLabTestForm]
AS
SELECT     dbo.LabTest.Id, dbo.LabTest.TestDate, dbo.LabTest.LoadId, dbo.Customer.Name AS [Customer Name], dbo.Generator.Name AS [Generator Name], 
                      dbo.Profile.ProfileNumber AS [Profile Number], dbo.LabTest.DocumentNumber, dbo.LabTest.DocumentType, dbo.LabTest.TruckNumber, 
                      dbo.Transporter.Name AS [Transporter Name], dbo.Driver.FirstName AS [Driver FName], dbo.Driver.LastName AS [Driver LName], 
                      dbo.UserMaster.FirstName AS [Lab FName], dbo.UserMaster.LastName AS [Lab Lname], dbo.LabTest.StartTime, dbo.LabTest.EndTime, 
                      dbo.LabTest.GrossWeight, dbo.LabTest.TareWeight, dbo.LabTest.Quantity, dbo.LabTest.Units, dbo.LabTest.WeightTicketNumber, 
                      dbo.LabTest.PreAdjAPI, dbo.LabTest.AdjAPI, dbo.LabTest.PreFlashPoint, dbo.LabTest.FlashPoint, dbo.LabTest.PreAPI, dbo.LabTest.API, 
                      dbo.LabTest.PreTemperature, dbo.LabTest.Temperature, dbo.LabTest.WashOut, dbo.LabTest.Compatibility, dbo.LabTest.PcntOil, 
                      dbo.LabTest.PcntWater, dbo.LabTest.PcntSolids, dbo.LabTest.PrePetroleumFlashPoint, dbo.LabTest.PetroleumFlashPoint, 
                      dbo.LabTest.PrePetroleumAPI, dbo.LabTest.PetroleumAPI, dbo.LabTest.PrePetroleumTemp, dbo.LabTest.PetroleumTemp, 
                      dbo.LabTest.PrePetroleumChlordetect, dbo.LabTest.PetroleumChlordetect, dbo.LabTest.PrePetroleumAsh, dbo.LabTest.PetroleumAsh, 
                      dbo.LabTest.PrePetroleumPcntWater, dbo.LabTest.PetroleumPcntWater, dbo.LabTest.PreAqueousCOD, dbo.LabTest.AqueousCOD, 
                      dbo.LabTest.PreAqueousAPI, dbo.LabTest.AqueousAPI, dbo.LabTest.PreAqueousTemp, dbo.LabTest.AqueousTemp, dbo.LabTest.PreAqueousPH, 
                      dbo.LabTest.AqueousPH, dbo.LabTest.PreAqueousAmmonia, dbo.LabTest.AqueousAmmonia, dbo.LabTest.PreAqueousZinc, dbo.LabTest.AqueousZinc, 
                      dbo.LabTest.PreAqueousCopper, dbo.LabTest.AqueousCopper, dbo.LabTest.Notes, dbo.LabTest.Status, dbo.LabTest.StatusDescription, 
                      dbo.LabTest.ReportTo, dbo.LabTest.PrePetroleumAdjAPI, dbo.LabTest.PetroleumAdjAPI, dbo.LabTest.PreAqueousFlashPoint, 
                      dbo.LabTest.AqueousFlashPoint, dbo.LabTest.PreAqueousAdjAPI, dbo.LabTest.AqueousAdjAPI, dbo.LabTest.Location, dbo.LabTest.Destination, 
                      dbo.LabTest.AirPermitTracking, dbo.LabTest.HandlingCode, dbo.LabTest.PcntRags, dbo.LabTest.PrePetroleumPour, dbo.LabTest.PetroleumPour, 
                      dbo.LabTest.PreAqueousToc, dbo.LabTest.AqueousToc, dbo.fnProfileHazardYesNo(dbo.Profile.HTYes) AS Hazard
FROM         dbo.Generator RIGHT OUTER JOIN
                      dbo.Profile ON dbo.Generator.Id = dbo.Profile.GeneratorId LEFT OUTER JOIN
                      dbo.Customer ON dbo.Profile.CustomerId = dbo.Customer.Id RIGHT OUTER JOIN
                      dbo.LabTest LEFT OUTER JOIN
                      dbo.Transporter ON dbo.LabTest.TransporterId = dbo.Transporter.Id LEFT OUTER JOIN
                      dbo.Driver ON dbo.LabTest.DriverId = dbo.Driver.Id LEFT OUTER JOIN
                      dbo.UserMaster ON dbo.LabTest.LabTechId = dbo.UserMaster.UserName ON dbo.Profile.Id = dbo.LabTest.ProfileId

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Customer]](../Tables/dbo_Customer.md)
* [[dbo].[Driver]](../Tables/dbo_Driver.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[LabTest]](../Tables/dbo_LabTest.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[Transporter]](../Tables/dbo_Transporter.md)
* [[dbo].[UserMaster]](../Tables/dbo_UserMaster.md)
* [[dbo].[fnProfileHazardYesNo]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnProfileHazardYesNo.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

