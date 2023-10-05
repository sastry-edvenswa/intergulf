#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwRptProspectAllOpportunities

# ![Views](../../../../Images/View32.png) [dbo].[vwRptProspectAllOpportunities]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 10:50:50 PM Saturday, June 6, 2015 |
| Last Modified | 10:50:50 PM Saturday, June 6, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| Date | date | 3 |  |
| Customer Name | varchar(200) | 200 |  |
| Opportunity Name | varchar(200) | 200 |  |
| Description | varchar(1000) | 1000 |  |
| Stage | varchar(50) | 50 |  |
| ExpectedCloseDate | date | 3 |  |
| Probability | bigint | 8 |  |
| NextStep | varchar(50) | 50 |  |
| Amount | numeric(18,0) | 9 |  |
| Frequency | varchar(50) | 50 |  |
| Id | numeric(18,0) | 9 | 0 - 0 |
| OwnerId | varchar(50) | 50 |  |
| FirstName | varchar(50) | 50 |  |
| LastName | varchar(50) | 50 |  |
| SalesPersonName | varchar(8000) | 8000 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwRptProspectAllOpportunities]
AS
SELECT     dbo.ProspectOpportunity.Date, dbo.Prospect.Name AS [Customer Name], dbo.ProspectOpportunity.Name AS [Opportunity Name], dbo.ProspectOpportunity.Description, 
                      dbo.ProspectOpportunity.Stage, dbo.ProspectOpportunity.ExpectedCloseDate, dbo.ProspectOpportunity.Probability, dbo.ProspectOpportunity.NextStep, 
                      dbo.ProspectOpportunity.Amount, dbo.ProspectOpportunity.Frequency, dbo.Prospect.Id, dbo.ProspectOpportunity.OwnerId, dbo.UserMaster.FirstName, 
                      dbo.UserMaster.LastName, RTRIM(LTRIM(REPLACE(dbo.UserMaster.FirstName, ' ', '') + '  ' + REPLACE(dbo.UserMaster.LastName, ' ', ''))) AS SalesPersonName
FROM         dbo.UserMaster RIGHT OUTER JOIN
                      dbo.ProspectOpportunity ON dbo.UserMaster.UserName = dbo.ProspectOpportunity.OwnerId LEFT OUTER JOIN
                      dbo.Prospect ON dbo.ProspectOpportunity.Id = dbo.Prospect.Id

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

