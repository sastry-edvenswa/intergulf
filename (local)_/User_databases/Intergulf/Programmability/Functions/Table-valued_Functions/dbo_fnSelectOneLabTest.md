#### 

[Project](../../../../../../index.md) > [(local)\\](../../../../../index.md) > [User databases](../../../../index.md) > [Intergulf](../../../index.md) > Programmability > Functions > [Table-valued Functions](Table-valued_Functions.md) > dbo.fnSelectOneLabTest

# ![Table-valued Functions](../../../../../../Images/Function_Table32.png) [dbo].[fnSelectOneLabTest]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| ANSI Nulls On | NO |
| Quoted Identifier On | YES |


---

## <a name="#parameters"></a>Parameters

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| @Id | int | 4 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
SET ANSI_NULLS OFF
GO


CREATE   FUNCTION [dbo].[fnSelectOneLabTest]
                 (@Id as int)
RETURNS table
AS
RETURN (
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
       WHERE dbo.LabTest.Id = @Id
       )






GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Customer]](../../../Tables/dbo_Customer.md)
* [[dbo].[Driver]](../../../Tables/dbo_Driver.md)
* [[dbo].[Generator]](../../../Tables/dbo_Generator.md)
* [[dbo].[LabTest]](../../../Tables/dbo_LabTest.md)
* [[dbo].[Profile]](../../../Tables/dbo_Profile.md)
* [[dbo].[Transporter]](../../../Tables/dbo_Transporter.md)
* [[dbo].[UserMaster]](../../../Tables/dbo_UserMaster.md)
* [[dbo].[fnProfileHazardYesNo]](../Scalar-valued_Functions/dbo_fnProfileHazardYesNo.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

