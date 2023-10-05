#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.Tanks

# ![Tables](../../../../Images/Table32.png) [dbo].[Tanks]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 125 |
| Created | 6:47:37 PM Monday, January 29, 2007 |
| Last Modified | 9:22:08 PM Tuesday, January 31, 2023 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability |
|---|---|---|---|---|
| [![Cluster Primary Key PK_Tanks: Description](../../../../Images/pkcluster.png)](#indexes) | Description | varchar(50) | 50 | NOT NULL |
|  | Volume | bigint | 8 | NULL allowed |
|  | Location | varchar(50) | 50 | NULL allowed |
|  | TrackInventory | varchar(3) | 3 | NULL allowed |
|  | CurrentTankTurnNumber | varchar(50) | 50 | NULL allowed |
|  | NewParkOnly | bit | 1 | NULL allowed |
|  | LandfillOnly | bit | 1 | NULL allowed |
|  | HandlingCode | varchar(25) | 25 | NULL allowed |
|  | Status | varchar(25) | 25 | NULL allowed |
|  | OnLoan | varchar(3) | 3 | NULL allowed |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_Tanks: Description](../../../../Images/pkcluster.png)](#indexes) | PK_Tanks | Description | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[Tanks]
(
[Description] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NOT NULL,
[Volume] [bigint] NULL,
[Location] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[TrackInventory] [varchar] (3) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CurrentTankTurnNumber] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[NewParkOnly] [bit] NULL,
[LandfillOnly] [bit] NULL,
[HandlingCode] [varchar] (25) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Status] [varchar] (25) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[OnLoan] [varchar] (3) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[Tanks] ADD CONSTRAINT [PK_Tanks] PRIMARY KEY CLUSTERED ([Description]) ON [PRIMARY]
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwSaturnTestTank]](../Views/dbo_vwSaturnTestTank.md)
* [[dbo].[vwSelectSaturnTransactions]](../Views/dbo_vwSelectSaturnTransactions.md)
* [[dbo].[vwSelectSaturnTransactionsBackup]](../Views/dbo_vwSelectSaturnTransactionsBackup.md)
* [[dbo].[vwSelectSaturnTransactionsLoads]](../Views/dbo_vwSelectSaturnTransactionsLoads.md)
* [[dbo].[vwSelectTanksForSaturn]](../Views/dbo_vwSelectTanksForSaturn.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

