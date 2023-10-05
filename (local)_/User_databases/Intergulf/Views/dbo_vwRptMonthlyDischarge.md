#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwRptMonthlyDischarge

# ![Views](../../../../Images/View32.png) [dbo].[vwRptMonthlyDischarge]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 3:00:48 AM Monday, July 23, 2012 |
| Last Modified | 2:05:38 PM Sunday, January 25, 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| Id | bigint | 8 | 0 - 0 |
| UserName | varchar(50) | 50 |  |
| CustomerName | varchar(200) | 200 |  |
| GeneratorName | varchar(200) | 200 |  |
| ProfileNumber | varchar(200) | 200 |  |
| SICCode | varchar(200) | 200 |  |
| EpaIdNo | varchar(200) | 200 |  |
| StateId | varchar(200) | 200 |  |
| TransporterName | varchar(200) | 200 |  |
| TransporterId | varchar(200) | 200 |  |
| OrganicWaste | varchar(200) | 200 |  |
| OilyWaste | varchar(200) | 200 |  |
| OtherWaste | varchar(200) | 200 |  |
| WasteName | varchar(200) | 200 |  |
| MaterialDescription | varchar(2000) | 2000 |  |
| EPAWasteCode | varchar(200) | 200 |  |
| TCEQWasteCode | varchar(200) | 200 |  |
| IndustrialCategory | varchar(200) | 200 |  |
| TreatmentDescription | varchar(200) | 200 |  |
| GCApprovalDate | datetime | 8 |  |
| GCApproved | bit | 1 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[vwRptMonthlyDischarge]
AS
SELECT     TOP 100 PERCENT Id, UserName, CustomerName, GeneratorName, ProfileNumber, SICCode, EpaIdNo, StateId, TransporterName, TransporterId, 
                      OrganicWaste, OilyWaste, OtherWaste, WasteName, MaterialDescription, EPAWasteCode, TCEQWasteCode, IndustrialCategory, 
                      TreatmentDescription, GCApprovalDate, GCApproved
FROM         dbo.MonthlyDischargeReport
ORDER BY GeneratorName, ProfileNumber

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[MonthlyDischargeReport]](../Tables/dbo_MonthlyDischargeReport.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

