#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.ProspectAttachments

# ![Tables](../../../../Images/Table32.png) [dbo].[ProspectAttachments]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 3 |
| Created | 4:40:19 PM Saturday, June 6, 2015 |
| Last Modified | 11:50:50 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_ProspectAttachments: Id](../../../../Images/pkcluster.png)](#indexes) | Id | bigint | 8 | NOT NULL | 1 - 1 |
|  | ProspectId | bigint | 8 | NULL allowed |  |
|  | OpportunityId | bigint | 8 | NULL allowed |  |
|  | FileLocation | varchar(500) | 500 | NULL allowed |  |
|  | Description | varchar(2000) | 2000 | NULL allowed |  |
|  | CreateUser | varchar(50) | 50 | NULL allowed |  |
|  | CreateDateTime | datetime | 8 | NULL allowed |  |
|  | CreateComputer | varchar(50) | 50 | NULL allowed |  |
|  | UpdateUser | varchar(50) | 50 | NULL allowed |  |
|  | UpdateDateTime | datetime | 8 | NULL allowed |  |
|  | UpdateComputer | varchar(50) | 50 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_ProspectAttachments: Id](../../../../Images/pkcluster.png)](#indexes) | PK_ProspectAttachments | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[ProspectAttachments]
(
[Id] [bigint] NOT NULL IDENTITY(1, 1),
[ProspectId] [bigint] NULL,
[OpportunityId] [bigint] NULL,
[FileLocation] [varchar] (500) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Description] [varchar] (2000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateDateTime] [datetime] NULL,
[CreateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[ProspectAttachments] ADD CONSTRAINT [PK_ProspectAttachments] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

