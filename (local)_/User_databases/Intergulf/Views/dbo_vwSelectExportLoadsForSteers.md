#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectExportLoadsForSteers

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectExportLoadsForSteers]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 1:55:26 PM Monday, October 8, 2018 |
| Last Modified | 12:53:42 PM Thursday, October 18, 2018 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Receiver | varchar(5) | 5 |
| TCEQ Type | varchar(2) | 2 |
| Internal Use | varchar(1) | 1 |
| Report Period | varchar(5) | 5 |
| No Shipments | varchar(1) | 1 |
| Manifest Number | varchar(50) | 50 |
| Gen Tceq Id | varchar(50) | 50 |
| Gen Epa Id | varchar(50) | 50 |
| Texas Waste Code | varchar(50) | 50 |
| Epa Haz 1 | varchar(10) | 10 |
| Epa Haz 2 | varchar(10) | 10 |
| Epa Haz 3 | varchar(10) | 10 |
| Epa Haz 4 | varchar(10) | 10 |
| Quantity | numeric(10,0) | 9 |
| QtyUOM | varchar(255) | 255 |
| System Type | varchar(3) | 3 |
| Date Received | datetime | 8 |
| Trans Tceq Id | varchar(50) | 50 |
| Trans Epa Id | varchar(50) | 50 |
| Method | varchar(1) | 1 |
| Action Code | varchar(1) | 1 |
| Id | bigint | 8 |
| Name | varchar(100) | 100 |
| GenFacility | varchar(50) | 50 |
| DestName | nvarchar(100) | 200 |
| DestFacility | varchar(50) | 50 |
| UseFacility | varchar(255) | 255 |
| DestEpaIdNo | nvarchar(50) | 100 |
| DestTceqNo | nvarchar(50) | 100 |
| Direction | varchar(50) | 50 |
| DispatchStatus | varchar(50) | 50 |
| LabTestId | bigint | 8 |
| Lab Status | varchar(50) | 50 |
| ActualQuantity | decimal(18,0) | 9 |
| ActualUnits | varchar(50) | 50 |
| TransDotNo | varchar(50) | 50 |
| DocumentType | varchar(50) | 50 |
| WCEndIn | varchar(1) | 1 |
| TransporterName | varchar(50) | 50 |
| TransporterDotNo | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectExportLoadsForSteers]
AS
SELECT        '39068' AS Receiver, 'R1' AS [TCEQ Type], '' AS [Internal Use], '09/18' AS [Report Period], '' AS [No Shipments], dbo.LabTest.DocumentNumber AS [Manifest Number], 
                         dbo.Generator.RegistrationNo AS [Gen Tceq Id], dbo.Generator.EpaIdNo AS [Gen Epa Id], dbo.Profile.WasteCode AS [Texas Waste Code], dbo.Profile.EPAWasteCode1 AS [Epa Haz 1], 
                         dbo.Profile.EPAWasteCode2 AS [Epa Haz 2], dbo.Profile.EPAWasteCode3 AS [Epa Haz 3], dbo.Profile.EPAWasteCode4 AS [Epa Haz 4], dbo.fnToPounds(dbo.LabTest.Quantity, dbo.LabTest.Units) AS Quantity, 
                         dbo.fnToPoundsDesc(dbo.LabTest.Quantity, dbo.LabTest.Units) AS QtyUOM, LEFT(RIGHT(dbo.LabTest.HandlingCode, 3), 3) AS [System Type], dbo.Loads.ScheduledDate AS [Date Received], 
                         dbo.Transporter.TceqNo AS [Trans Tceq Id], dbo.Transporter.EpaIdNo AS [Trans Epa Id], 'B' AS Method, 'A' AS [Action Code], dbo.Loads.Id, dbo.Generator.Name, dbo.Generator.Facility AS GenFacility, 
                         dbo.Destination.Name AS DestName, dbo.Destination.Facility AS DestFacility, dbo.fnUseFacility(dbo.Destination.Facility, dbo.Generator.Facility) AS UseFacility, dbo.Destination.EpaIdNo AS DestEpaIdNo, 
                         dbo.Destination.TceqNo AS DestTceqNo, dbo.Profile.Direction, dbo.Loads.DispatchStatus, dbo.LabTest.Id AS LabTestId, dbo.LabTest.Status AS [Lab Status], dbo.LabTest.ActualQuantity, dbo.LabTest.ActualUnits, 
                         dbo.Transporter.DotNo AS TransDotNo, dbo.Profile.DocumentType, RIGHT(dbo.Profile.WasteCode, 1) AS WCEndIn, dbo.Transporter.Name AS TransporterName, dbo.Transporter.DotNo AS TransporterDotNo
FROM            dbo.Transporter RIGHT OUTER JOIN
                         dbo.LabTest RIGHT OUTER JOIN
                         dbo.Loads INNER JOIN
                         dbo.Destination ON dbo.Loads.DestinationId = dbo.Destination.Id ON dbo.LabTest.Id = dbo.Loads.LabTestId ON dbo.Transporter.Id = dbo.Loads.TransporterId LEFT OUTER JOIN
                         dbo.Profile LEFT OUTER JOIN
                         dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id ON dbo.Loads.ProfileId = dbo.Profile.Id
WHERE        (dbo.Loads.ScheduledDate >= CONVERT(DATETIME, '2018-09-01 00:00:00', 102)) AND (RIGHT(dbo.Profile.WasteCode, 1) = 'H' OR
                         RIGHT(dbo.Profile.WasteCode, 1) = '1') AND (NOT (dbo.LabTest.Id IS NULL)) AND (dbo.LabTest.Status = 'Accepted')
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Destination]](../Tables/dbo_Destination.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[LabTest]](../Tables/dbo_LabTest.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[Transporter]](../Tables/dbo_Transporter.md)
* [[dbo].[fnToPounds]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnToPounds.md)
* [[dbo].[fnToPoundsDesc]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnToPoundsDesc.md)
* [[dbo].[fnUseFacility]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnUseFacility.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

