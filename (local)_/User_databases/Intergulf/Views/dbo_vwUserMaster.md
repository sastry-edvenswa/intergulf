#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwUserMaster

# ![Views](../../../../Images/View32.png) [dbo].[vwUserMaster]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 12:37:41 AM Saturday, February 10, 2007 |
| Last Modified | 5:24:20 PM Wednesday, September 25, 2019 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| UserName | varchar(50) | 50 |
| UserPassword | varchar(50) | 50 |
| UserType | varchar(50) | 50 |
| SalesPerson | varchar(2) | 2 |
| FirstName | varchar(50) | 50 |
| LastName | varchar(50) | 50 |
| WebUser | varchar(2) | 2 |
| ProspectReport | varchar(2) | 2 |
| Email | varchar(50) | 50 |
| UpdateDateTime | datetime | 8 |
| UpdateUser | varchar(50) | 50 |
| UpdateComputer | varchar(50) | 50 |
| MaterialCodeReviewer | varchar(2) | 2 |
| Status | varchar(10) | 10 |
| ProfileReviewer | varchar(2) | 2 |
| BackupProfileReviewerUserName | varchar(50) | 50 |
| BackupProfileReviewer | varchar(2) | 2 |
| UseBackupReviewer | varchar(2) | 2 |
| OverrideProfileReviewer | varchar(2) | 2 |
| ProspectEmail | varchar(2) | 2 |
| AllowResourceChanges | varchar(2) | 2 |
| ReceiveProfileOverrideEmail | varchar(2) | 2 |
| ReceiveCustomerStopEmail | varchar(2) | 2 |
| ReceiveCustomerStopOverrideEmail | varchar(2) | 2 |
| ReceiveScheduleOverrideEmail | varchar(2) | 2 |
| ReceiveProspectCWReversalEmail | varchar(2) | 2 |
| AllowScheduleUnlock | varchar(2) | 2 |
| CustomerServiceRep | varchar(2) | 2 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwUserMaster]
AS
SELECT        UserName, UserPassword, UserType, SalesPerson, FirstName, LastName, WebUser, ProspectReport, Email, UpdateDateTime, UpdateUser, UpdateComputer, MaterialCodeReviewer, Status, ProfileReviewer, 
                         BackupProfileReviewerUserName, BackupProfileReviewer, UseBackupReviewer, OverrideProfileReviewer, ProspectEmail, AllowResourceChanges, ReceiveProfileOverrideEmail, ReceiveCustomerStopEmail, 
                         ReceiveCustomerStopOverrideEmail, ReceiveScheduleOverrideEmail, ReceiveProspectCWReversalEmail, AllowScheduleUnlock, CustomerServiceRep
FROM            dbo.fnSelectUserMaster() AS fnSelectUserMaster
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[fnSelectUserMaster]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectUserMaster.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

