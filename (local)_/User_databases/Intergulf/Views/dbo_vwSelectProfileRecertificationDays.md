#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectProfileRecertificationDays

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectProfileRecertificationDays]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 8:38:20 PM Monday, May 8, 2023 |
| Last Modified | 8:38:20 PM Monday, May 8, 2023 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| Id | bigint | 8 | 0 - 0 |
| ProfileNumber | varchar(50) | 50 |  |
| ProfileType | varchar(50) | 50 |  |
| SalesPersonId | varchar(50) | 50 |  |
| CSRPersonId | varchar(50) | 50 |  |
| Status | varchar(20) | 20 |  |
| CreateDate | datetime | 8 |  |
| EffectiveDate | datetime | 8 |  |
| DaysToExpire | int | 4 |  |
| LastLoadDate | datetime | 8 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectProfileRecertificationDays]
AS
SELECT        Id, ProfileNumber, ProfileType, SalesPersonId, CSRPersonId, Status, CreateDate, EffectiveDate, DATEDIFF(day, GETDATE(), EffectiveDate) AS DaysToExpire,
                             (SELECT        TOP (1) ScheduledDate
                               FROM            dbo.Loads
                               WHERE        (ProfileId = dbo.Profile.Id)
                               ORDER BY ScheduledDate DESC) AS LastLoadDate
FROM            dbo.Profile
WHERE        (Status = 'Active')
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[Profile]](../Tables/dbo_Profile.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

