#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.ProspectOpportunity

# ![Tables](../../../../Images/Table32.png) [dbo].[ProspectOpportunity]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 2547 |
| Created | 10:53:33 AM Tuesday, May 19, 2015 |
| Last Modified | 4:31:59 PM Sunday, April 8, 2018 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_ProspectOpportunity: Id](../../../../Images/pkcluster.png)](#indexes) | Id | bigint | 8 | NOT NULL | 1 - 1 |
|  | ProspectId | numeric(18,0) | 9 | NULL allowed |  |
|  | OwnerId | varchar(50) | 50 | NULL allowed |  |
|  | Name | varchar(200) | 200 | NULL allowed |  |
|  | Description | varchar(1000) | 1000 | NULL allowed |  |
|  | Date | date | 3 | NULL allowed |  |
|  | Stage | varchar(50) | 50 | NULL allowed |  |
|  | ExpectedCloseDate | date | 3 | NULL allowed |  |
|  | Probability | bigint | 8 | NULL allowed |  |
|  | NextStep | varchar(50) | 50 | NULL allowed |  |
|  | Amount | numeric(18,0) | 9 | NULL allowed |  |
|  | Frequency | varchar(50) | 50 | NULL allowed |  |
|  | Notes | varchar(2000) | 2000 | NULL allowed |  |
|  | CreateUser | varchar(50) | 50 | NULL allowed |  |
|  | CreateDateTime | datetime | 8 | NULL allowed |  |
|  | CreateComputer | varchar(50) | 50 | NULL allowed |  |
|  | UpdateUser | varchar(50) | 50 | NULL allowed |  |
|  | UpdateDateTime | datetime | 8 | NULL allowed |  |
|  | UpdateComputer | varchar(50) | 50 | NULL allowed |  |
|  | CWProfileNo | varchar(10) | 10 | NULL allowed |  |
|  | CWSageCustomerNo | varchar(10) | 10 | NULL allowed |  |
|  | CWDate | date | 3 | NULL allowed |  |
|  | CWProfileId | varchar(10) | 10 | NULL allowed |  |
|  | BusinessUnitId | bigint | 8 | NULL allowed |  |
|  | Volume | bigint | 8 | NULL allowed |  |
|  | VolumePeriod | varchar(10) | 10 | NULL allowed |  |
|  | ExpectedAmount | bigint | 8 | NULL allowed |  |
|  | UnitOfMeasure | varchar(20) | 20 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_ProspectOpportunity: Id](../../../../Images/pkcluster.png)](#indexes) | PK_ProspectOpportunity | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[ProspectOpportunity]
(
[Id] [bigint] NOT NULL IDENTITY(1, 1),
[ProspectId] [numeric] (18, 0) NULL,
[OwnerId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Name] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Description] [varchar] (1000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Date] [date] NULL,
[Stage] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ExpectedCloseDate] [date] NULL,
[Probability] [bigint] NULL,
[NextStep] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Amount] [numeric] (18, 0) NULL,
[Frequency] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Notes] [varchar] (2000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateDateTime] [datetime] NULL,
[CreateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CWProfileNo] [varchar] (10) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CWSageCustomerNo] [varchar] (10) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CWDate] [date] NULL,
[CWProfileId] [varchar] (10) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[BusinessUnitId] [bigint] NULL,
[Volume] [bigint] NULL,
[VolumePeriod] [varchar] (10) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ExpectedAmount] [bigint] NULL,
[UnitOfMeasure] [varchar] (20) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[ProspectOpportunity] ADD CONSTRAINT [PK_ProspectOpportunity] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwRptProspectAllOpportunities]](../Views/dbo_vwRptProspectAllOpportunities.md)
* [[dbo].[vwSelectProspectOpportunity]](../Views/dbo_vwSelectProspectOpportunity.md)
* [[dbo].[vwSelectProspectOpportunityBad]](../Views/dbo_vwSelectProspectOpportunityBad.md)
* [[dbo].[vwSelectProspectOpportunityForDavid]](../Views/dbo_vwSelectProspectOpportunityForDavid.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

