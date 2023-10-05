#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectProspectLabTestSample

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectProspectLabTestSample]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 4:41:24 PM Saturday, June 6, 2015 |
| Last Modified | 4:41:24 PM Saturday, June 6, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| Id | bigint | 8 | 0 - 0 |
| LabTestSampleId | bigint | 8 |  |
| ProspectId | bigint | 8 |  |
| OpportunityId | bigint | 8 |  |
| Customer | varchar(4000) | 4000 |  |
| Facility | varchar(4000) | 4000 |  |
| MaterialDescription | varchar(4000) | 4000 |  |
| SalesPersonFirstName | varchar(50) | 50 |  |
| SalesPersonLastName | varchar(50) | 50 |  |
| Comments | varchar(4000) | 4000 |  |
| EntryDate | datetime | 8 |  |
| DueDate | datetime | 8 |  |
| Status | varchar(50) | 50 |  |
| LabTechFirstName | varchar(50) | 50 |  |
| LabTechLastName | varchar(50) | 50 |  |
| ApprovalStatus | varchar(50) | 50 |  |
| EmailSent | varchar(10) | 10 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectProspectLabTestSample]
AS
SELECT     dbo.ProspectLabTestSample.Id, dbo.ProspectLabTestSample.LabTestSampleId, dbo.ProspectLabTestSample.ProspectId, dbo.ProspectLabTestSample.OpportunityId, 
                      dbo.LabTestSample.Customer, dbo.LabTestSample.Facility, dbo.LabTestSample.MaterialDescription, dbo.UserMaster.FirstName AS SalesPersonFirstName, 
                      dbo.UserMaster.LastName AS SalesPersonLastName, dbo.LabTestSample.Comments, dbo.LabTestSample.EntryDate, dbo.LabTestSample.DueDate, 
                      dbo.LabTestSample.Status, UserMaster_1.FirstName AS LabTechFirstName, UserMaster_1.LastName AS LabTechLastName, dbo.LabTestSample.ApprovalStatus, 
                      dbo.LabTestSample.EmailSent
FROM         dbo.UserMaster AS UserMaster_1 RIGHT OUTER JOIN
                      dbo.LabTestSample ON UserMaster_1.UserName = dbo.LabTestSample.LabTechId LEFT OUTER JOIN
                      dbo.UserMaster ON dbo.LabTestSample.SalesPersonId = dbo.UserMaster.UserName RIGHT OUTER JOIN
                      dbo.ProspectLabTestSample ON dbo.LabTestSample.Id = dbo.ProspectLabTestSample.LabTestSampleId

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[LabTestSample]](../Tables/dbo_LabTestSample.md)
* [[dbo].[ProspectLabTestSample]](../Tables/dbo_ProspectLabTestSample.md)
* [[dbo].[UserMaster]](../Tables/dbo_UserMaster.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

