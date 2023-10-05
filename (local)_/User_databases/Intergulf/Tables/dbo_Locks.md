#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.Locks

# ![Tables](../../../../Images/Table32.png) [dbo].[Locks]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 0 |
| Created | 6:47:34 PM Monday, January 29, 2007 |
| Last Modified | 11:50:49 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_Locks: Id](../../../../Images/pkcluster.png)](#indexes) | Id | bigint | 8 | NOT NULL | 1 - 1 |
|  | TableName | varchar(50) | 50 | NULL allowed |  |
|  | RecordKey | varchar(50) | 50 | NULL allowed |  |
|  | CreateTime | datetime | 8 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_Locks: Id](../../../../Images/pkcluster.png)](#indexes) | PK_Locks | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[Locks]
(
[Id] [bigint] NOT NULL IDENTITY(1, 1),
[TableName] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[RecordKey] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateTime] [datetime] NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[Locks] ADD CONSTRAINT [PK_Locks] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

