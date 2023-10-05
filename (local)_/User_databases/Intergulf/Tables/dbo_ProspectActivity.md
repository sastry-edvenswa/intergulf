#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.ProspectActivity

# ![Tables](../../../../Images/Table32.png) [dbo].[ProspectActivity]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 181 |
| Created | 10:53:13 AM Tuesday, May 19, 2015 |
| Last Modified | 11:50:50 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_ProspectActivity: Id](../../../../Images/pkcluster.png)](#indexes) | Id | numeric(18,0) | 9 | NOT NULL | 1 - 1 |
|  | ProspectId | numeric(18,0) | 9 | NULL allowed |  |
|  | ContactId | numeric(18,0) | 9 | NULL allowed |  |
|  | OpportunityId | numeric(18,0) | 9 | NULL allowed |  |
|  | AssignedToId | varchar(50) | 50 | NULL allowed |  |
|  | SentTo | varchar(200) | 200 | NULL allowed |  |
|  | Subject | varchar(200) | 200 | NULL allowed |  |
|  | ActivityType | varchar(50) | 50 | NULL allowed |  |
|  | ActivityDate | date | 3 | NULL allowed |  |
|  | ActivityTime | decimal(18,0) | 9 | NULL allowed |  |
|  | Notes | varchar(5000) | 5000 | NULL allowed |  |
|  | FollowupNotes | varchar(5000) | 5000 | NULL allowed |  |
|  | SendToCalendar | int | 4 | NULL allowed |  |
|  | SendReminder | int | 4 | NULL allowed |  |
|  | ReminderDate | date | 3 | NULL allowed |  |
|  | ReminderTime | decimal(18,0) | 9 | NULL allowed |  |
|  | AutoClose | int | 4 | NULL allowed |  |
|  | Emailed | int | 4 | NULL allowed |  |
|  | Closed | int | 4 | NULL allowed |  |
|  | UpdateDateTime | datetime | 8 | NULL allowed |  |
|  | UpdateUser | varchar(50) | 50 | NULL allowed |  |
|  | UpdateComputer | varchar(50) | 50 | NULL allowed |  |
|  | CreateDateTime | datetime | 8 | NULL allowed |  |
|  | CreateUser | varchar(50) | 50 | NULL allowed |  |
|  | CreateComputer | varchar(50) | 50 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_ProspectActivity: Id](../../../../Images/pkcluster.png)](#indexes) | PK_ProspectActivity | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[ProspectActivity]
(
[Id] [numeric] (18, 0) NOT NULL IDENTITY(1, 1),
[ProspectId] [numeric] (18, 0) NULL,
[ContactId] [numeric] (18, 0) NULL,
[OpportunityId] [numeric] (18, 0) NULL,
[AssignedToId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SentTo] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Subject] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ActivityType] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ActivityDate] [date] NULL,
[ActivityTime] [decimal] (18, 0) NULL,
[Notes] [varchar] (5000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[FollowupNotes] [varchar] (5000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SendToCalendar] [int] NULL,
[SendReminder] [int] NULL,
[ReminderDate] [date] NULL,
[ReminderTime] [decimal] (18, 0) NULL,
[AutoClose] [int] NULL,
[Emailed] [int] NULL,
[Closed] [int] NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateDateTime] [datetime] NULL,
[CreateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[ProspectActivity] ADD CONSTRAINT [PK_ProspectActivity] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwSelectProspectActivity]](../Views/dbo_vwSelectProspectActivity.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

