#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectProfileBlinds

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectProfileBlinds]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 11:18:09 PM Tuesday, December 17, 2013 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| InboundId | bigint | 8 |
| InboundGenerator | varchar(100) | 100 |
| InboundProfileNumber | varchar(50) | 50 |
| InboundDriection | varchar(50) | 50 |
| OutboundLinkId | bigint | 8 |
| InboundLinkDirection | varchar(10) | 10 |
| OutboundId | bigint | 8 |
| OutboundGenerator | varchar(100) | 100 |
| OutboundProfileNumber | varchar(50) | 50 |
| OutboundDirection | varchar(50) | 50 |
| InboundLinkId | bigint | 8 |
| OutboundLinkDirection | varchar(10) | 10 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectProfileBlinds]
AS
SELECT     dbo.Profile.Id AS InboundId, dbo.Generator.Name AS InboundGenerator, dbo.Profile.ProfileNumber AS InboundProfileNumber, 
                      dbo.Profile.Direction AS InboundDriection, dbo.Profile.LinkProfileId AS OutboundLinkId, dbo.Profile.LinkDirection AS InboundLinkDirection, 
                      Profile_1.Id AS OutboundId, Generator_1.Name AS OutboundGenerator, Profile_1.ProfileNumber AS OutboundProfileNumber, 
                      Profile_1.Direction AS OutboundDirection, Profile_1.LinkProfileId AS InboundLinkId, Profile_1.LinkDirection AS OutboundLinkDirection
FROM         dbo.Generator Generator_1 INNER JOIN
                      dbo.Profile Profile_1 ON Generator_1.Id = Profile_1.GeneratorId INNER JOIN
                      dbo.Profile ON Profile_1.Id = dbo.Profile.LinkProfileId LEFT OUTER JOIN
                      dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id
WHERE     (dbo.Profile.LinkDirection = 'In Bound')

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

