#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.AuditTables

# ![Tables](../../../../Images/Table32.png) [dbo].[AuditTables]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 1 |
| Created | 9:51:33 PM Tuesday, January 5, 2010 |
| Last Modified | 11:50:36 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_AuditTables: TableName](../../../../Images/pkcluster.png)](#indexes) | TableName | varchar(50) | 50 | NOT NULL |
|  | FieldList | varchar(2000) | 2000 | NULL allowed |
|  | UpdateUser | varchar(50) | 50 | NULL allowed |
|  | UpdateDateTime | datetime | 8 | NULL allowed |
|  | UpdateComputer | varchar(50) | 50 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_AuditTables: TableName](../../../../Images/pkcluster.png)](#indexes) | PK_AuditTables | TableName | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[AuditTables]
(
[TableName] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL,
[FieldList] [varchar] (2000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[AuditTables] ADD CONSTRAINT [PK_AuditTables] PRIMARY KEY CLUSTERED ([TableName]) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

