#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectEmergencyContactNumber

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectEmergencyContactNumber]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 6:27:30 PM Thursday, June 8, 2023 |
| Last Modified | 6:27:30 PM Thursday, June 8, 2023 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| PECPhone | varchar(50) | 50 |
| GECPhone | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectEmergencyContactNumber]
AS
SELECT        TOP (100) PERCENT dbo.Profile.Id, dbo.ProfileEmergencyContact.Phone AS PECPhone, dbo.EmergencyContact.Phone AS GECPhone
FROM            dbo.Profile LEFT OUTER JOIN
                         dbo.ProfileEmergencyContact ON dbo.Profile.Id = dbo.ProfileEmergencyContact.Id LEFT OUTER JOIN
                         dbo.EmergencyContact RIGHT OUTER JOIN
                         dbo.Generator ON dbo.EmergencyContact.Id = dbo.Generator.Id ON dbo.Profile.GeneratorId = dbo.Generator.Id
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[EmergencyContact]](../Tables/dbo_EmergencyContact.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[ProfileEmergencyContact]](../Tables/dbo_ProfileEmergencyContact.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

