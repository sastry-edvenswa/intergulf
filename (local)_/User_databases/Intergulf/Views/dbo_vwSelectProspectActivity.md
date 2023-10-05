#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwSelectProspectActivity

# ![Views](../../../../Images/View32.png) [dbo].[vwSelectProspectActivity]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 10:53:49 AM Tuesday, May 19, 2015 |
| Last Modified | 10:53:49 AM Tuesday, May 19, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| Id | numeric(18,0) | 9 | 0 - 0 |
| ProspectId | numeric(18,0) | 9 |  |
| ContactId | numeric(18,0) | 9 |  |
| OpportunityId | numeric(18,0) | 9 |  |
| AssignedToId | varchar(50) | 50 |  |
| SalesPersonFirstName | varchar(50) | 50 |  |
| SalesPersonLastName | varchar(50) | 50 |  |
| SentTo | varchar(200) | 200 |  |
| Subject | varchar(200) | 200 |  |
| ActivityDate | date | 3 |  |
| ActivityTime | decimal(18,0) | 9 |  |
| Notes | varchar(5000) | 5000 |  |
| SendToCalendar | int | 4 |  |
| SendReminder | int | 4 |  |
| ReminderDate | date | 3 |  |
| ReminderTime | decimal(18,0) | 9 |  |
| AutoClose | int | 4 |  |
| Emailed | int | 4 |  |
| Closed | int | 4 |  |
| FollowupNotes | varchar(5000) | 5000 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwSelectProspectActivity]
AS
SELECT     TOP (100) PERCENT dbo.ProspectActivity.Id, dbo.ProspectActivity.ProspectId, dbo.ProspectActivity.ContactId, dbo.ProspectActivity.OpportunityId, 
                      dbo.ProspectActivity.AssignedToId, dbo.UserMaster.FirstName AS SalesPersonFirstName, dbo.UserMaster.LastName AS SalesPersonLastName, 
                      dbo.ProspectActivity.SentTo, dbo.ProspectActivity.Subject, dbo.ProspectActivity.ActivityDate, dbo.ProspectActivity.ActivityTime, dbo.ProspectActivity.Notes, 
                      dbo.ProspectActivity.SendToCalendar, dbo.ProspectActivity.SendReminder, dbo.ProspectActivity.ReminderDate, dbo.ProspectActivity.ReminderTime, 
                      dbo.ProspectActivity.AutoClose, dbo.ProspectActivity.Emailed, dbo.ProspectActivity.Closed, dbo.ProspectActivity.FollowupNotes
FROM         dbo.ProspectActivity LEFT OUTER JOIN
                      dbo.UserMaster ON dbo.ProspectActivity.AssignedToId = dbo.UserMaster.UserName
ORDER BY dbo.ProspectActivity.ActivityDate, dbo.ProspectActivity.ActivityTime

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[ProspectActivity]](../Tables/dbo_ProspectActivity.md)
* [[dbo].[UserMaster]](../Tables/dbo_UserMaster.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

