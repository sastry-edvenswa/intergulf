#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Views](Views.md) > dbo.vwRptLoadBillingSummary

# ![Views](../../../../Images/View32.png) [dbo].[vwRptLoadBillingSummary]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 10:01:52 PM Thursday, April 4, 2013 |
| Last Modified | 4:26:47 PM Thursday, January 17, 2019 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| Id | bigint | 8 |
| BillingDepartment | varchar(50) | 50 |
| DeliveryCompleteTime | numeric(18,2) | 9 |
| PickupDepartTime | numeric(18,2) | 9 |
| BillingTime | numeric(18,2) | 9 |
| ScheduledDate | datetime | 8 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[vwRptLoadBillingSummary]
AS
SELECT        TOP (100) PERCENT dbo.Loads.Id, dbo.LoadsBillingSummary.BillingDepartment, dbo.Loads.DeliveryCompleteTime, dbo.Loads.PickupDepartTime, dbo.LoadsBillingSummary.BillingTime, 
                         dbo.Loads.ScheduledDate
FROM            dbo.Loads INNER JOIN
                         dbo.LoadsBillingSummary ON dbo.Loads.Id = dbo.LoadsBillingSummary.LoadId
ORDER BY dbo.LoadsBillingSummary.BillingDepartment
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Loads]](../Tables/dbo_Loads.md)
* [[dbo].[LoadsBillingSummary]](../Tables/dbo_LoadsBillingSummary.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

