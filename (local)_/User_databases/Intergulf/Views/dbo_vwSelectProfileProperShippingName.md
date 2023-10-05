#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectProfileProperShippingName

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectProfileProperShippingName]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 11:10:08 PM Monday, December 17, 2012 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| MaterialCodeId | int | 4 |
| MaterialCode | nvarchar(50) | 100 |
| ShippingName | varchar(1000) | 1000 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectProfileProperShippingName]
AS
SELECT     dbo.Profile.Id, dbo.MaterialCode.ID AS MaterialCodeId, dbo.MaterialCode.MaterialCode, dbo.Profile.ShippingName
FROM         dbo.Profile LEFT OUTER JOIN
                      dbo.MaterialCode ON dbo.Profile.MaterialCodeId = dbo.MaterialCode.ID

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[MaterialCode]](../Tables/dbo_MaterialCode.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

