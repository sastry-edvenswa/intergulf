#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectProfileInformation

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectProfileInformation]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 3:24:12 PM Wednesday, February 11, 2015 |
| Last Modified | 3:24:12 PM Wednesday, February 11, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| GeneratorName | varchar(100) | 100 |  |
| GeneratorId | bigint | 8 |  |
| ProfileNumber | varchar(50) | 50 |  |
| ProfileId | bigint | 8 | 0 - 0 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectProfileInformation]
AS
SELECT     dbo.Generator.Name AS GeneratorName, dbo.Profile.GeneratorId, dbo.Profile.ProfileNumber, dbo.Profile.Id AS ProfileId
FROM         dbo.Profile LEFT OUTER JOIN
                      dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id

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

