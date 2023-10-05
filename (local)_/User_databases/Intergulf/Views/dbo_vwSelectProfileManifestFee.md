#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectProfileManifestFee

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectProfileManifestFee]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 5:28:53 PM Friday, April 24, 2020 |
| Last Modified | 1:01:31 PM Thursday, April 30, 2020 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| ProfileNumber | varchar(50) | 50 |
| Direction | varchar(50) | 50 |
| HTYes | varchar(50) | 50 |
| WasteCode | varchar(50) | 50 |
| EPAWasteCode1 | varchar(10) | 10 |
| EPAWasteCode2 | varchar(10) | 10 |
| EPAWasteCode3 | varchar(10) | 10 |
| EPAWasteCode4 | varchar(10) | 10 |
| EPAManifestFee | numeric(18,2) | 9 |
| ManifestFee | numeric(18,2) | 9 |
| Haz Id | varchar(50) | 50 |
| Haz Fee | numeric(18,2) | 9 |
| NonHaz Id | varchar(50) | 50 |
| NonHaz Fee | numeric(18,2) | 9 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectProfileManifestFee]
AS
SELECT        dbo.Profile.Id, dbo.Profile.ProfileNumber, dbo.Profile.Direction, dbo.Profile.HTYes, dbo.Profile.WasteCode, dbo.Profile.EPAWasteCode1, dbo.Profile.EPAWasteCode2, dbo.Profile.EPAWasteCode3, 
                         dbo.Profile.EPAWasteCode4, dbo.Profile.EPAManifestFee, dbo.Profile.ManifestFee, ManifestFees_1.Id AS [Haz Id], ManifestFees_1.Fee AS [Haz Fee], dbo.ManifestFees.Id AS [NonHaz Id], 
                         dbo.ManifestFees.Fee AS [NonHaz Fee]
FROM            dbo.Profile CROSS JOIN
                         dbo.ManifestFees AS ManifestFees_1 CROSS JOIN
                         dbo.ManifestFees
WHERE        (ManifestFees_1.Id = 'EPAManifestFee') AND (dbo.ManifestFees.Id = 'ManifestFee')
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[ManifestFees]](../Tables/dbo_ManifestFees.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

