#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectExportProfilesApprovalDays

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectExportProfilesApprovalDays]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 7:35:29 PM Tuesday, July 14, 2020 |
| Last Modified | 9:15:17 PM Wednesday, July 22, 2020 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| GeneratorId | bigint | 8 |
| GeneratorName | varchar(100) | 100 |
| CustomerId | bigint | 8 |
| CustomerName | varchar(100) | 100 |
| ProfileNumber | varchar(50) | 50 |
| MaterialDescription | varchar(3000) | 3000 |
| ProfileType | varchar(50) | 50 |
| Direction | varchar(50) | 50 |
| SalesPersonId | varchar(50) | 50 |
| CSRPersonId | varchar(50) | 50 |
| CreateDateTime | datetime | 8 |
| CreateDate | datetime | 8 |
| Status | varchar(20) | 20 |
| StatusChangeDate | datetime | 8 |
| Days | int | 4 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectExportProfilesApprovalDays]
AS
SELECT        dbo.Profile.GeneratorId, dbo.Generator.Name AS GeneratorName, dbo.Profile.CustomerId, dbo.Customer.Name AS CustomerName, dbo.Profile.ProfileNumber, dbo.Profile.MaterialDescription, 
                         dbo.Profile.ProfileType, dbo.Profile.Direction, dbo.Profile.SalesPersonId, dbo.UserMaster.CSRPersonId, dbo.Profile.CreateDateTime, dbo.Profile.CreateDate, dbo.Profile.Status, dbo.Profile.StatusChangeDate, 
                         dbo.fnProfileDays(dbo.Profile.Status, dbo.Profile.CreateDate, dbo.Profile.StatusChangeDate) AS Days
FROM            dbo.Profile LEFT OUTER JOIN
                         dbo.UserMaster ON dbo.Profile.SalesPersonId = dbo.UserMaster.UserName LEFT OUTER JOIN
                         dbo.Customer ON dbo.Profile.CustomerId = dbo.Customer.Id LEFT OUTER JOIN
                         dbo.Generator ON dbo.Profile.GeneratorId = dbo.Generator.Id
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Customer]](../Tables/dbo_Customer.md)
* [[dbo].[Generator]](../Tables/dbo_Generator.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)
* [[dbo].[UserMaster]](../Tables/dbo_UserMaster.md)
* [[dbo].[fnProfileDays]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnProfileDays.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

