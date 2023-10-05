#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.ProfilesWithErrors

# ![Tables](../../../../Images/Table32.png) [dbo].[ProfilesWithErrors]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 303 |
| Created | 11:15:54 PM Monday, December 17, 2012 |
| Last Modified | 11:50:50 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_ProfilesWithErrors: Id](../../../../Images/pkcluster.png)](#indexes) | Id | bigint | 8 | NOT NULL | 1 - 1 |
|  | ProfileId | bigint | 8 | NULL allowed |  |
|  | ProblemDescription | varchar(3000) | 3000 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_ProfilesWithErrors: Id](../../../../Images/pkcluster.png)](#indexes) | PK_ProfilesWithErrors | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[ProfilesWithErrors]
(
[Id] [bigint] NOT NULL IDENTITY(1, 1),
[ProfileId] [bigint] NULL,
[ProblemDescription] [varchar] (3000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[ProfilesWithErrors] ADD CONSTRAINT [PK_ProfilesWithErrors] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwSelectProfilesWithErrors]](../Views/dbo_vwSelectProfilesWithErrors.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

