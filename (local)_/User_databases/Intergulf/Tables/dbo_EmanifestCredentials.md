#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.EmanifestCredentials

# ![Tables](../../../../Images/Table32.png) [dbo].[EmanifestCredentials]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 3 |
| Created | 7:57:28 PM Thursday, September 23, 2021 |
| Last Modified | 7:57:28 PM Thursday, September 23, 2021 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_EmanifestCredentials: FacilityName](../../../../Images/pkcluster.png)](#indexes) | FacilityName | varchar(50) | 50 | NOT NULL |
|  | UserId | varchar(200) | 200 | NULL allowed |
|  | UserPassword | varchar(200) | 200 | NULL allowed |
|  | UpdateDateTime | datetime | 8 | NULL allowed |
|  | UpdateUser | varchar(50) | 50 | NULL allowed |
|  | UpdateComputer | varchar(50) | 50 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_EmanifestCredentials: FacilityName](../../../../Images/pkcluster.png)](#indexes) | PK_EmanifestCredentials | FacilityName | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[EmanifestCredentials]
(
[FacilityName] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL,
[UserId] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UserPassword] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[EmanifestCredentials] ADD CONSTRAINT [PK_EmanifestCredentials] PRIMARY KEY CLUSTERED ([FacilityName]) ON [PRIMARY]
GO

```


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

