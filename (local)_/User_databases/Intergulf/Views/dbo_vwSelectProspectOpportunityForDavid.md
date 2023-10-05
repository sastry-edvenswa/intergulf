#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectProspectOpportunityForDavid

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectProspectOpportunityForDavid]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 3:00:01 PM Tuesday, October 31, 2017 |
| Last Modified | 1:56:53 PM Wednesday, February 14, 2018 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| UserName | varchar(50) | 50 |
| Prospect Name | varchar(200) | 200 |
| Name | varchar(200) | 200 |
| Description | varchar(1000) | 1000 |
| Date | date | 3 |
| Stage | varchar(50) | 50 |
| ExpectedCloseDate | date | 3 |
| Probability | bigint | 8 |
| NextStep | varchar(50) | 50 |
| Amount | numeric(18,0) | 9 |
| Frequency | varchar(50) | 50 |
| Notes | varchar(2000) | 2000 |
| CreateUser | varchar(50) | 50 |
| CreateDateTime | datetime | 8 |
| UpdateUser | varchar(50) | 50 |
| UpdateDateTime | datetime | 8 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectProspectOpportunityForDavid]
AS
SELECT        dbo.ProspectOpportunity.Id, dbo.UserMaster.UserName, dbo.Prospect.Name AS [Prospect Name], dbo.ProspectOpportunity.Name, dbo.ProspectOpportunity.Description, dbo.ProspectOpportunity.Date, 
                         dbo.ProspectOpportunity.Stage, dbo.ProspectOpportunity.ExpectedCloseDate, dbo.ProspectOpportunity.Probability, dbo.ProspectOpportunity.NextStep, dbo.ProspectOpportunity.Amount, 
                         dbo.ProspectOpportunity.Frequency, dbo.ProspectOpportunity.Notes, dbo.ProspectOpportunity.CreateUser, dbo.ProspectOpportunity.CreateDateTime, dbo.ProspectOpportunity.UpdateUser, 
                         dbo.ProspectOpportunity.UpdateDateTime
FROM            dbo.ProspectOpportunity INNER JOIN
                         dbo.Prospect ON dbo.ProspectOpportunity.ProspectId = dbo.Prospect.Id LEFT OUTER JOIN
                         dbo.UserMaster ON dbo.ProspectOpportunity.OwnerId = dbo.UserMaster.UserName
WHERE        (dbo.ProspectOpportunity.CreateDateTime >= CONVERT(DATETIME, '2018-01-01 00:00:00', 102))
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Prospect]](../Tables/dbo_Prospect.md)
* [[dbo].[ProspectOpportunity]](../Tables/dbo_ProspectOpportunity.md)
* [[dbo].[UserMaster]](../Tables/dbo_UserMaster.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

