#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.ProfileMaterialCodeAudit

# ![Tables](../../../../Images/Table32.png) [dbo].[ProfileMaterialCodeAudit]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 6432 |
| Created | 11:11:01 PM Monday, December 17, 2012 |
| Last Modified | 11:50:50 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_ProfileMaterialCodeAudit: Id](../../../../Images/pkcluster.png)](#indexes) | Id | bigint | 8 | NOT NULL | 1 - 1 |
|  | ProfileId | bigint | 8 | NULL allowed |  |
|  | UserName | varchar(50) | 50 | NULL allowed |  |
|  | Answer | varchar(10) | 10 | NULL allowed |  |
|  | OriginalMaterialCode | varchar(50) | 50 | NULL allowed |  |
|  | MaterialCode | varchar(50) | 50 | NULL allowed |  |
|  | UpdateDateTime | datetime | 8 | NULL allowed |  |
|  | UpdateUser | varchar(50) | 50 | NULL allowed |  |
|  | UpdateComputer | varchar(50) | 50 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_ProfileMaterialCodeAudit: Id](../../../../Images/pkcluster.png)](#indexes) | PK_ProfileMaterialCodeAudit | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[ProfileMaterialCodeAudit]
(
[Id] [bigint] NOT NULL IDENTITY(1, 1),
[ProfileId] [bigint] NULL,
[UserName] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Answer] [varchar] (10) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[OriginalMaterialCode] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[MaterialCode] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[ProfileMaterialCodeAudit] ADD CONSTRAINT [PK_ProfileMaterialCodeAudit] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

