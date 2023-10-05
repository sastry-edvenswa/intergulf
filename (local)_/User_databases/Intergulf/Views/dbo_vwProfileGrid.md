#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwProfileGrid

# ![Views](../../../../Images/View32.png) [dbo].[vwProfileGrid]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 7:30:24 PM Monday, January 29, 2007 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| Id | bigint | 8 | 0 - 0 |
| WasteCode | varchar(50) | 50 |  |
| Description | varchar(255) | 255 |  |
| CustomerId | bigint | 8 |  |
| GeneratorId | bigint | 8 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwProfileGrid]
AS
SELECT     Id, WasteCode, dbo.fnGetDescription(MaterialDescription) AS Description, CustomerId, GeneratorId
FROM         dbo.Profile
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[fnGetDescription]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnGetDescription.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

