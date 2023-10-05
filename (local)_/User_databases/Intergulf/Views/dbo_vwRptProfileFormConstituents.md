#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwRptProfileFormConstituents

# ![Views](../../../../Images/View32.png) [dbo].[vwRptProfileFormConstituents]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 7:16:02 PM Monday, January 29, 2007 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| Id | numeric(18,0) | 9 | 0 - 0 |
| ProfileId | numeric(18,0) | 9 |  |
| PetroleumPcnt | varchar(50) | 50 |  |
| PetroleumPhase | varchar(300) | 300 |  |
| AqueousPcnt | varchar(50) | 50 |  |
| AqueousPhase | varchar(300) | 300 |  |
| SolidsPcnt | varchar(50) | 50 |  |
| SolidsPhase | varchar(300) | 300 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwRptProfileFormConstituents]
AS
SELECT     Id, ProfileId, PetroleumPcnt, PetroleumPhase, AqueousPcnt, AqueousPhase, SolidsPcnt, SolidsPhase
FROM         dbo.ProfileConstituents
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[ProfileConstituents]](../Tables/dbo_ProfileConstituents.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

