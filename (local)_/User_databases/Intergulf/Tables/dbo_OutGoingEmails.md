#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.OutGoingEmails

# ![Tables](../../../../Images/Table32.png) [dbo].[OutGoingEmails]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 320840 |
| Created | 9:56:00 PM Friday, February 1, 2008 |
| Last Modified | 3:32:17 PM Tuesday, February 5, 2019 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_OutGoingEmails: Id](../../../../Images/pkcluster.png)](#indexes)[![Indexes _dta_index_OutGoingEmails_5_1486628339__K7_1_2_3_4_5_6_8_9_10](../../../../Images/Index.png)](#indexes) | Id | bigint | 8 | NOT NULL | 1 - 1 |
| [![Indexes _dta_index_OutGoingEmails_5_1486628339__K7_1_2_3_4_5_6_8_9_10](../../../../Images/Index.png)](#indexes) | Subject | varchar(500) | 500 | NULL allowed |  |
| [![Indexes _dta_index_OutGoingEmails_5_1486628339__K7_1_2_3_4_5_6_8_9_10](../../../../Images/Index.png)](#indexes) | Body | varchar(3000) | 3000 | NULL allowed |  |
| [![Indexes _dta_index_OutGoingEmails_5_1486628339__K7_1_2_3_4_5_6_8_9_10](../../../../Images/Index.png)](#indexes) | WhoTo | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_OutGoingEmails_5_1486628339__K7_1_2_3_4_5_6_8_9_10](../../../../Images/Index.png)](#indexes) | WhoFrom | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_OutGoingEmails_5_1486628339__K7_1_2_3_4_5_6_8_9_10](../../../../Images/Index.png)](#indexes) | Importance | int | 4 | NULL allowed |  |
| [![Indexes _dta_index_OutGoingEmails_5_1486628339__K7_1_2_3_4_5_6_8_9_10](../../../../Images/Index.png)](#indexes) | Sent | int | 4 | NULL allowed |  |
| [![Indexes _dta_index_OutGoingEmails_5_1486628339__K7_1_2_3_4_5_6_8_9_10](../../../../Images/Index.png)](#indexes) | UpdateDateTime | datetime | 8 | NULL allowed |  |
| [![Indexes _dta_index_OutGoingEmails_5_1486628339__K7_1_2_3_4_5_6_8_9_10](../../../../Images/Index.png)](#indexes) | UpdateUser | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_OutGoingEmails_5_1486628339__K7_1_2_3_4_5_6_8_9_10](../../../../Images/Index.png)](#indexes) | UpdateComputer | varchar(50) | 50 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Included Columns | Unique |
|---|---|---|---|---|
| [![Cluster Primary Key PK_OutGoingEmails: Id](../../../../Images/pkcluster.png)](#indexes) | PK_OutGoingEmails | Id |  | YES |
|  | _dta_index_OutGoingEmails_5_1486628339__K7_1_2_3_4_5_6_8_9_10 | Sent | Id, Subject, Body, WhoTo, WhoFrom, Importance, UpdateDateTime, UpdateUser, UpdateComputer |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[OutGoingEmails]
(
[Id] [bigint] NOT NULL IDENTITY(1, 1),
[Subject] [varchar] (500) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Body] [varchar] (3000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[WhoTo] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[WhoFrom] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Importance] [int] NULL,
[Sent] [int] NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[OutGoingEmails] ADD CONSTRAINT [PK_OutGoingEmails] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO
CREATE NONCLUSTERED INDEX [_dta_index_OutGoingEmails_5_1486628339__K7_1_2_3_4_5_6_8_9_10] ON [dbo].[OutGoingEmails] ([Sent]) INCLUDE ([Id], [Subject], [Body], [WhoTo], [WhoFrom], [Importance], [UpdateDateTime], [UpdateUser], [UpdateComputer]) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwSelectOutgoingEmailsForProfile07888]](../Views/dbo_vwSelectOutgoingEmailsForProfile07888.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

