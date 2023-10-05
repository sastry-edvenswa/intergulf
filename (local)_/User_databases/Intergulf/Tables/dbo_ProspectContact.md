#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.ProspectContact

# ![Tables](../../../../Images/Table32.png) [dbo].[ProspectContact]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 320 |
| Created | 10:53:25 AM Tuesday, May 19, 2015 |
| Last Modified | 11:50:50 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_ProspectContact: Id](../../../../Images/pkcluster.png)](#indexes) | Id | numeric(18,0) | 9 | NOT NULL | 1 - 1 |
|  | ProspectId | numeric(18,0) | 9 | NULL allowed |  |
|  | OpportunityId | numeric(18,0) | 9 | NULL allowed |  |
|  | DepartmentId | numeric(18,0) | 9 | NULL allowed |  |
|  | CategoryId | numeric(18,0) | 9 | NULL allowed |  |
|  | SalesPersonId | varchar(50) | 50 | NULL allowed |  |
|  | FirstName | varchar(50) | 50 | NULL allowed |  |
|  | LastName | varchar(50) | 50 | NULL allowed |  |
|  | OfficePhone | varchar(50) | 50 | NULL allowed |  |
|  | CellPhone | varchar(50) | 50 | NULL allowed |  |
|  | Email | varchar(50) | 50 | NULL allowed |  |
|  | Notes | varchar(5000) | 5000 | NULL allowed |  |
|  | LastUpdateUser | varchar(50) | 50 | NULL allowed |  |
|  | LastUpdateDate | datetime | 8 | NULL allowed |  |
|  | KeyWords | varchar(1000) | 1000 | NULL allowed |  |
|  | MarkForDeletion | varchar(1) | 1 | NULL allowed |  |
|  | UpdateDateTime | datetime | 8 | NULL allowed |  |
|  | UpdateUser | varchar(50) | 50 | NULL allowed |  |
|  | UpdateComputer | varchar(50) | 50 | NULL allowed |  |
|  | CreateUser | varchar(50) | 50 | NULL allowed |  |
|  | CreateDateTime | datetime | 8 | NULL allowed |  |
|  | CreateComputer | varchar(50) | 50 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_ProspectContact: Id](../../../../Images/pkcluster.png)](#indexes) | PK_ProspectContact | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[ProspectContact]
(
[Id] [numeric] (18, 0) NOT NULL IDENTITY(1, 1),
[ProspectId] [numeric] (18, 0) NULL,
[OpportunityId] [numeric] (18, 0) NULL,
[DepartmentId] [numeric] (18, 0) NULL,
[CategoryId] [numeric] (18, 0) NULL,
[SalesPersonId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[FirstName] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[LastName] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[OfficePhone] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CellPhone] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Email] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Notes] [varchar] (5000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[LastUpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[LastUpdateDate] [datetime] NULL,
[KeyWords] [varchar] (1000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[MarkForDeletion] [varchar] (1) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateDateTime] [datetime] NULL,
[CreateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[ProspectContact] ADD CONSTRAINT [PK_ProspectContact] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwRptProspectContactByName]](../Views/dbo_vwRptProspectContactByName.md)
* [[dbo].[vwSelectProspectContact]](../Views/dbo_vwSelectProspectContact.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

