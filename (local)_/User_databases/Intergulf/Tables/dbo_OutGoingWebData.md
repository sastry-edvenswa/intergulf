#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.OutGoingWebData

# ![Tables](../../../../Images/Table32.png) [dbo].[OutGoingWebData]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 1 |
| Created | 6:47:35 PM Monday, January 29, 2007 |
| Last Modified | 11:50:49 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_OutGoingWebData: Id](../../../../Images/pkcluster.png)](#indexes) | Id | numeric(18,0) | 9 | NOT NULL | 1 - 1 |
|  | FileKey | varchar(50) | 50 | NULL allowed |  |
|  | FileName | varchar(50) | 50 | NULL allowed |  |
|  | FileData | varchar(5000) | 5000 | NULL allowed |  |
|  | FileSent | int | 4 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_OutGoingWebData: Id](../../../../Images/pkcluster.png)](#indexes) | PK_OutGoingWebData | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[OutGoingWebData]
(
[Id] [numeric] (18, 0) NOT NULL IDENTITY(1, 1),
[FileKey] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[FileName] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[FileData] [varchar] (5000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[FileSent] [int] NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[OutGoingWebData] ADD CONSTRAINT [PK_OutGoingWebData] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

