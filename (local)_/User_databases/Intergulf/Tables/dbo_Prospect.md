#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.Prospect

# ![Tables](../../../../Images/Table32.png) [dbo].[Prospect]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 1003 |
| Created | 10:53:06 AM Tuesday, May 19, 2015 |
| Last Modified | 11:50:50 AM Sunday, January 15, 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_Prospects: Id](../../../../Images/pkcluster.png)](#indexes) | Id | numeric(18,0) | 9 | NOT NULL | 1 - 1 |
|  | Name | varchar(200) | 200 | NULL allowed |  |
|  | Address | varchar(200) | 200 | NULL allowed |  |
|  | City | varchar(200) | 200 | NULL allowed |  |
|  | State | varchar(50) | 50 | NULL allowed |  |
|  | Zip | varchar(50) | 50 | NULL allowed |  |
|  | County | varchar(50) | 50 | NULL allowed |  |
|  | MailName | varchar(200) | 200 | NULL allowed |  |
|  | MailAddress | varchar(200) | 200 | NULL allowed |  |
|  | MailCity | varchar(200) | 200 | NULL allowed |  |
|  | MailState | varchar(50) | 50 | NULL allowed |  |
|  | MailZip | varchar(50) | 50 | NULL allowed |  |
|  | Phone | varchar(50) | 50 | NULL allowed |  |
|  | Fax | varchar(50) | 50 | NULL allowed |  |
|  | ParentName | varchar(200) | 200 | NULL allowed |  |
|  | ParentAddress | varchar(200) | 200 | NULL allowed |  |
|  | ParentCity | varchar(200) | 200 | NULL allowed |  |
|  | ParentState | varchar(50) | 50 | NULL allowed |  |
|  | ParentZip | varchar(50) | 50 | NULL allowed |  |
|  | ParentPhone | varchar(50) | 50 | NULL allowed |  |
|  | ParentFax | varchar(50) | 50 | NULL allowed |  |
|  | TollFree | varchar(50) | 50 | NULL allowed |  |
|  | WebSite | varchar(255) | 255 | NULL allowed |  |
|  | Email | varchar(50) | 50 | NULL allowed |  |
|  | YearEstablished | varchar(50) | 50 | NULL allowed |  |
|  | NoEmployees | varchar(50) | 50 | NULL allowed |  |
|  | AnnualSales | varchar(50) | 50 | NULL allowed |  |
|  | SIC | varchar(10) | 10 | NULL allowed |  |
|  | SICDescription | varchar(2000) | 2000 | NULL allowed |  |
|  | NAICS | varchar(10) | 10 | NULL allowed |  |
|  | NAICSDescription | varchar(2000) | 2000 | NULL allowed |  |
|  | Refinery | varchar(255) | 255 | NULL allowed |  |
|  | Capacity | varchar(1024) | 1024 | NULL allowed |  |
|  | Location | varchar(1024) | 1024 | NULL allowed |  |
|  | Processes | varchar(1024) | 1024 | NULL allowed |  |
|  | Products | varchar(5000) | 5000 | NULL allowed |  |
|  | FeedStocks | varchar(5000) | 5000 | NULL allowed |  |
|  | ByProducts | varchar(5000) | 5000 | NULL allowed |  |
|  | RawMaterial | varchar(5000) | 5000 | NULL allowed |  |
|  | Waste | varchar(5000) | 5000 | NULL allowed |  |
|  | Notes | varchar(1024) | 1024 | NULL allowed |  |
|  | PlantManager | varchar(50) | 50 | NULL allowed |  |
|  | PlantManagerPhone | varchar(50) | 50 | NULL allowed |  |
|  | PurchasingManager | varchar(50) | 50 | NULL allowed |  |
|  | PurchasingManagerPhone | varchar(50) | 50 | NULL allowed |  |
|  | EngineeringManager | varchar(50) | 50 | NULL allowed |  |
|  | EngineeringManagerPhone | varchar(50) | 50 | NULL allowed |  |
|  | EnvironmentalManager | varchar(50) | 50 | NULL allowed |  |
|  | EnvironmentalManagerPhone | varchar(50) | 50 | NULL allowed |  |
|  | SalesPersonId | varchar(50) | 50 | NULL allowed |  |
|  | MarkForDeletion | varchar(1) | 1 | NULL allowed |  |
|  | AccessId | bigint | 8 | NULL allowed |  |
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
| [![Cluster Primary Key PK_Prospects: Id](../../../../Images/pkcluster.png)](#indexes) | PK_Prospects | Id | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[Prospect]
(
[Id] [numeric] (18, 0) NOT NULL IDENTITY(1, 1),
[Name] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Address] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[City] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[State] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Zip] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[County] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[MailName] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[MailAddress] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[MailCity] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[MailState] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[MailZip] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Phone] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Fax] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ParentName] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ParentAddress] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ParentCity] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ParentState] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ParentZip] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ParentPhone] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ParentFax] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[TollFree] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[WebSite] [varchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Email] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[YearEstablished] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[NoEmployees] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[AnnualSales] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SIC] [varchar] (10) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SICDescription] [varchar] (2000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[NAICS] [varchar] (10) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[NAICSDescription] [varchar] (2000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Refinery] [varchar] (255) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Capacity] [varchar] (1024) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Location] [varchar] (1024) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Processes] [varchar] (1024) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Products] [varchar] (5000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[FeedStocks] [varchar] (5000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ByProducts] [varchar] (5000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[RawMaterial] [varchar] (5000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Waste] [varchar] (5000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Notes] [varchar] (1024) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PlantManager] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PlantManagerPhone] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PurchasingManager] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PurchasingManagerPhone] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[EngineeringManager] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[EngineeringManagerPhone] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[EnvironmentalManager] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[EnvironmentalManagerPhone] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SalesPersonId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[MarkForDeletion] [varchar] (1) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[AccessId] [bigint] NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateDateTime] [datetime] NULL,
[CreateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[Prospect] ADD CONSTRAINT [PK_Prospects] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwRptProspectAllOpportunities]](../Views/dbo_vwRptProspectAllOpportunities.md)
* [[dbo].[vwRptProspectByName]](../Views/dbo_vwRptProspectByName.md)
* [[dbo].[vwSelectProspectOpportunity]](../Views/dbo_vwSelectProspectOpportunity.md)
* [[dbo].[vwSelectProspectOpportunityBad]](../Views/dbo_vwSelectProspectOpportunityBad.md)
* [[dbo].[vwSelectProspectOpportunityForDavid]](../Views/dbo_vwSelectProspectOpportunityForDavid.md)
* [[dbo].[vwSelectProspects]](../Views/dbo_vwSelectProspects.md)
* [[dbo].[vwSelectProspectsNAICS]](../Views/dbo_vwSelectProspectsNAICS.md)
* [[dbo].[vwSelectProspectsSIC]](../Views/dbo_vwSelectProspectsSIC.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

