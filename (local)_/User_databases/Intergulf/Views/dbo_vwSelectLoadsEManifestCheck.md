#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLoadsEManifestCheck

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLoadsEManifestCheck]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 2:18:06 PM Wednesday, September 1, 2021 |
| Last Modified | 2:19:03 PM Wednesday, September 1, 2021 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| TransporterName | varchar(100) | 100 |
| TransporterEPAId | varchar(50) | 50 |
| DestinationId | int | 4 |
| DestinationName | nvarchar(100) | 200 |
| DestinationEPAId | nvarchar(50) | 100 |
| LabTestId | bigint | 8 |
| LabLocation | varchar(50) | 50 |
| LabStatus | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectLoadsEManifestCheck]
AS
SELECT        dbo.Loads.Id, dbo.Transporter.Name AS TransporterName, dbo.Transporter.EpaIdNo AS TransporterEPAId, dbo.Destination.Id AS DestinationId, dbo.Destination.Name AS DestinationName, 
                         dbo.Destination.EpaIdNo AS DestinationEPAId, dbo.Loads.LabTestId, dbo.LabTest.Location AS LabLocation, dbo.LabTest.Status AS LabStatus
FROM            dbo.Loads LEFT OUTER JOIN
                         dbo.Destination ON dbo.Loads.DestinationId = dbo.Destination.Id LEFT OUTER JOIN
                         dbo.Transporter ON dbo.Loads.TransporterId = dbo.Transporter.Id LEFT OUTER JOIN
                         dbo.LabTest ON dbo.Loads.LabTestId = dbo.LabTest.Id LEFT OUTER JOIN
                         dbo.Profile ON dbo.Loads.ProfileId = dbo.Profile.Id
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Destination]](../Tables/dbo_Destination.md)
* [[dbo].[LabTest]](../Tables/dbo_LabTest.md)
* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[Transporter]](../Tables/dbo_Transporter.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

