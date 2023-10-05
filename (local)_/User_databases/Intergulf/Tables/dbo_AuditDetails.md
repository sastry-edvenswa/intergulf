#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.AuditDetails

# ![Tables](../../../../Images/Table32.png) [dbo].[AuditDetails]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 223320 |
| Created | 9:51:11 PM Tuesday, January 5, 2010 |
| Last Modified | 11:50:36 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_AuditDetails: Id](../../../../Images/pkcluster.png)](#indexes) | Id | bigint | 8 | NOT NULL | 1 - 1 |
|  | TableName | varchar(50) | 50 | NULL allowed |  |
|  | KeyValue | varchar(50) | 50 | NULL allowed |  |
|  | FieldName | varchar(100) | 100 | NULL allowed |  |
|  | OriginalValue | varchar(500) | 500 | NULL allowed |  |
|  | NewValue | varchar(500) | 500 | NULL allowed |  |
|  | UpdateUser | varchar(50) | 50 | NULL allowed |  |
|  | UpdateDateTime | datetime | 8 | NULL allowed |  |
|  | UpdateComputer | varchar(50) | 50 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_AuditDetails: Id](../../../../Images/pkcluster.png)](#indexes) | PK_AuditDetails | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[AuditDetails]
(
[Id] [bigint] NOT NULL IDENTITY(1, 1),
[TableName] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[KeyValue] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[FieldName] [varchar] (100) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[OriginalValue] [varchar] (500) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[NewValue] [varchar] (500) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[AuditDetails] ADD CONSTRAINT [PK_AuditDetails] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

