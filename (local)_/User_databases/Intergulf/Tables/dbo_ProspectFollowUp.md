#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.ProspectFollowUp

# ![Tables](../../../../Images/Table32.png) [dbo].[ProspectFollowUp]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 0 |
| Created | 6:47:36 PM Monday, January 29, 2007 |
| Last Modified | 11:50:50 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_ProspectFollowUp: FollowUpId](../../../../Images/pkcluster.png)](#indexes) | FollowUpId | numeric(18,0) | 9 | NOT NULL | 1 - 1 |
|  | ProspectId | varchar(50) | 50 | NULL allowed |  |
|  | ContactId | varchar(50) | 50 | NULL allowed |  |
|  | Notes | varchar(5000) | 5000 | NULL allowed |  |
|  | FollowUpDate | datetime | 8 | NULL allowed |  |
|  | DateCreated | datetime | 8 | NULL allowed |  |
|  | CreatedBy | varchar(50) | 50 | NULL allowed |  |
|  | Closed | int | 4 | NULL allowed |  |
|  | AutoClose | int | 4 | NULL allowed |  |
|  | Emailed | int | 4 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_ProspectFollowUp: FollowUpId](../../../../Images/pkcluster.png)](#indexes) | PK_ProspectFollowUp | FollowUpId | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[ProspectFollowUp]
(
[FollowUpId] [numeric] (18, 0) NOT NULL IDENTITY(1, 1),
[ProspectId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ContactId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Notes] [varchar] (5000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[FollowUpDate] [datetime] NULL,
[DateCreated] [datetime] NULL,
[CreatedBy] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Closed] [int] NULL,
[AutoClose] [int] NULL,
[Emailed] [int] NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[ProspectFollowUp] ADD CONSTRAINT [PK_ProspectFollowUp] PRIMARY KEY CLUSTERED ([FollowUpId]) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

