#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.Loads

# ![Tables](../../../../Images/Table32.png) [dbo].[Loads]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 448938 |
| Created | 12:01:25 AM Monday, September 10, 2007 |
| Last Modified | 12:47:26 PM Tuesday, October 4, 2022 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_Loads: Id](../../../../Images/pkcluster.png)](#indexes)[![Indexes Loads23, _dta_index_Loads_5_1166627199__K1_40_41_42_43_44_45_46_47_48_49, _dta_index_Loads_5_1166627199__K39_K38_K1_K5_K9_K30_K12_10_13_14_15_18_20_23_71_73_74_76_78_79, _dta_index_Loads_5_1166627199__K10_K38_K12_K5_K13_1_2_3_9_30_39, _dta_stat_1166627199_30_1_3_12_7, _dta_stat_1166627199_30_1_38_12_39_3_5_8_13, _dta_stat_1166627199_30_1_39, _dta_stat_1166627199_30_1_7_39_5_8_3, _dta_stat_1166627199_30_1_7_39_9, _dta_stat_1166627199_30_1_9_5_12, _dta_stat_1166627199_38_8_3_1_39, _dta_stat_1166627199_38_8_3_1_5_12_13_39, _dta_stat_1166627199_38_12_1_3_5_8_13_30, _dta_stat_1166627199_8_3_1_39_5_38_12_9_13, _dta_stat_1166627199_8_3_1_5, _dta_stat_1166627199_8_30_1_3_39_5_12, _dta_stat_1166627199_1_30_39_3_5_8_38, _dta_stat_1166627199_1_30_5_9_39_38_12, _dta_stat_1166627199_1_30_12_7_39_5_8_3, _dta_stat_1166627199_1_39_8, _dta_stat_1166627199_1_39_9, _dta_stat_1166627199_1_12_3, _dta_stat_1166627199_39_30_5_3_12_1, _dta_stat_1166627199_39_38_1_5_30, _dta_stat_1166627199_39_38_1_12_9, _dta_stat_1166627199_39_1_3_30_12_7, _dta_stat_1166627199_5_38_1_8, hind_1166627199_5A_38A_12A_13A_1A_3A_4A_6A_8A_14A_15A_26A_27A_28A_29A_33A, _dta_stat_1166627199_5_1_9, _dta_stat_1166627199_5_12_1_30_8, _dta_stat_1166627199_12_8_30_1_3_39, _dta_stat_1166627199_12_8_1_3_5_30, _dta_stat_1166627199_12_1_39, _dta_stat_1166627199_12_1_39_5_30, _dta_stat_1166627199_12_1_5_3_30_7_39, _dta_stat_1166627199_12_1_5_8_3_13_30_7_39_9, _dta_stat_1166627199_12_1_9_30, _dta_stat_1166627199_12_9_1_5_39_38, _dta_stat_1166627199_9_39_38_1, hind_1166627199_68A_1A_69A, hind_1166627199_68A_69A_1A](../../../../Images/Index.png)](#indexes)(41) | Id | bigint | 8 | NOT NULL | 1 - 1 |
| [![Indexes _dta_index_Loads_5_1166627199__K10_K38_K12_K5_K13_1_2_3_9_30_39](../../../../Images/Index.png)](#indexes) | SalesPersonId | varchar(50) | 50 | NULL allowed |  |
| [![Indexes Loads23, _dta_index_Loads_5_1166627199__K10_K38_K12_K5_K13_1_2_3_9_30_39, _dta_stat_1166627199_3_5_8, _dta_stat_1166627199_3_12_30_39, _dta_stat_1166627199_30_3_12, _dta_stat_1166627199_30_1_3_12_7, _dta_stat_1166627199_30_1_38_12_39_3_5_8_13, _dta_stat_1166627199_30_1_7_39_5_8_3, _dta_stat_1166627199_38_3_5_8_12_13, _dta_stat_1166627199_38_8_3_1_39, _dta_stat_1166627199_38_8_3_1_5_12_13_39, _dta_stat_1166627199_38_12_1_3_5_8_13_30, _dta_stat_1166627199_8_3_1_39_5_38_12_9_13, _dta_stat_1166627199_8_3_1_5, _dta_stat_1166627199_8_30_1_3_39_5_12, _dta_stat_1166627199_1_30_39_3_5_8_38, _dta_stat_1166627199_1_30_12_7_39_5_8_3, _dta_stat_1166627199_1_12_3, _dta_stat_1166627199_39_30_5_3_12_1, _dta_stat_1166627199_39_1_3_30_12_7, hind_1166627199_5A_38A_12A_13A_1A_3A_4A_6A_8A_14A_15A_26A_27A_28A_29A_33A, _dta_stat_1166627199_12_30_8_3, _dta_stat_1166627199_12_38_3_5, _dta_stat_1166627199_12_8_30_1_3_39, _dta_stat_1166627199_12_8_1_3_5_30, _dta_stat_1166627199_12_1_5_3_30_7_39, _dta_stat_1166627199_12_1_5_8_3_13_30_7_39_9, _dta_stat_1166627199_12_13_8_3_38_39_9, _dta_stat_1166627199_12_9_13_8_3_38, _dta_stat_1166627199_13_3_12_30_7_39_9, _dta_stat_1166627199_13_9_3_12](../../../../Images/Index.png)](#indexes)(31) | CustomerId | bigint | 8 | NULL allowed |  |
| [![Indexes Loads23, hind_1166627199_5A_38A_12A_13A_1A_3A_4A_6A_8A_14A_15A_26A_27A_28A_29A_33A](../../../../Images/Index.png)](#indexes)(2) | VendorId | bigint | 8 | NULL allowed |  |
| [![Indexes Loads23, _dta_index_Loads_5_1166627199__K39_K38_K1_K5_K9_K30_K12_10_13_14_15_18_20_23_71_73_74_76_78_79, _dta_index_Loads_5_1166627199__K10_K38_K12_K5_K13_1_2_3_9_30_39, _dta_stat_1166627199_3_5_8, _dta_stat_1166627199_30_1_38_12_39_3_5_8_13, _dta_stat_1166627199_30_1_7_39_5_8_3, _dta_stat_1166627199_30_1_9_5_12, _dta_stat_1166627199_38_3_5_8_12_13, _dta_stat_1166627199_38_8_3_1_5_12_13_39, _dta_stat_1166627199_38_5_9_30, _dta_stat_1166627199_38_12_1_3_5_8_13_30, _dta_stat_1166627199_8_3_1_39_5_38_12_9_13, _dta_stat_1166627199_8_3_1_5, _dta_stat_1166627199_8_30_1_3_39_5_12, _dta_stat_1166627199_1_30_39_3_5_8_38, _dta_stat_1166627199_1_30_5_9_39_38_12, _dta_stat_1166627199_1_30_12_7_39_5_8_3, _dta_stat_1166627199_39_30_5_3_12_1, _dta_stat_1166627199_39_38_1_5_30, _dta_stat_1166627199_5_30_9_39_38, _dta_stat_1166627199_5_38_1_8, hind_1166627199_5A_38A_12A_13A_1A_3A_4A_6A_8A_14A_15A_26A_27A_28A_29A_33A, _dta_stat_1166627199_5_1_9, _dta_stat_1166627199_5_39_38, _dta_stat_1166627199_5_12_1_30_8, _dta_stat_1166627199_5_12_10, _dta_stat_1166627199_5_10, _dta_stat_1166627199_12_38_3_5, _dta_stat_1166627199_12_8_1_3_5_30, _dta_stat_1166627199_12_1_39_5_30, _dta_stat_1166627199_12_1_5_3_30_7_39, _dta_stat_1166627199_12_1_5_8_3_13_30_7_39_9, _dta_stat_1166627199_12_39_30_5, _dta_stat_1166627199_12_9_1_5_39_38, _dta_stat_1166627199_10_38_5_12_13, _dta_stat_1166627199_9_5](../../../../Images/Index.png)](#indexes)(36) | ProfileId | bigint | 8 | NULL allowed |  |
| [![Indexes Loads23, hind_1166627199_5A_38A_12A_13A_1A_3A_4A_6A_8A_14A_15A_26A_27A_28A_29A_33A](../../../../Images/Index.png)](#indexes)(2) | LoadType | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_stat_1166627199_30_1_3_12_7, _dta_stat_1166627199_30_1_7_39_5_8_3, _dta_stat_1166627199_30_1_7_39_9, _dta_stat_1166627199_1_30_12_7_39_5_8_3, _dta_stat_1166627199_39_1_3_30_12_7, _dta_stat_1166627199_12_1_5_3_30_7_39, _dta_stat_1166627199_12_1_5_8_3_13_30_7_39_9, _dta_stat_1166627199_13_3_12_30_7_39_9, _dta_stat_1166627199_13_12_30_7_39_9](../../../../Images/Index.png)](#indexes)(9) | TransporterId | bigint | 8 | NULL allowed |  |
| [![Indexes Loads23, _dta_stat_1166627199_3_5_8, _dta_stat_1166627199_30_1_38_12_39_3_5_8_13, _dta_stat_1166627199_30_1_7_39_5_8_3, _dta_stat_1166627199_38_3_5_8_12_13, _dta_stat_1166627199_38_8_3_1_39, _dta_stat_1166627199_38_8_3_1_5_12_13_39, _dta_stat_1166627199_38_12_1_3_5_8_13_30, _dta_stat_1166627199_8_3_1_39_5_38_12_9_13, _dta_stat_1166627199_8_3_1_5, _dta_stat_1166627199_8_30_1_3_39_5_12, _dta_stat_1166627199_1_30_39_3_5_8_38, _dta_stat_1166627199_1_30_12_7_39_5_8_3, _dta_stat_1166627199_1_39_8, _dta_stat_1166627199_5_38_1_8, hind_1166627199_5A_38A_12A_13A_1A_3A_4A_6A_8A_14A_15A_26A_27A_28A_29A_33A, _dta_stat_1166627199_5_12_1_30_8, _dta_stat_1166627199_12_30_8_3, _dta_stat_1166627199_12_8_30_1_3_39, _dta_stat_1166627199_12_8_1_3_5_30, _dta_stat_1166627199_12_1_5_8_3_13_30_7_39_9, _dta_stat_1166627199_12_13_8_3_38_39_9, _dta_stat_1166627199_12_9_13_8_3_38](../../../../Images/Index.png)](#indexes)(23) | DriverId | bigint | 8 | NULL allowed |  |
| [![Indexes _dta_index_Loads_5_1166627199__K39_K38_K1_K5_K9_K30_K12_10_13_14_15_18_20_23_71_73_74_76_78_79, _dta_index_Loads_5_1166627199__K10_K38_K12_K5_K13_1_2_3_9_30_39, _dta_stat_1166627199_30_1_7_39_9, _dta_stat_1166627199_30_1_9_5_12, _dta_stat_1166627199_38_5_9_30, _dta_stat_1166627199_8_3_1_39_5_38_12_9_13, _dta_stat_1166627199_1_30_5_9_39_38_12, _dta_stat_1166627199_1_39_9, _dta_stat_1166627199_39_38_1_12_9, _dta_stat_1166627199_5_30_9_39_38, _dta_stat_1166627199_5_1_9, _dta_stat_1166627199_12_1_5_8_3_13_30_7_39_9, _dta_stat_1166627199_12_1_9_30, _dta_stat_1166627199_12_13_8_3_38_39_9, _dta_stat_1166627199_12_9_1_5_39_38, _dta_stat_1166627199_12_9_13_8_3_38, _dta_stat_1166627199_13_3_12_30_7_39_9, _dta_stat_1166627199_13_12_30_7_39_9, _dta_stat_1166627199_13_9_3_12, _dta_stat_1166627199_9_39_38_1, _dta_stat_1166627199_9_5](../../../../Images/Index.png)](#indexes)(21) | TruckId | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_Loads_5_1166627199__K39_K38_K1_K5_K9_K30_K12_10_13_14_15_18_20_23_71_73_74_76_78_79, _dta_index_Loads_5_1166627199__K10_K38_K12_K5_K13_1_2_3_9_30_39, _dta_stat_1166627199_5_12_10, _dta_stat_1166627199_5_10, _dta_stat_1166627199_12_13_10, _dta_stat_1166627199_12_13_10_38, _dta_stat_1166627199_12_10, _dta_stat_1166627199_10_38_5_12_13](../../../../Images/Index.png)](#indexes)(8) | TrailerId | varchar(50) | 50 | NULL allowed |  |
|  | ContainerTypeId | bigint | 8 | NULL allowed |  |
| [![Indexes Loads23, _dta_index_Loads_5_1166627199__K39_K38_K1_K5_K9_K30_K12_10_13_14_15_18_20_23_71_73_74_76_78_79, _dta_index_Loads_5_1166627199__K10_K38_K12_K5_K13_1_2_3_9_30_39, _dta_stat_1166627199_3_12_30_39, _dta_stat_1166627199_30_3_12, _dta_stat_1166627199_30_1_3_12_7, _dta_stat_1166627199_30_1_38_12_39_3_5_8_13, _dta_stat_1166627199_30_1_9_5_12, _dta_stat_1166627199_38_3_5_8_12_13, _dta_stat_1166627199_38_8_3_1_5_12_13_39, _dta_stat_1166627199_38_12_1_3_5_8_13_30, _dta_stat_1166627199_8_3_1_39_5_38_12_9_13, _dta_stat_1166627199_8_30_1_3_39_5_12, _dta_stat_1166627199_1_30_5_9_39_38_12, _dta_stat_1166627199_1_30_12_7_39_5_8_3, _dta_stat_1166627199_1_12_3, _dta_stat_1166627199_39_30_5_3_12_1, _dta_stat_1166627199_39_38_1_12_9, _dta_stat_1166627199_39_1_3_30_12_7, hind_1166627199_5A_38A_12A_13A_1A_3A_4A_6A_8A_14A_15A_26A_27A_28A_29A_33A, _dta_stat_1166627199_5_12_1_30_8, _dta_stat_1166627199_5_12_10, _dta_stat_1166627199_12_30, _dta_stat_1166627199_12_30_8_3, _dta_stat_1166627199_12_38_3_5, _dta_stat_1166627199_12_8_30_1_3_39, _dta_stat_1166627199_12_8_1_3_5_30, _dta_stat_1166627199_12_1_39, _dta_stat_1166627199_12_1_39_5_30, _dta_stat_1166627199_12_1_5_3_30_7_39, _dta_stat_1166627199_12_1_5_8_3_13_30_7_39_9, _dta_stat_1166627199_12_1_9_30, _dta_stat_1166627199_12_39_30_5, _dta_stat_1166627199_12_13_38, _dta_stat_1166627199_12_13_8_3_38_39_9, _dta_stat_1166627199_12_13_10, _dta_stat_1166627199_12_13_10_38, _dta_stat_1166627199_12_10, _dta_stat_1166627199_12_9_1_5_39_38, _dta_stat_1166627199_12_9_13_8_3_38, _dta_stat_1166627199_13_3_12_30_7_39_9, _dta_stat_1166627199_13_12_30_7_39_9, _dta_stat_1166627199_13_9_3_12, _dta_stat_1166627199_10_38_5_12_13](../../../../Images/Index.png)](#indexes)(44) | ScheduledDate | datetime | 8 | NULL allowed |  |
| [![Indexes Loads23, _dta_index_Loads_5_1166627199__K39_K38_K1_K5_K9_K30_K12_10_13_14_15_18_20_23_71_73_74_76_78_79, _dta_index_Loads_5_1166627199__K10_K38_K12_K5_K13_1_2_3_9_30_39, _dta_stat_1166627199_30_1_38_12_39_3_5_8_13, _dta_stat_1166627199_38_3_5_8_12_13, _dta_stat_1166627199_38_8_3_1_5_12_13_39, _dta_stat_1166627199_38_12_1_3_5_8_13_30, _dta_stat_1166627199_8_3_1_39_5_38_12_9_13, hind_1166627199_5A_38A_12A_13A_1A_3A_4A_6A_8A_14A_15A_26A_27A_28A_29A_33A, _dta_stat_1166627199_12_1_5_8_3_13_30_7_39_9, _dta_stat_1166627199_12_13_38, _dta_stat_1166627199_12_13_8_3_38_39_9, _dta_stat_1166627199_12_13_10, _dta_stat_1166627199_12_13_10_38, _dta_stat_1166627199_12_9_13_8_3_38, _dta_stat_1166627199_13_3_12_30_7_39_9, _dta_stat_1166627199_13_12_30_7_39_9, _dta_stat_1166627199_13_9_3_12, _dta_stat_1166627199_10_38_5_12_13](../../../../Images/Index.png)](#indexes)(19) | ScheduledTime | datetime | 8 | NULL allowed |  |
| [![Indexes Loads23, _dta_index_Loads_5_1166627199__K39_K38_K1_K5_K9_K30_K12_10_13_14_15_18_20_23_71_73_74_76_78_79, hind_1166627199_5A_38A_12A_13A_1A_3A_4A_6A_8A_14A_15A_26A_27A_28A_29A_33A](../../../../Images/Index.png)](#indexes)(3) | ActualDate | datetime | 8 | NULL allowed |  |
| [![Indexes Loads23, _dta_index_Loads_5_1166627199__K39_K38_K1_K5_K9_K30_K12_10_13_14_15_18_20_23_71_73_74_76_78_79, hind_1166627199_5A_38A_12A_13A_1A_3A_4A_6A_8A_14A_15A_26A_27A_28A_29A_33A](../../../../Images/Index.png)](#indexes)(3) | ActualTime | datetime | 8 | NULL allowed |  |
|  | StartTime | datetime | 8 | NULL allowed |  |
|  | EndTime | datetime | 8 | NULL allowed |  |
| [![Indexes _dta_index_Loads_5_1166627199__K39_K38_K1_K5_K9_K30_K12_10_13_14_15_18_20_23_71_73_74_76_78_79](../../../../Images/Index.png)](#indexes) | DocumentNumber | varchar(50) | 50 | NULL allowed |  |
|  | TankNumber | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_Loads_5_1166627199__K39_K38_K1_K5_K9_K30_K12_10_13_14_15_18_20_23_71_73_74_76_78_79](../../../../Images/Index.png)](#indexes) | DeliveryReleaseNumber | varchar(50) | 50 | NULL allowed |  |
|  | Notes | varchar(6000) | 6000 | NULL allowed |  |
|  | Processed | int | 4 | NULL allowed |  |
| [![Indexes _dta_index_Loads_5_1166627199__K39_K38_K1_K5_K9_K30_K12_10_13_14_15_18_20_23_71_73_74_76_78_79, _dta_index_Loads_5_1166627199__K23_K30](../../../../Images/Index.png)](#indexes)(2) | LoadRequestId | bigint | 8 | NULL allowed |  |
|  | RequestedDate | datetime | 8 | NULL allowed |  |
|  | RequestedTime | datetime | 8 | NULL allowed |  |
| [![Indexes Loads23, hind_1166627199_5A_38A_12A_13A_1A_3A_4A_6A_8A_14A_15A_26A_27A_28A_29A_33A](../../../../Images/Index.png)](#indexes)(2) | ContactName | varchar(100) | 100 | NULL allowed |  |
| [![Indexes Loads23, hind_1166627199_5A_38A_12A_13A_1A_3A_4A_6A_8A_14A_15A_26A_27A_28A_29A_33A](../../../../Images/Index.png)](#indexes)(2) | ContactPhone | varchar(50) | 50 | NULL allowed |  |
| [![Indexes Loads23, hind_1166627199_5A_38A_12A_13A_1A_3A_4A_6A_8A_14A_15A_26A_27A_28A_29A_33A](../../../../Images/Index.png)](#indexes)(2) | PickupLocation | varchar(200) | 200 | NULL allowed |  |
| [![Indexes Loads23, hind_1166627199_5A_38A_12A_13A_1A_3A_4A_6A_8A_14A_15A_26A_27A_28A_29A_33A](../../../../Images/Index.png)](#indexes)(2) | VesselTank | varchar(100) | 100 | NULL allowed |  |
| [![Indexes _dta_index_Loads_5_1166627199__K39_K38_K1_K5_K9_K30_K12_10_13_14_15_18_20_23_71_73_74_76_78_79, _dta_index_Loads_5_1166627199__K23_K30, _dta_index_Loads_5_1166627199__K10_K38_K12_K5_K13_1_2_3_9_30_39, _dta_stat_1166627199_3_12_30_39, _dta_stat_1166627199_30_3_12, _dta_stat_1166627199_30_1_3_12_7, _dta_stat_1166627199_30_1_38_12_39_3_5_8_13, _dta_stat_1166627199_30_1_39, _dta_stat_1166627199_30_1_7_39_5_8_3, _dta_stat_1166627199_30_1_7_39_9, _dta_stat_1166627199_30_1_9_5_12, _dta_stat_1166627199_38_5_9_30, _dta_stat_1166627199_38_12_1_3_5_8_13_30, _dta_stat_1166627199_8_30_1_3_39_5_12, _dta_stat_1166627199_1_30_39_3_5_8_38, _dta_stat_1166627199_1_30_5_9_39_38_12, _dta_stat_1166627199_1_30_12_7_39_5_8_3, _dta_stat_1166627199_39_30_5_3_12_1, _dta_stat_1166627199_39_38_1_5_30, _dta_stat_1166627199_39_1_3_30_12_7, _dta_stat_1166627199_5_30_9_39_38, _dta_stat_1166627199_5_12_1_30_8, _dta_stat_1166627199_12_30, _dta_stat_1166627199_12_30_8_3, _dta_stat_1166627199_12_8_30_1_3_39, _dta_stat_1166627199_12_8_1_3_5_30, _dta_stat_1166627199_12_1_39_5_30, _dta_stat_1166627199_12_1_5_3_30_7_39, _dta_stat_1166627199_12_1_5_8_3_13_30_7_39_9, _dta_stat_1166627199_12_1_9_30, _dta_stat_1166627199_12_39_30_5, _dta_stat_1166627199_13_3_12_30_7_39_9, _dta_stat_1166627199_13_12_30_7_39_9](../../../../Images/Index.png)](#indexes)(33) | DestinationId | bigint | 8 | NULL allowed |  |
|  | NoLoads | int | 4 | NULL allowed |  |
|  | EstQuantity | varchar(50) | 50 | NULL allowed |  |
| [![Indexes Loads23, hind_1166627199_5A_38A_12A_13A_1A_3A_4A_6A_8A_14A_15A_26A_27A_28A_29A_33A](../../../../Images/Index.png)](#indexes)(2) | EquipmentType | varchar(50) | 50 | NULL allowed |  |
|  | SubOk | varchar(10) | 10 | NULL allowed |  |
|  | WashOutRequired | varchar(50) | 50 | NULL allowed |  |
|  | WeightTicket | varchar(50) | 50 | NULL allowed |  |
|  | SpecialRequirements | varchar(3000) | 3000 | NULL allowed |  |
| [![Indexes Loads23, _dta_index_Loads_5_1166627199__K39_K38_K1_K5_K9_K30_K12_10_13_14_15_18_20_23_71_73_74_76_78_79, _dta_index_Loads_5_1166627199__K10_K38_K12_K5_K13_1_2_3_9_30_39, _dta_stat_1166627199_30_1_38_12_39_3_5_8_13, _dta_stat_1166627199_38_3_5_8_12_13, _dta_stat_1166627199_38_8_3_1_39, _dta_stat_1166627199_38_8_3_1_5_12_13_39, _dta_stat_1166627199_38_5_9_30, _dta_stat_1166627199_38_12_1_3_5_8_13_30, _dta_stat_1166627199_8_3_1_39_5_38_12_9_13, _dta_stat_1166627199_1_30_39_3_5_8_38, _dta_stat_1166627199_1_30_5_9_39_38_12, _dta_stat_1166627199_39_38_1_5_30, _dta_stat_1166627199_39_38_1_12_9, _dta_stat_1166627199_5_30_9_39_38, _dta_stat_1166627199_5_38_1_8, hind_1166627199_5A_38A_12A_13A_1A_3A_4A_6A_8A_14A_15A_26A_27A_28A_29A_33A, _dta_stat_1166627199_5_39_38, _dta_stat_1166627199_12_38_3_5, _dta_stat_1166627199_12_13_38, _dta_stat_1166627199_12_13_8_3_38_39_9, _dta_stat_1166627199_12_13_10_38, _dta_stat_1166627199_12_9_1_5_39_38, _dta_stat_1166627199_12_9_13_8_3_38, _dta_stat_1166627199_10_38_5_12_13, _dta_stat_1166627199_9_39_38_1](../../../../Images/Index.png)](#indexes)(26) | DispatchStatus | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_Loads_5_1166627199__K39_K38_K1_K5_K9_K30_K12_10_13_14_15_18_20_23_71_73_74_76_78_79, _dta_index_Loads_5_1166627199__K10_K38_K12_K5_K13_1_2_3_9_30_39, _dta_stat_1166627199_3_12_30_39, _dta_stat_1166627199_30_1_38_12_39_3_5_8_13, _dta_stat_1166627199_30_1_39, _dta_stat_1166627199_30_1_7_39_5_8_3, _dta_stat_1166627199_30_1_7_39_9, _dta_stat_1166627199_38_8_3_1_39, _dta_stat_1166627199_38_8_3_1_5_12_13_39, _dta_stat_1166627199_8_3_1_39_5_38_12_9_13, _dta_stat_1166627199_8_30_1_3_39_5_12, _dta_stat_1166627199_1_30_39_3_5_8_38, _dta_stat_1166627199_1_30_5_9_39_38_12, _dta_stat_1166627199_1_30_12_7_39_5_8_3, _dta_stat_1166627199_1_39_8, _dta_stat_1166627199_1_39_9, _dta_stat_1166627199_39_30_5_3_12_1, _dta_stat_1166627199_39_38_1_5_30, _dta_stat_1166627199_39_38_1_12_9, _dta_stat_1166627199_39_1_3_30_12_7, _dta_stat_1166627199_5_30_9_39_38, _dta_stat_1166627199_5_39_38, _dta_stat_1166627199_12_8_30_1_3_39, _dta_stat_1166627199_12_1_39, _dta_stat_1166627199_12_1_39_5_30, _dta_stat_1166627199_12_1_5_3_30_7_39, _dta_stat_1166627199_12_1_5_8_3_13_30_7_39_9, _dta_stat_1166627199_12_39_30_5, _dta_stat_1166627199_12_13_8_3_38_39_9, _dta_stat_1166627199_12_9_1_5_39_38, _dta_stat_1166627199_13_3_12_30_7_39_9, _dta_stat_1166627199_13_12_30_7_39_9, _dta_stat_1166627199_9_39_38_1](../../../../Images/Index.png)](#indexes)(33) | LabTestId | bigint | 8 | NULL allowed |  |
| [![Indexes _dta_index_Loads_5_1166627199__K1_40_41_42_43_44_45_46_47_48_49](../../../../Images/Index.png)](#indexes) | LabCheckInDate | datetime | 8 | NULL allowed |  |
| [![Indexes _dta_index_Loads_5_1166627199__K1_40_41_42_43_44_45_46_47_48_49](../../../../Images/Index.png)](#indexes) | LabStartTime | decimal(18,2) | 9 | NULL allowed |  |
| [![Indexes _dta_index_Loads_5_1166627199__K1_40_41_42_43_44_45_46_47_48_49](../../../../Images/Index.png)](#indexes) | LabTestStartTime | decimal(18,2) | 9 | NULL allowed |  |
| [![Indexes _dta_index_Loads_5_1166627199__K1_40_41_42_43_44_45_46_47_48_49](../../../../Images/Index.png)](#indexes) | LabTestEndTime | decimal(18,2) | 9 | NULL allowed |  |
| [![Indexes _dta_index_Loads_5_1166627199__K1_40_41_42_43_44_45_46_47_48_49](../../../../Images/Index.png)](#indexes) | LabEndTime | decimal(18,2) | 9 | NULL allowed |  |
| [![Indexes _dta_index_Loads_5_1166627199__K1_40_41_42_43_44_45_46_47_48_49](../../../../Images/Index.png)](#indexes) | PadCheckInDate | datetime | 8 | NULL allowed |  |
| [![Indexes _dta_index_Loads_5_1166627199__K1_40_41_42_43_44_45_46_47_48_49](../../../../Images/Index.png)](#indexes) | PadStartTime | decimal(18,2) | 9 | NULL allowed |  |
| [![Indexes _dta_index_Loads_5_1166627199__K1_40_41_42_43_44_45_46_47_48_49](../../../../Images/Index.png)](#indexes) | PadPumpStartTime | decimal(18,2) | 9 | NULL allowed |  |
| [![Indexes _dta_index_Loads_5_1166627199__K1_40_41_42_43_44_45_46_47_48_49](../../../../Images/Index.png)](#indexes) | PadPumpStopTime | decimal(18,2) | 9 | NULL allowed |  |
| [![Indexes _dta_index_Loads_5_1166627199__K1_40_41_42_43_44_45_46_47_48_49](../../../../Images/Index.png)](#indexes) | PadEndTime | decimal(18,2) | 9 | NULL allowed |  |
|  | WashOutPerformed | varchar(50) | 50 | NULL allowed |  |
|  | WashOutTime | decimal(18,2) | 9 | NULL allowed |  |
|  | PickupDate | datetime | 8 | NULL allowed |  |
|  | PickupDepartTime | numeric(18,2) | 9 | NULL allowed |  |
|  | PickupLocationArrivalTime | numeric(18,2) | 9 | NULL allowed |  |
|  | PickupLocationDepartTime | numeric(18,2) | 9 | NULL allowed |  |
|  | DeliveryDate | datetime | 8 | NULL allowed |  |
|  | DeliveryArrivalTime | numeric(18,2) | 9 | NULL allowed |  |
|  | DeliveryDepartTime | numeric(18,2) | 9 | NULL allowed |  |
|  | DeliveryCompleteTime | numeric(18,2) | 9 | NULL allowed |  |
|  | BillingTime | decimal(18,2) | 9 | NULL allowed |  |
|  | BillingRate | decimal(18,2) | 9 | NULL allowed |  |
|  | Number | varchar(50) | 50 | NULL allowed |  |
|  | PackageType | varchar(50) | 50 | NULL allowed |  |
|  | ShippingWeight | decimal(18,0) | 9 | NULL allowed |  |
|  | BillingDepartment | varchar(50) | 50 | NULL allowed |  |
|  | BillingStatus | varchar(50) | 50 | NULL allowed |  |
|  | DriverTimeNotes | varchar(3000) | 3000 | NULL allowed |  |
| [![Indexes Loads24, hind_1166627199_68A_1A_69A, hind_1166627199_68A_69A_1A](../../../../Images/Index.png)](#indexes)(3) | UpdateDateTime | datetime | 8 | NULL allowed |  |
| [![Indexes hind_1166627199_68A_1A_69A, hind_1166627199_68A_69A_1A](../../../../Images/Index.png)](#indexes)(2) | UpdateUser | varchar(50) | 50 | NULL allowed |  |
|  | UpdateComputer | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_Loads_5_1166627199__K39_K38_K1_K5_K9_K30_K12_10_13_14_15_18_20_23_71_73_74_76_78_79](../../../../Images/Index.png)](#indexes) | AccountingStatus | varchar(40) | 40 | NULL allowed |  |
|  | AccountingPrint | varchar(3) | 3 | NULL allowed |  |
| [![Indexes _dta_index_Loads_5_1166627199__K39_K38_K1_K5_K9_K30_K12_10_13_14_15_18_20_23_71_73_74_76_78_79](../../../../Images/Index.png)](#indexes) | AccountingAction | varchar(40) | 40 | NULL allowed |  |
| [![Indexes _dta_index_Loads_5_1166627199__K39_K38_K1_K5_K9_K30_K12_10_13_14_15_18_20_23_71_73_74_76_78_79](../../../../Images/Index.png)](#indexes) | Accountingnotes | varchar(3000) | 3000 | NULL allowed |  |
|  | PadNotes | varchar(3000) | 3000 | NULL allowed |  |
| [![Indexes _dta_index_Loads_5_1166627199__K39_K38_K1_K5_K9_K30_K12_10_13_14_15_18_20_23_71_73_74_76_78_79](../../../../Images/Index.png)](#indexes) | BlindLoadId | bigint | 8 | NULL allowed |  |
|  | ProjectNumber | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_Loads_5_1166627199__K39_K38_K1_K5_K9_K30_K12_10_13_14_15_18_20_23_71_73_74_76_78_79](../../../../Images/Index.png)](#indexes) | ExportedToSteers | varchar(3) | 3 | NULL allowed |  |
| [![Indexes _dta_index_Loads_5_1166627199__K39_K38_K1_K5_K9_K30_K12_10_13_14_15_18_20_23_71_73_74_76_78_79](../../../../Images/Index.png)](#indexes) | CommissionsPaid | varchar(3) | 3 | NULL allowed |  |
|  | CreateUser | varchar(50) | 50 | NULL allowed |  |
|  | CreateDateTime | datetime | 8 | NULL allowed |  |
|  | CreateComputer | varchar(50) | 50 | NULL allowed |  |
|  | CustomerPickupDelivery | varchar(3) | 3 | NULL allowed |  |
|  | PickupAnytime | varchar(3) | 3 | NULL allowed |  |
|  | CustomerPoNumber | varchar(50) | 50 | NULL allowed |  |
|  | CustomerPoNumberExpirationDate | date | 3 | NULL allowed |  |
|  | ContractNumber | varchar(50) | 50 | NULL allowed |  |
|  | TransactionType | varchar(20) | 20 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Included Columns | Unique |
|---|---|---|---|---|
| [![Cluster Primary Key PK_Loads: Id](../../../../Images/pkcluster.png)](#indexes) | PK_Loads | Id |  | YES |
|  | Loads23 | DispatchStatus, Id, CustomerId, VendorId, ProfileId, LoadType, DriverId, ScheduledDate, ScheduledTime, ActualDate, ActualTime, ContactName, ContactPhone, PickupLocation, VesselTank, EquipmentType |  |  |
|  | Loads24 | UpdateDateTime |  |  |
|  | _dta_index_Loads_5_1166627199__K10_K38_K12_K5_K13_1_2_3_9_30_39 | TrailerId, DispatchStatus, ScheduledDate, ProfileId, ScheduledTime | Id, SalesPersonId, CustomerId, TruckId, DestinationId, LabTestId |  |
|  | _dta_index_Loads_5_1166627199__K1_40_41_42_43_44_45_46_47_48_49 | Id | LabCheckInDate, LabStartTime, PadPumpStopTime, PadEndTime, LabTestStartTime, LabTestEndTime, LabEndTime, PadCheckInDate, PadStartTime, PadPumpStartTime |  |
|  | _dta_index_Loads_5_1166627199__K23_K30 | LoadRequestId, DestinationId |  |  |
|  | _dta_index_Loads_5_1166627199__K39_K38_K1_K5_K9_K30_K12_10_13_14_15_18_20_23_71_73_74_76_78_79 | LabTestId, DispatchStatus, Id, ProfileId, TruckId, DestinationId, ScheduledDate | ExportedToSteers, CommissionsPaid, DeliveryReleaseNumber, LoadRequestId, AccountingStatus, AccountingAction, Accountingnotes, BlindLoadId, TrailerId, ScheduledTime, ActualDate, ActualTime, DocumentNumber |  |


---

## <a name="#statistics"></a>Statistics

| Name | Key Columns |
|---|---|
| _dta_stat_1166627199_10_38_5_12_13 | TrailerId, DispatchStatus, ProfileId, ScheduledDate, ScheduledTime |
| _dta_stat_1166627199_12_10 | ScheduledDate, TrailerId |
| _dta_stat_1166627199_12_13_10 | ScheduledDate, ScheduledTime, TrailerId |
| _dta_stat_1166627199_12_13_10_38 | ScheduledDate, ScheduledTime, TrailerId, DispatchStatus |
| _dta_stat_1166627199_12_13_38 | ScheduledDate, ScheduledTime, DispatchStatus |
| _dta_stat_1166627199_12_13_8_3_38_39_9 | ScheduledDate, ScheduledTime, DriverId, CustomerId, DispatchStatus, LabTestId, TruckId |
| _dta_stat_1166627199_12_1_39 | ScheduledDate, Id, LabTestId |
| _dta_stat_1166627199_12_1_39_5_30 | ScheduledDate, Id, LabTestId, ProfileId, DestinationId |
| _dta_stat_1166627199_12_1_5_3_30_7_39 | ScheduledDate, Id, ProfileId, CustomerId, DestinationId, TransporterId, LabTestId |
| _dta_stat_1166627199_12_1_5_8_3_13_30_7_39_9 | ScheduledDate, Id, ProfileId, DriverId, CustomerId, ScheduledTime, DestinationId, TransporterId, LabTestId, TruckId |
| _dta_stat_1166627199_12_1_9_30 | ScheduledDate, Id, TruckId, DestinationId |
| _dta_stat_1166627199_12_30 | ScheduledDate, DestinationId |
| _dta_stat_1166627199_12_30_8_3 | ScheduledDate, DestinationId, DriverId, CustomerId |
| _dta_stat_1166627199_12_38_3_5 | ScheduledDate, DispatchStatus, CustomerId, ProfileId |
| _dta_stat_1166627199_12_39_30_5 | ScheduledDate, LabTestId, DestinationId, ProfileId |
| _dta_stat_1166627199_12_8_1_3_5_30 | ScheduledDate, DriverId, Id, CustomerId, ProfileId, DestinationId |
| _dta_stat_1166627199_12_8_30_1_3_39 | ScheduledDate, DriverId, DestinationId, Id, CustomerId, LabTestId |
| _dta_stat_1166627199_12_9_13_8_3_38 | ScheduledDate, TruckId, ScheduledTime, DriverId, CustomerId, DispatchStatus |
| _dta_stat_1166627199_12_9_1_5_39_38 | ScheduledDate, TruckId, Id, ProfileId, LabTestId, DispatchStatus |
| _dta_stat_1166627199_13_12_30_7_39_9 | ScheduledTime, ScheduledDate, DestinationId, TransporterId, LabTestId, TruckId |
| _dta_stat_1166627199_13_3_12_30_7_39_9 | ScheduledTime, CustomerId, ScheduledDate, DestinationId, TransporterId, LabTestId, TruckId |
| _dta_stat_1166627199_13_9_3_12 | ScheduledTime, TruckId, CustomerId, ScheduledDate |
| _dta_stat_1166627199_1_12_3 | Id, ScheduledDate, CustomerId |
| _dta_stat_1166627199_1_30_12_7_39_5_8_3 | Id, DestinationId, ScheduledDate, TransporterId, LabTestId, ProfileId, DriverId, CustomerId |
| _dta_stat_1166627199_1_30_39_3_5_8_38 | Id, DestinationId, LabTestId, CustomerId, ProfileId, DriverId, DispatchStatus |
| _dta_stat_1166627199_1_30_5_9_39_38_12 | Id, DestinationId, ProfileId, TruckId, LabTestId, DispatchStatus, ScheduledDate |
| _dta_stat_1166627199_1_39_8 | Id, LabTestId, DriverId |
| _dta_stat_1166627199_1_39_9 | Id, LabTestId, TruckId |
| _dta_stat_1166627199_30_1_38_12_39_3_5_8_13 | DestinationId, Id, DispatchStatus, ScheduledDate, LabTestId, CustomerId, ProfileId, DriverId, ScheduledTime |
| _dta_stat_1166627199_30_1_39 | DestinationId, Id, LabTestId |
| _dta_stat_1166627199_30_1_3_12_7 | DestinationId, Id, CustomerId, ScheduledDate, TransporterId |
| _dta_stat_1166627199_30_1_7_39_5_8_3 | DestinationId, Id, TransporterId, LabTestId, ProfileId, DriverId, CustomerId |
| _dta_stat_1166627199_30_1_7_39_9 | DestinationId, Id, TransporterId, LabTestId, TruckId |
| _dta_stat_1166627199_30_1_9_5_12 | DestinationId, Id, TruckId, ProfileId, ScheduledDate |
| _dta_stat_1166627199_30_3_12 | DestinationId, CustomerId, ScheduledDate |
| _dta_stat_1166627199_38_12_1_3_5_8_13_30 | DispatchStatus, ScheduledDate, Id, CustomerId, ProfileId, DriverId, ScheduledTime, DestinationId |
| _dta_stat_1166627199_38_3_5_8_12_13 | DispatchStatus, CustomerId, ProfileId, DriverId, ScheduledDate, ScheduledTime |
| _dta_stat_1166627199_38_5_9_30 | DispatchStatus, ProfileId, TruckId, DestinationId |
| _dta_stat_1166627199_38_8_3_1_39 | DispatchStatus, DriverId, CustomerId, Id, LabTestId |
| _dta_stat_1166627199_38_8_3_1_5_12_13_39 | DispatchStatus, DriverId, CustomerId, Id, ProfileId, ScheduledDate, ScheduledTime, LabTestId |
| _dta_stat_1166627199_39_1_3_30_12_7 | LabTestId, Id, CustomerId, DestinationId, ScheduledDate, TransporterId |
| _dta_stat_1166627199_39_30_5_3_12_1 | LabTestId, DestinationId, ProfileId, CustomerId, ScheduledDate, Id |
| _dta_stat_1166627199_39_38_1_12_9 | LabTestId, DispatchStatus, Id, ScheduledDate, TruckId |
| _dta_stat_1166627199_39_38_1_5_30 | LabTestId, DispatchStatus, Id, ProfileId, DestinationId |
| _dta_stat_1166627199_3_12_30_39 | CustomerId, ScheduledDate, DestinationId, LabTestId |
| _dta_stat_1166627199_3_5_8 | CustomerId, ProfileId, DriverId |
| _dta_stat_1166627199_5_10 | ProfileId, TrailerId |
| _dta_stat_1166627199_5_12_10 | ProfileId, ScheduledDate, TrailerId |
| _dta_stat_1166627199_5_12_1_30_8 | ProfileId, ScheduledDate, Id, DestinationId, DriverId |
| _dta_stat_1166627199_5_1_9 | ProfileId, Id, TruckId |
| _dta_stat_1166627199_5_30_9_39_38 | ProfileId, DestinationId, TruckId, LabTestId, DispatchStatus |
| _dta_stat_1166627199_5_38_1_8 | ProfileId, DispatchStatus, Id, DriverId |
| _dta_stat_1166627199_5_39_38 | ProfileId, LabTestId, DispatchStatus |
| _dta_stat_1166627199_8_30_1_3_39_5_12 | DriverId, DestinationId, Id, CustomerId, LabTestId, ProfileId, ScheduledDate |
| _dta_stat_1166627199_8_3_1_39_5_38_12_9_13 | DriverId, CustomerId, Id, LabTestId, ProfileId, DispatchStatus, ScheduledDate, TruckId, ScheduledTime |
| _dta_stat_1166627199_8_3_1_5 | DriverId, CustomerId, Id, ProfileId |
| _dta_stat_1166627199_9_39_38_1 | TruckId, LabTestId, DispatchStatus, Id |
| _dta_stat_1166627199_9_5 | TruckId, ProfileId |
| hind_1166627199_5A_38A_12A_13A_1A_3A_4A_6A_8A_14A_15A_26A_27A_28A_29A_33A | ProfileId, DispatchStatus, ScheduledDate, ScheduledTime, Id, CustomerId, VendorId, LoadType, DriverId, ActualDate, ActualTime, ContactName, ContactPhone, PickupLocation, VesselTank, EquipmentType |
| hind_1166627199_68A_1A_69A | UpdateDateTime, Id, UpdateUser |
| hind_1166627199_68A_69A_1A | UpdateDateTime, UpdateUser, Id |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[Loads]
(
[Id] [bigint] NOT NULL IDENTITY(1, 1),
[SalesPersonId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CustomerId] [bigint] NULL,
[VendorId] [bigint] NULL,
[ProfileId] [bigint] NULL,
[LoadType] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[TransporterId] [bigint] NULL,
[DriverId] [bigint] NULL,
[TruckId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[TrailerId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ContainerTypeId] [bigint] NULL,
[ScheduledDate] [datetime] NULL,
[ScheduledTime] [datetime] NULL,
[ActualDate] [datetime] NULL,
[ActualTime] [datetime] NULL,
[StartTime] [datetime] NULL,
[EndTime] [datetime] NULL,
[DocumentNumber] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[TankNumber] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[DeliveryReleaseNumber] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Notes] [varchar] (6000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Processed] [int] NULL,
[LoadRequestId] [bigint] NULL,
[RequestedDate] [datetime] NULL,
[RequestedTime] [datetime] NULL,
[ContactName] [varchar] (100) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ContactPhone] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PickupLocation] [varchar] (200) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[VesselTank] [varchar] (100) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[DestinationId] [bigint] NULL,
[NoLoads] [int] NULL,
[EstQuantity] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[EquipmentType] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SubOk] [varchar] (10) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[WashOutRequired] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[WeightTicket] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[SpecialRequirements] [varchar] (3000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[DispatchStatus] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[LabTestId] [bigint] NULL,
[LabCheckInDate] [datetime] NULL,
[LabStartTime] [decimal] (18, 2) NULL,
[LabTestStartTime] [decimal] (18, 2) NULL,
[LabTestEndTime] [decimal] (18, 2) NULL,
[LabEndTime] [decimal] (18, 2) NULL,
[PadCheckInDate] [datetime] NULL,
[PadStartTime] [decimal] (18, 2) NULL,
[PadPumpStartTime] [decimal] (18, 2) NULL,
[PadPumpStopTime] [decimal] (18, 2) NULL,
[PadEndTime] [decimal] (18, 2) NULL,
[WashOutPerformed] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[WashOutTime] [decimal] (18, 2) NULL,
[PickupDate] [datetime] NULL,
[PickupDepartTime] [numeric] (18, 2) NULL,
[PickupLocationArrivalTime] [numeric] (18, 2) NULL,
[PickupLocationDepartTime] [numeric] (18, 2) NULL,
[DeliveryDate] [datetime] NULL,
[DeliveryArrivalTime] [numeric] (18, 2) NULL,
[DeliveryDepartTime] [numeric] (18, 2) NULL,
[DeliveryCompleteTime] [numeric] (18, 2) NULL,
[BillingTime] [decimal] (18, 2) NULL,
[BillingRate] [decimal] (18, 2) NULL,
[Number] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PackageType] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ShippingWeight] [decimal] (18, 0) NULL,
[BillingDepartment] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[BillingStatus] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[DriverTimeNotes] [varchar] (3000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[AccountingStatus] [varchar] (40) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[AccountingPrint] [varchar] (3) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[AccountingAction] [varchar] (40) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Accountingnotes] [varchar] (3000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PadNotes] [varchar] (3000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[BlindLoadId] [bigint] NULL,
[ProjectNumber] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ExportedToSteers] [varchar] (3) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CommissionsPaid] [varchar] (3) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CreateDateTime] [datetime] NULL,
[CreateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CustomerPickupDelivery] [varchar] (3) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PickupAnytime] [varchar] (3) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CustomerPoNumber] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[CustomerPoNumberExpirationDate] [date] NULL,
[ContractNumber] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[TransactionType] [varchar] (20) COLLATE SQL_Latin1_General_CP1_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[Loads] ADD CONSTRAINT [PK_Loads] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO
CREATE NONCLUSTERED INDEX [Loads23] ON [dbo].[Loads] ([DispatchStatus], [Id], [CustomerId], [VendorId], [ProfileId], [LoadType], [DriverId], [ScheduledDate], [ScheduledTime], [ActualDate], [ActualTime], [ContactName], [ContactPhone], [PickupLocation], [VesselTank], [EquipmentType]) ON [PRIMARY]
GO
CREATE NONCLUSTERED INDEX [_dta_index_Loads_5_1166627199__K1_40_41_42_43_44_45_46_47_48_49] ON [dbo].[Loads] ([Id]) INCLUDE ([LabCheckInDate], [LabStartTime], [LabTestStartTime], [LabTestEndTime], [LabEndTime], [PadCheckInDate], [PadStartTime], [PadPumpStartTime], [PadPumpStopTime], [PadEndTime]) ON [PRIMARY]
GO
CREATE NONCLUSTERED INDEX [_dta_index_Loads_5_1166627199__K39_K38_K1_K5_K9_K30_K12_10_13_14_15_18_20_23_71_73_74_76_78_79] ON [dbo].[Loads] ([LabTestId], [DispatchStatus], [Id], [ProfileId], [TruckId], [DestinationId], [ScheduledDate]) INCLUDE ([TrailerId], [ScheduledTime], [ActualDate], [ActualTime], [DocumentNumber], [DeliveryReleaseNumber], [LoadRequestId], [AccountingStatus], [AccountingAction], [Accountingnotes], [BlindLoadId], [ExportedToSteers], [CommissionsPaid]) ON [PRIMARY]
GO
CREATE NONCLUSTERED INDEX [_dta_index_Loads_5_1166627199__K23_K30] ON [dbo].[Loads] ([LoadRequestId], [DestinationId]) ON [PRIMARY]
GO
CREATE NONCLUSTERED INDEX [_dta_index_Loads_5_1166627199__K10_K38_K12_K5_K13_1_2_3_9_30_39] ON [dbo].[Loads] ([TrailerId], [DispatchStatus], [ScheduledDate], [ProfileId], [ScheduledTime]) INCLUDE ([Id], [SalesPersonId], [CustomerId], [TruckId], [DestinationId], [LabTestId]) ON [PRIMARY]
GO
CREATE NONCLUSTERED INDEX [Loads24] ON [dbo].[Loads] ([UpdateDateTime]) ON [PRIMARY]
GO
CREATE STATISTICS [_dta_stat_1166627199_3_5_8] ON [dbo].[Loads] ([CustomerId], [ProfileId], [DriverId])
GO
CREATE STATISTICS [_dta_stat_1166627199_3_12_30_39] ON [dbo].[Loads] ([CustomerId], [ScheduledDate], [DestinationId], [LabTestId])
GO
CREATE STATISTICS [_dta_stat_1166627199_30_3_12] ON [dbo].[Loads] ([DestinationId], [CustomerId], [ScheduledDate])
GO
CREATE STATISTICS [_dta_stat_1166627199_30_1_3_12_7] ON [dbo].[Loads] ([DestinationId], [Id], [CustomerId], [ScheduledDate], [TransporterId])
GO
CREATE STATISTICS [_dta_stat_1166627199_30_1_38_12_39_3_5_8_13] ON [dbo].[Loads] ([DestinationId], [Id], [DispatchStatus], [ScheduledDate], [LabTestId], [CustomerId], [ProfileId], [DriverId], [ScheduledTime])
GO
CREATE STATISTICS [_dta_stat_1166627199_30_1_39] ON [dbo].[Loads] ([DestinationId], [Id], [LabTestId])
GO
CREATE STATISTICS [_dta_stat_1166627199_30_1_7_39_5_8_3] ON [dbo].[Loads] ([DestinationId], [Id], [TransporterId], [LabTestId], [ProfileId], [DriverId], [CustomerId])
GO
CREATE STATISTICS [_dta_stat_1166627199_30_1_7_39_9] ON [dbo].[Loads] ([DestinationId], [Id], [TransporterId], [LabTestId], [TruckId])
GO
CREATE STATISTICS [_dta_stat_1166627199_30_1_9_5_12] ON [dbo].[Loads] ([DestinationId], [Id], [TruckId], [ProfileId], [ScheduledDate])
GO
CREATE STATISTICS [_dta_stat_1166627199_38_3_5_8_12_13] ON [dbo].[Loads] ([DispatchStatus], [CustomerId], [ProfileId], [DriverId], [ScheduledDate], [ScheduledTime])
GO
CREATE STATISTICS [_dta_stat_1166627199_38_8_3_1_39] ON [dbo].[Loads] ([DispatchStatus], [DriverId], [CustomerId], [Id], [LabTestId])
GO
CREATE STATISTICS [_dta_stat_1166627199_38_8_3_1_5_12_13_39] ON [dbo].[Loads] ([DispatchStatus], [DriverId], [CustomerId], [Id], [ProfileId], [ScheduledDate], [ScheduledTime], [LabTestId])
GO
CREATE STATISTICS [_dta_stat_1166627199_38_5_9_30] ON [dbo].[Loads] ([DispatchStatus], [ProfileId], [TruckId], [DestinationId])
GO
CREATE STATISTICS [_dta_stat_1166627199_38_12_1_3_5_8_13_30] ON [dbo].[Loads] ([DispatchStatus], [ScheduledDate], [Id], [CustomerId], [ProfileId], [DriverId], [ScheduledTime], [DestinationId])
GO
CREATE STATISTICS [_dta_stat_1166627199_8_3_1_39_5_38_12_9_13] ON [dbo].[Loads] ([DriverId], [CustomerId], [Id], [LabTestId], [ProfileId], [DispatchStatus], [ScheduledDate], [TruckId], [ScheduledTime])
GO
CREATE STATISTICS [_dta_stat_1166627199_8_3_1_5] ON [dbo].[Loads] ([DriverId], [CustomerId], [Id], [ProfileId])
GO
CREATE STATISTICS [_dta_stat_1166627199_8_30_1_3_39_5_12] ON [dbo].[Loads] ([DriverId], [DestinationId], [Id], [CustomerId], [LabTestId], [ProfileId], [ScheduledDate])
GO
CREATE STATISTICS [_dta_stat_1166627199_1_30_39_3_5_8_38] ON [dbo].[Loads] ([Id], [DestinationId], [LabTestId], [CustomerId], [ProfileId], [DriverId], [DispatchStatus])
GO
CREATE STATISTICS [_dta_stat_1166627199_1_30_5_9_39_38_12] ON [dbo].[Loads] ([Id], [DestinationId], [ProfileId], [TruckId], [LabTestId], [DispatchStatus], [ScheduledDate])
GO
CREATE STATISTICS [_dta_stat_1166627199_1_30_12_7_39_5_8_3] ON [dbo].[Loads] ([Id], [DestinationId], [ScheduledDate], [TransporterId], [LabTestId], [ProfileId], [DriverId], [CustomerId])
GO
CREATE STATISTICS [_dta_stat_1166627199_1_39_8] ON [dbo].[Loads] ([Id], [LabTestId], [DriverId])
GO
CREATE STATISTICS [_dta_stat_1166627199_1_39_9] ON [dbo].[Loads] ([Id], [LabTestId], [TruckId])
GO
CREATE STATISTICS [_dta_stat_1166627199_1_12_3] ON [dbo].[Loads] ([Id], [ScheduledDate], [CustomerId])
GO
CREATE STATISTICS [_dta_stat_1166627199_39_30_5_3_12_1] ON [dbo].[Loads] ([LabTestId], [DestinationId], [ProfileId], [CustomerId], [ScheduledDate], [Id])
GO
CREATE STATISTICS [_dta_stat_1166627199_39_38_1_5_30] ON [dbo].[Loads] ([LabTestId], [DispatchStatus], [Id], [ProfileId], [DestinationId])
GO
CREATE STATISTICS [_dta_stat_1166627199_39_38_1_12_9] ON [dbo].[Loads] ([LabTestId], [DispatchStatus], [Id], [ScheduledDate], [TruckId])
GO
CREATE STATISTICS [_dta_stat_1166627199_39_1_3_30_12_7] ON [dbo].[Loads] ([LabTestId], [Id], [CustomerId], [DestinationId], [ScheduledDate], [TransporterId])
GO
CREATE STATISTICS [_dta_stat_1166627199_5_30_9_39_38] ON [dbo].[Loads] ([ProfileId], [DestinationId], [TruckId], [LabTestId], [DispatchStatus])
GO
CREATE STATISTICS [_dta_stat_1166627199_5_38_1_8] ON [dbo].[Loads] ([ProfileId], [DispatchStatus], [Id], [DriverId])
GO
CREATE STATISTICS [hind_1166627199_5A_38A_12A_13A_1A_3A_4A_6A_8A_14A_15A_26A_27A_28A_29A_33A] ON [dbo].[Loads] ([ProfileId], [DispatchStatus], [ScheduledDate], [ScheduledTime], [Id], [CustomerId], [VendorId], [LoadType], [DriverId], [ActualDate], [ActualTime], [ContactName], [ContactPhone], [PickupLocation], [VesselTank], [EquipmentType])
GO
CREATE STATISTICS [_dta_stat_1166627199_5_1_9] ON [dbo].[Loads] ([ProfileId], [Id], [TruckId])
GO
CREATE STATISTICS [_dta_stat_1166627199_5_39_38] ON [dbo].[Loads] ([ProfileId], [LabTestId], [DispatchStatus])
GO
CREATE STATISTICS [_dta_stat_1166627199_5_12_1_30_8] ON [dbo].[Loads] ([ProfileId], [ScheduledDate], [Id], [DestinationId], [DriverId])
GO
CREATE STATISTICS [_dta_stat_1166627199_5_12_10] ON [dbo].[Loads] ([ProfileId], [ScheduledDate], [TrailerId])
GO
CREATE STATISTICS [_dta_stat_1166627199_5_10] ON [dbo].[Loads] ([ProfileId], [TrailerId])
GO
CREATE STATISTICS [_dta_stat_1166627199_12_30] ON [dbo].[Loads] ([ScheduledDate], [DestinationId])
GO
CREATE STATISTICS [_dta_stat_1166627199_12_30_8_3] ON [dbo].[Loads] ([ScheduledDate], [DestinationId], [DriverId], [CustomerId])
GO
CREATE STATISTICS [_dta_stat_1166627199_12_38_3_5] ON [dbo].[Loads] ([ScheduledDate], [DispatchStatus], [CustomerId], [ProfileId])
GO
CREATE STATISTICS [_dta_stat_1166627199_12_8_30_1_3_39] ON [dbo].[Loads] ([ScheduledDate], [DriverId], [DestinationId], [Id], [CustomerId], [LabTestId])
GO
CREATE STATISTICS [_dta_stat_1166627199_12_8_1_3_5_30] ON [dbo].[Loads] ([ScheduledDate], [DriverId], [Id], [CustomerId], [ProfileId], [DestinationId])
GO
CREATE STATISTICS [_dta_stat_1166627199_12_1_39] ON [dbo].[Loads] ([ScheduledDate], [Id], [LabTestId])
GO
CREATE STATISTICS [_dta_stat_1166627199_12_1_39_5_30] ON [dbo].[Loads] ([ScheduledDate], [Id], [LabTestId], [ProfileId], [DestinationId])
GO
CREATE STATISTICS [_dta_stat_1166627199_12_1_5_3_30_7_39] ON [dbo].[Loads] ([ScheduledDate], [Id], [ProfileId], [CustomerId], [DestinationId], [TransporterId], [LabTestId])
GO
CREATE STATISTICS [_dta_stat_1166627199_12_1_5_8_3_13_30_7_39_9] ON [dbo].[Loads] ([ScheduledDate], [Id], [ProfileId], [DriverId], [CustomerId], [ScheduledTime], [DestinationId], [TransporterId], [LabTestId], [TruckId])
GO
CREATE STATISTICS [_dta_stat_1166627199_12_1_9_30] ON [dbo].[Loads] ([ScheduledDate], [Id], [TruckId], [DestinationId])
GO
CREATE STATISTICS [_dta_stat_1166627199_12_39_30_5] ON [dbo].[Loads] ([ScheduledDate], [LabTestId], [DestinationId], [ProfileId])
GO
CREATE STATISTICS [_dta_stat_1166627199_12_13_38] ON [dbo].[Loads] ([ScheduledDate], [ScheduledTime], [DispatchStatus])
GO
CREATE STATISTICS [_dta_stat_1166627199_12_13_8_3_38_39_9] ON [dbo].[Loads] ([ScheduledDate], [ScheduledTime], [DriverId], [CustomerId], [DispatchStatus], [LabTestId], [TruckId])
GO
CREATE STATISTICS [_dta_stat_1166627199_12_13_10] ON [dbo].[Loads] ([ScheduledDate], [ScheduledTime], [TrailerId])
GO
CREATE STATISTICS [_dta_stat_1166627199_12_13_10_38] ON [dbo].[Loads] ([ScheduledDate], [ScheduledTime], [TrailerId], [DispatchStatus])
GO
CREATE STATISTICS [_dta_stat_1166627199_12_10] ON [dbo].[Loads] ([ScheduledDate], [TrailerId])
GO
CREATE STATISTICS [_dta_stat_1166627199_12_9_1_5_39_38] ON [dbo].[Loads] ([ScheduledDate], [TruckId], [Id], [ProfileId], [LabTestId], [DispatchStatus])
GO
CREATE STATISTICS [_dta_stat_1166627199_12_9_13_8_3_38] ON [dbo].[Loads] ([ScheduledDate], [TruckId], [ScheduledTime], [DriverId], [CustomerId], [DispatchStatus])
GO
CREATE STATISTICS [_dta_stat_1166627199_13_3_12_30_7_39_9] ON [dbo].[Loads] ([ScheduledTime], [CustomerId], [ScheduledDate], [DestinationId], [TransporterId], [LabTestId], [TruckId])
GO
CREATE STATISTICS [_dta_stat_1166627199_13_12_30_7_39_9] ON [dbo].[Loads] ([ScheduledTime], [ScheduledDate], [DestinationId], [TransporterId], [LabTestId], [TruckId])
GO
CREATE STATISTICS [_dta_stat_1166627199_13_9_3_12] ON [dbo].[Loads] ([ScheduledTime], [TruckId], [CustomerId], [ScheduledDate])
GO
CREATE STATISTICS [_dta_stat_1166627199_10_38_5_12_13] ON [dbo].[Loads] ([TrailerId], [DispatchStatus], [ProfileId], [ScheduledDate], [ScheduledTime])
GO
CREATE STATISTICS [_dta_stat_1166627199_9_39_38_1] ON [dbo].[Loads] ([TruckId], [LabTestId], [DispatchStatus], [Id])
GO
CREATE STATISTICS [_dta_stat_1166627199_9_5] ON [dbo].[Loads] ([TruckId], [ProfileId])
GO
CREATE STATISTICS [hind_1166627199_68A_1A_69A] ON [dbo].[Loads] ([UpdateDateTime], [Id], [UpdateUser])
GO
CREATE STATISTICS [hind_1166627199_68A_69A_1A] ON [dbo].[Loads] ([UpdateDateTime], [UpdateUser], [Id])
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwExportLoadLabVolume]](../Views/dbo_vwExportLoadLabVolume.md)
* [[dbo].[vwExportLoadVolume]](../Views/dbo_vwExportLoadVolume.md)
* [[dbo].[vwRptLoadAccounting]](../Views/dbo_vwRptLoadAccounting.md)
* [[dbo].[vwRptLoadBillingAccounting]](../Views/dbo_vwRptLoadBillingAccounting.md)
* [[dbo].[vwRptLoadBillingAccountingNew]](../Views/dbo_vwRptLoadBillingAccountingNew.md)
* [[dbo].[vwRptLoadBillingDetail]](../Views/dbo_vwRptLoadBillingDetail.md)
* [[dbo].[vwRptLoadBillingSummary]](../Views/dbo_vwRptLoadBillingSummary.md)
* [[dbo].[vwRptLoadBOL]](../Views/dbo_vwRptLoadBOL.md)
* [[dbo].[vwRptLoadDriverTimeLog]](../Views/dbo_vwRptLoadDriverTimeLog.md)
* [[dbo].[vwRptLoadInternalTruck]](../Views/dbo_vwRptLoadInternalTruck.md)
* [[dbo].[vwRptLoadInternalTruckNew]](../Views/dbo_vwRptLoadInternalTruckNew.md)
* [[dbo].[vwRptLoadInventoryDetails]](../Views/dbo_vwRptLoadInventoryDetails.md)
* [[dbo].[vwRptLoadLabPadTimes]](../Views/dbo_vwRptLoadLabPadTimes.md)
* [[dbo].[vwRptLoadManifest]](../Views/dbo_vwRptLoadManifest.md)
* [[dbo].[vwRptLoadMaterialDestination]](../Views/dbo_vwRptLoadMaterialDestination.md)
* [[dbo].[vwRptLoadMaterialGenerator]](../Views/dbo_vwRptLoadMaterialGenerator.md)
* [[dbo].[vwRptLoadMaterialGeneratorKStarks]](../Views/dbo_vwRptLoadMaterialGeneratorKStarks.md)
* [[dbo].[vwRptLoadMaterialGeneratorKStarksProfileNo]](../Views/dbo_vwRptLoadMaterialGeneratorKStarksProfileNo.md)
* [[dbo].[vwRptLoadSchedule]](../Views/dbo_vwRptLoadSchedule.md)
* [[dbo].[vwRptLoadScheduleByPump]](../Views/dbo_vwRptLoadScheduleByPump.md)
* [[dbo].[vwRptLoadScheduleNew]](../Views/dbo_vwRptLoadScheduleNew.md)
* [[dbo].[vwRptLoadsTrailerStorage]](../Views/dbo_vwRptLoadsTrailerStorage.md)
* [[dbo].[vwRptLoadTCEQ]](../Views/dbo_vwRptLoadTCEQ.md)
* [[dbo].[vwRptSelectSchedulePumpTimes]](../Views/dbo_vwRptSelectSchedulePumpTimes.md)
* [[dbo].[vwRptSelectScheduleTimes]](../Views/dbo_vwRptSelectScheduleTimes.md)
* [[dbo].[vwRptWasteLoads]](../Views/dbo_vwRptWasteLoads.md)
* [[dbo].[vwSaturnTestLoads]](../Views/dbo_vwSaturnTestLoads.md)
* [[dbo].[vwSelectAvailableForScheduledLoadsAll]](../Views/dbo_vwSelectAvailableForScheduledLoadsAll.md)
* [[dbo].[vwSelectAvailableForScheduledLoadsPending]](../Views/dbo_vwSelectAvailableForScheduledLoadsPending.md)
* [[dbo].[vwSelectAvailableForScheduledLoadsScheduled]](../Views/dbo_vwSelectAvailableForScheduledLoadsScheduled.md)
* [[dbo].[vwSelectCustomerStopInformation]](../Views/dbo_vwSelectCustomerStopInformation.md)
* [[dbo].[vwSelectEManifest]](../Views/dbo_vwSelectEManifest.md)
* [[dbo].[vwSelectEquipmentLastLoadDescription]](../Views/dbo_vwSelectEquipmentLastLoadDescription.md)
* [[dbo].[vwSelectExportBayportTimes]](../Views/dbo_vwSelectExportBayportTimes.md)
* [[dbo].[vwSelectExportIntergulfDriversOnSiteTime]](../Views/dbo_vwSelectExportIntergulfDriversOnSiteTime.md)
* [[dbo].[vwSelectExportLoadLabVolume]](../Views/dbo_vwSelectExportLoadLabVolume.md)
* [[dbo].[vwSelectExportLoadLabVolumeNew]](../Views/dbo_vwSelectExportLoadLabVolumeNew.md)
* [[dbo].[vwSelectExportLoadsForEBE]](../Views/dbo_vwSelectExportLoadsForEBE.md)
* [[dbo].[vwSelectExportLoadsForEBETemp]](../Views/dbo_vwSelectExportLoadsForEBETemp.md)
* [[dbo].[vwSelectExportLoadsForSchedule]](../Views/dbo_vwSelectExportLoadsForSchedule.md)
* [[dbo].[vwSelectExportLoadsForSteers]](../Views/dbo_vwSelectExportLoadsForSteers.md)
* [[dbo].[vwSelectExportLoadsTruckTimes]](../Views/dbo_vwSelectExportLoadsTruckTimes.md)
* [[dbo].[vwSelectExportProfileNewBusiness]](../Views/dbo_vwSelectExportProfileNewBusiness.md)
* [[dbo].[vwSelectExportProfilesNew]](../Views/dbo_vwSelectExportProfilesNew.md)
* [[dbo].[vwSelectExportProfileVolume]](../Views/dbo_vwSelectExportProfileVolume.md)
* [[dbo].[vwSelectExportStrangTimes]](../Views/dbo_vwSelectExportStrangTimes.md)
* [[dbo].[vwSelectExportToSage]](../Views/dbo_vwSelectExportToSage.md)
* [[dbo].[vwSelectExportToSageAccrual]](../Views/dbo_vwSelectExportToSageAccrual.md)
* [[dbo].[vwSelectExportToSageTest]](../Views/dbo_vwSelectExportToSageTest.md)
* [[dbo].[vwSelectLabTestLatentTests]](../Views/dbo_vwSelectLabTestLatentTests.md)
* [[dbo].[vwSelectLastLoadInformation]](../Views/dbo_vwSelectLastLoadInformation.md)
* [[dbo].[vwSelectLegOneDriverOnSiteTime]](../Views/dbo_vwSelectLegOneDriverOnSiteTime.md)
* [[dbo].[vwSelectLoadBillingTimes]](../Views/dbo_vwSelectLoadBillingTimes.md)
* [[dbo].[vwSelectLoadCTCount]](../Views/dbo_vwSelectLoadCTCount.md)
* [[dbo].[vwSelectLoadDriver]](../Views/dbo_vwSelectLoadDriver.md)
* [[dbo].[vwSelectLoadForSchedule]](../Views/dbo_vwSelectLoadForSchedule.md)
* [[dbo].[vwSelectLoadLabCopper06087]](../Views/dbo_vwSelectLoadLabCopper06087.md)
* [[dbo].[vwSelectLoadPadTimesForExport]](../Views/dbo_vwSelectLoadPadTimesForExport.md)
* [[dbo].[vwSelectLoadProfileMaterialCode]](../Views/dbo_vwSelectLoadProfileMaterialCode.md)
* [[dbo].[vwSelectLoadRequestForOverage]](../Views/dbo_vwSelectLoadRequestForOverage.md)
* [[dbo].[vwSelectLoadRequestLoadTimes]](../Views/dbo_vwSelectLoadRequestLoadTimes.md)
* [[dbo].[vwSelectLoads]](../Views/dbo_vwSelectLoads.md)
* [[dbo].[vwSelectLoads4thQtrBayportLoadTimes]](../Views/dbo_vwSelectLoads4thQtrBayportLoadTimes.md)
* [[dbo].[vwSelectLoadsByProfileCreateDate]](../Views/dbo_vwSelectLoadsByProfileCreateDate.md)
* [[dbo].[vwSelectLoadsCount]](../Views/dbo_vwSelectLoadsCount.md)
* [[dbo].[vwSelectLoadsEManifestCheck]](../Views/dbo_vwSelectLoadsEManifestCheck.md)
* [[dbo].[vwSelectLoadsFor225ByMonth]](../Views/dbo_vwSelectLoadsFor225ByMonth.md)
* [[dbo].[vwSelectLoadsForBayportCWaste]](../Views/dbo_vwSelectLoadsForBayportCWaste.md)
* [[dbo].[vwSelectLoadsForBayportTurnTimes]](../Views/dbo_vwSelectLoadsForBayportTurnTimes.md)
* [[dbo].[vwSelectLoadsForSaturn]](../Views/dbo_vwSelectLoadsForSaturn.md)
* [[dbo].[vwSelectLoadsInactive]](../Views/dbo_vwSelectLoadsInactive.md)
* [[dbo].[vwSelectLoadsLabForAProfile]](../Views/dbo_vwSelectLoadsLabForAProfile.md)
* [[dbo].[vwSelectLoadsMotiva20121001]](../Views/dbo_vwSelectLoadsMotiva20121001.md)
* [[dbo].[vwSelectLoadsScheduleCreateUser]](../Views/dbo_vwSelectLoadsScheduleCreateUser.md)
* [[dbo].[vwSelectLoadsScheduled]](../Views/dbo_vwSelectLoadsScheduled.md)
* [[dbo].[vwSelectLoadsScheduledForChart]](../Views/dbo_vwSelectLoadsScheduledForChart.md)
* [[dbo].[vwSelectLoadsScheduledLoad]](../Views/dbo_vwSelectLoadsScheduledLoad.md)
* [[dbo].[vwSelectLoadsScheduleForExport]](../Views/dbo_vwSelectLoadsScheduleForExport.md)
* [[dbo].[vwSelectLoadsWithProfileExpDateToMarkInactive]](../Views/dbo_vwSelectLoadsWithProfileExpDateToMarkInactive.md)
* [[dbo].[vwSelectMonthlyDischarge]](../Views/dbo_vwSelectMonthlyDischarge.md)
* [[dbo].[vwSelectPendingLoads]](../Views/dbo_vwSelectPendingLoads.md)
* [[dbo].[vwSelectProfileActiveLastLoadDate]](../Views/dbo_vwSelectProfileActiveLastLoadDate.md)
* [[dbo].[vwSelectProfileActiveLastLoadDateNew]](../Views/dbo_vwSelectProfileActiveLastLoadDateNew.md)
* [[dbo].[vwSelectProfileRecertificationDays]](../Views/dbo_vwSelectProfileRecertificationDays.md)
* [[dbo].[vwSelectProfilesRecertificationDateExpired]](../Views/dbo_vwSelectProfilesRecertificationDateExpired.md)
* [[dbo].[vwSelectProfileVolumeQuantity]](../Views/dbo_vwSelectProfileVolumeQuantity.md)
* [[dbo].[vwSelectProfileVolumeTest]](../Views/dbo_vwSelectProfileVolumeTest.md)
* [[dbo].[vwSelectSaturnTransactions]](../Views/dbo_vwSelectSaturnTransactions.md)
* [[dbo].[vwSelectSaturnTransactionsBackup]](../Views/dbo_vwSelectSaturnTransactionsBackup.md)
* [[dbo].[vwSelectSaturnTransactionsLoads]](../Views/dbo_vwSelectSaturnTransactionsLoads.md)
* [[dbo].[vwSelectScheduledLoads]](../Views/dbo_vwSelectScheduledLoads.md)
* [[dbo].[vwSelectTrailerLastLoad]](../Views/dbo_vwSelectTrailerLastLoad.md)
* [[dbo].[vwSelectTrailerScheduledLoads]](../Views/dbo_vwSelectTrailerScheduledLoads.md)
* [[dbo].[vwSelectWashoutAllTables]](../Views/dbo_vwSelectWashoutAllTables.md)
* [[dbo].[vwSteersTest]](../Views/dbo_vwSteersTest.md)
* [[dbo].[fnIsTrailerLoaded]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnIsTrailerLoaded.md)
* [[dbo].[fnIsTrailerPlanned]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnIsTrailerPlanned.md)
* [[dbo].[fnIsTrailerScheduled]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnIsTrailerScheduled.md)
* [[dbo].[fnSelectLoads]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectLoads.md)
* [[dbo].[fnSelectOneLoads]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectOneLoads.md)
* [[dbo].[fnSelectPendingLoads]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectPendingLoads.md)
* [[dbo].[fnSelectProfileVolume]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnSelectProfileVolume.md)
* [[dbo].[fnSelectScheduledLoads]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectScheduledLoads.md)
* [[dbo].[fnTrailerLastLoadDescription]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnTrailerLastLoadDescription.md)
* [[dbo].[fnTrailerLastLoadId]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnTrailerLastLoadId.md)
* [[dbo].[fnTrailerTest]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnTrailerTest.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

