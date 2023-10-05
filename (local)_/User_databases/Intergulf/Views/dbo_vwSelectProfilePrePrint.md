#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectProfilePrePrint

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectProfilePrePrint]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 2:43:21 PM Tuesday, October 26, 2021 |
| Last Modified | 5:27:11 PM Tuesday, October 26, 2021 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| GeneratorId | bigint | 8 |
| Generator Name | varchar(100) | 100 |
| Generator Address | varchar(3000) | 3000 |
| Generator City | varchar(50) | 50 |
| Generator State | varchar(50) | 50 |
| Generator Zip | varchar(50) | 50 |
| TransporterId | bigint | 8 |
| Transporter Name | varchar(100) | 100 |
| Transporter Contact Name | varchar(50) | 50 |
| Transporter Contact Phone | varchar(50) | 50 |
| Transporter EpaIdNo | varchar(50) | 50 |
| Transporter TceqNo | varchar(50) | 50 |
| Transporter DotNo | varchar(50) | 50 |
| DestinationId | bigint | 8 |
| Destination Name | nvarchar(100) | 200 |
| Destination Address | nvarchar(50) | 100 |
| Destination City | nvarchar(50) | 100 |
| Destination State | nvarchar(50) | 100 |
| Destination Zip | nvarchar(50) | 100 |
| Destination Contact Name | nvarchar(50) | 100 |
| Destination Contact Phone | nvarchar(50) | 100 |
| Destination EpaIdNo | nvarchar(50) | 100 |
| Destination TceqNo | nvarchar(50) | 100 |
| PContactName | varchar(50) | 50 |
| PContactPhone | varchar(50) | 50 |
| GContactName | varchar(50) | 50 |
| GContactPhone | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectProfilePrePrint]
AS
SELECT        dbo.Profile.Id, dbo.Profile.GeneratorId, dbo.Generator.Name AS [Generator Name], dbo.Generator.Address AS [Generator Address], dbo.Generator.City AS [Generator City], dbo.Generator.State AS [Generator State], 
                         dbo.Generator.Zip AS [Generator Zip], dbo.Profile.TransporterId, dbo.Transporter.Name AS [Transporter Name], dbo.Transporter.Contact AS [Transporter Contact Name], 
                         dbo.Transporter.Phone AS [Transporter Contact Phone], dbo.Transporter.EpaIdNo AS [Transporter EpaIdNo], dbo.Transporter.TceqNo AS [Transporter TceqNo], dbo.Transporter.DotNo AS [Transporter DotNo], 
                         dbo.Profile.DestinationId, dbo.Destination.Name AS [Destination Name], dbo.Destination.Address AS [Destination Address], dbo.Destination.City AS [Destination City], dbo.Destination.State AS [Destination State], 
                         dbo.Destination.Zip AS [Destination Zip], dbo.Destination.Contact AS [Destination Contact Name], dbo.Destination.Phone AS [Destination Contact Phone], dbo.Destination.EpaIdNo AS [Destination EpaIdNo], 
                         dbo.Destination.TceqNo AS [Destination TceqNo], dbo.ProfileEmergencyContact.Name AS PContactName, dbo.ProfileEmergencyContact.Phone AS PContactPhone, dbo.EmergencyContact.Name AS GContactName, 
                         dbo.EmergencyContact.Phone AS GContactPhone
FROM            dbo.ProfileEmergencyContact RIGHT OUTER JOIN
                         dbo.Profile ON dbo.ProfileEmergencyContact.Id = dbo.Profile.Id LEFT OUTER JOIN
                         dbo.Destination ON dbo.Profile.DestinationId = dbo.Destination.Id LEFT OUTER JOIN
                         dbo.Transporter ON dbo.Profile.TransporterId = dbo.Transporter.Id LEFT OUTER JOIN
                         dbo.EmergencyContact RIGHT OUTER JOIN
                         dbo.Generator ON dbo.EmergencyContact.Id = dbo.Generator.Id ON dbo.Profile.GeneratorId = dbo.Generator.Id
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Destination]](../Tables/dbo_Destination.md)
* [[dbo].[EmergencyContact]](../Tables/dbo_EmergencyContact.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[ProfileEmergencyContact]](../Tables/dbo_ProfileEmergencyContact.md)
* [[dbo].[Transporter]](../Tables/dbo_Transporter.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

