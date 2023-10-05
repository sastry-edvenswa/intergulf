#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectProspectOpportunityBad

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectProspectOpportunityBad]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 1:23:43 PM Monday, April 23, 2018 |
| Last Modified | 3:07:42 PM Monday, March 11, 2019 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| ProspectId | numeric(18,0) | 9 |
| OwnerId | varchar(50) | 50 |
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
| CreateComputer | varchar(50) | 50 |
| UpdateUser | varchar(50) | 50 |
| UpdateDateTime | datetime | 8 |
| UpdateComputer | varchar(50) | 50 |
| CWProfileNo | varchar(10) | 10 |
| CWSageCustomerNo | varchar(10) | 10 |
| CWDate | date | 3 |
| CWProfileId | varchar(10) | 10 |
| BusinessUnitId | bigint | 8 |
| Volume | bigint | 8 |
| VolumePeriod | varchar(10) | 10 |
| ExpectedAmount | bigint | 8 |
| UnitOfMeasure | varchar(20) | 20 |
| ProspectName | varchar(200) | 200 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwSelectProspectOpportunityBad]
AS
SELECT        TOP (100) PERCENT dbo.ProspectOpportunity.Id, dbo.ProspectOpportunity.ProspectId, dbo.ProspectOpportunity.OwnerId, dbo.ProspectOpportunity.Name, dbo.ProspectOpportunity.Description, 
                         dbo.ProspectOpportunity.Date, dbo.ProspectOpportunity.Stage, dbo.ProspectOpportunity.ExpectedCloseDate, dbo.ProspectOpportunity.Probability, dbo.ProspectOpportunity.NextStep, 
                         dbo.ProspectOpportunity.Amount, dbo.ProspectOpportunity.Frequency, dbo.ProspectOpportunity.Notes, dbo.ProspectOpportunity.CreateUser, dbo.ProspectOpportunity.CreateDateTime, 
                         dbo.ProspectOpportunity.CreateComputer, dbo.ProspectOpportunity.UpdateUser, dbo.ProspectOpportunity.UpdateDateTime, dbo.ProspectOpportunity.UpdateComputer, dbo.ProspectOpportunity.CWProfileNo, 
                         dbo.ProspectOpportunity.CWSageCustomerNo, dbo.ProspectOpportunity.CWDate, dbo.ProspectOpportunity.CWProfileId, dbo.ProspectOpportunity.BusinessUnitId, dbo.ProspectOpportunity.Volume, 
                         dbo.ProspectOpportunity.VolumePeriod, dbo.ProspectOpportunity.ExpectedAmount, dbo.ProspectOpportunity.UnitOfMeasure, dbo.Prospect.Name AS ProspectName
FROM            dbo.ProspectOpportunity LEFT OUTER JOIN
                         dbo.Prospect ON dbo.ProspectOpportunity.ProspectId = dbo.Prospect.Id
ORDER BY dbo.ProspectOpportunity.OwnerId, dbo.ProspectOpportunity.ProspectId, dbo.ProspectOpportunity.Name, dbo.ProspectOpportunity.UpdateDateTime DESC, dbo.ProspectOpportunity.Description
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Prospect]](../Tables/dbo_Prospect.md)
* [[dbo].[ProspectOpportunity]](../Tables/dbo_ProspectOpportunity.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

