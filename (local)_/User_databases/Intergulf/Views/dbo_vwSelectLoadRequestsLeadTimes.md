#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectLoadRequestsLeadTimes

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectLoadRequestsLeadTimes]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 9:53:34 PM Sunday, March 4, 2018 |
| Last Modified | 9:53:34 PM Sunday, March 4, 2018 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| Name | varchar(100) | 100 |
| ProfileNumber | varchar(50) | 50 |
| CreateUser | varchar(50) | 50 |
| CreateDate | varchar(8) | 8 |
| CreateTime | datetime | 8 |
| RequestedDate | varchar(8) | 8 |
| LoadRequestTime | varchar(50) | 50 |
| Days | int | 4 |
| NoLoads | decimal(18,0) | 9 |
| EstQuantity | varchar(50) | 50 |
| EquipmentType | varchar(50) | 50 |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectLoadRequestsLeadTimes]
AS
SELECT        TOP (100) PERCENT dbo.LoadRequest.Id, dbo.Generator.Name, dbo.Profile.ProfileNumber, dbo.LoadRequest.CreateUser, CONVERT(Varchar(8), 
                         dbo.LoadRequest.CreateDate, 1) AS CreateDate, dbo.LoadRequest.CreateTime, CONVERT(Varchar(8), dbo.LoadRequest.LoadRequestDate, 1) AS RequestedDate, 
                         dbo.LoadRequest.LoadRequestTime, DATEDIFF(dd, dbo.LoadRequest.CreateDate, dbo.LoadRequest.LoadRequestDate) AS Days, dbo.LoadRequest.NoLoads, 
                         dbo.LoadRequest.EstQuantity, dbo.LoadRequest.EquipmentType
FROM            dbo.LoadRequest LEFT OUTER JOIN
                         dbo.Generator INNER JOIN
                         dbo.Profile ON dbo.Generator.Id = dbo.Profile.GeneratorId ON dbo.LoadRequest.ProfileId = dbo.Profile.Id
WHERE        (dbo.LoadRequest.CreateDate >= CONVERT(DATETIME, '2018-01-01 00:00:00', 102))
ORDER BY dbo.LoadRequest.CreateUser

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[LoadRequest]](../Tables/dbo_LoadRequest.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

