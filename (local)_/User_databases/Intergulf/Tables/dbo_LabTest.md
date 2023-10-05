#### 

[Project](../../../../index.md) > [(local)\\](../../../index.md) > [User databases](../../index.md) > [Intergulf](../index.md) > [Tables](Tables.md) > dbo.LabTest

# ![Tables](../../../../Images/Table32.png) [dbo].[LabTest]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | SQL_Latin1_General_CP1_CI_AS |
| Row Count (~) | 335119 |
| Created | 5:09:33 PM Tuesday, April 17, 2007 |
| Last Modified | 8:10:17 PM Wednesday, December 14, 2022 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_LabTest: Id](../../../../Images/pkcluster.png)](#indexes)[![Indexes _dta_index_LabTest_5_446624634__K86_K70_K6_K2_1_14, _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes)(2) | Id | bigint | 8 | NOT NULL | 1 - 1 |
| [![Indexes _dta_index_LabTest_5_446624634__K86_K70_K6_K2_1_14, _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_, _dta_stat_446624634_2_86_70, _dta_stat_446624634_2_6_86, _dta_stat_446624634_6_86_70_2, _dta_stat_446624634_6_77_2_5_4_3](../../../../Images/Index.png)](#indexes)(6) | LoadId | decimal(18,0) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_, _dta_stat_446624634_5_4_3_6_7, _dta_stat_446624634_6_77_2_5_4_3, _dta_stat_446624634_6_77_5_4_3](../../../../Images/Index.png)](#indexes)(4) | CustomerId | decimal(18,0) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_, _dta_stat_446624634_5_4_3_6_7, _dta_stat_446624634_6_7_5_4, _dta_stat_446624634_6_4_5, _dta_stat_446624634_6_77_2_5_4_3, _dta_stat_446624634_6_77_5_4_3](../../../../Images/Index.png)](#indexes)(6) | GeneratorId | decimal(18,0) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_, _dta_stat_446624634_5_4_3_6_7, _dta_stat_446624634_6_7_5_4, _dta_stat_446624634_6_4_5, _dta_stat_446624634_6_77_2_5_4_3, _dta_stat_446624634_6_77_5_4_3](../../../../Images/Index.png)](#indexes)(6) | ProfileId | decimal(18,0) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K86_K70_K6_K2_1_14, _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_, _dta_stat_446624634_2_6_86, _dta_stat_446624634_5_4_3_6_7, _dta_stat_446624634_70_6, _dta_stat_446624634_6_7_5_4, _dta_stat_446624634_6_4_5, _dta_stat_446624634_6_86_70_2, _dta_stat_446624634_6_77_2_5_4_3, _dta_stat_446624634_6_77_5_4_3](../../../../Images/Index.png)](#indexes)(10) | TestDate | datetime | 8 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_, _dta_stat_446624634_5_4_3_6_7, _dta_stat_446624634_6_7_5_4](../../../../Images/Index.png)](#indexes)(3) | DocumentNumber | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | DocumentType | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | TruckNumber | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | TransporterId | decimal(18,0) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | DriverId | decimal(18,0) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | LabTechId | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | ApprovedById | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K86_K70_K6_K2_1_14, _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes)(2) | StartTime | datetime | 8 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | EndTime | datetime | 8 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | Quantity | decimal(18,0) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | Units | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | PcntWater | decimal(18,2) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | PcntOil | decimal(18,2) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | PcntSolids | decimal(18,2) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | PreFlashPoint | varchar(5) | 5 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | FlashPoint | decimal(18,0) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | PreAPI | varchar(5) | 5 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | API | decimal(18,1) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | PreTemperature | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | Temperature | decimal(18,0) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | PreAdjAPI | varchar(5) | 5 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | AdjAPI | decimal(18,1) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | GrossWeight | decimal(18,0) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | TareWeight | decimal(18,0) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | NetWeight | decimal(18,0) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | WashOut | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | Compatibility | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | PrePetroleumCOD | varchar(5) | 5 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | PetroleumCOD | decimal(18,0) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | PrePetroleumAPI | varchar(5) | 5 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | PetroleumAPI | decimal(18,1) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | PrePetroleumTemp | varchar(5) | 5 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | PetroleumTemp | decimal(18,0) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | PrePetroleumAdjAPI | varchar(5) | 5 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | PetroleumAdjAPI | decimal(18,1) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | PrePetroleumFlashPoint | varchar(5) | 5 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | PetroleumFlashPoint | decimal(18,0) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | PrePetroleumChlordetect | varchar(5) | 5 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | PetroleumChlordetect | decimal(18,0) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | PrePetroleumAsh | varchar(5) | 5 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | PetroleumAsh | decimal(18,4) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | PrePetroleumPcntWater | varchar(5) | 5 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | PetroleumPcntWater | decimal(18,1) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | PreAqueousCOD | varchar(5) | 5 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | AqueousCOD | decimal(18,0) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | PreAqueousAPI | varchar(5) | 5 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | AqueousAPI | decimal(18,1) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | PreAqueousTemp | varchar(5) | 5 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | AqueousTemp | decimal(18,0) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | PreAqueousAdjAPI | varchar(5) | 5 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | AqueousAdjAPI | decimal(18,1) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | PreAqueousFlashPoint | varchar(5) | 5 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | AqueousFlashPoint | decimal(18,0) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | PreAqueousPH | varchar(5) | 5 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | AqueousPH | decimal(18,1) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | PreAqueousAmmonia | varchar(5) | 5 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | AqueousAmmonia | decimal(18,0) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | PreAqueousZinc | varchar(5) | 5 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | AqueousZinc | decimal(18,2) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | PreAqueousCopper | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | AqueousCopper | decimal(18,2) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | WeightTicketNumber | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | Notes | varchar(5000) | 5000 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K86_K70_K6_K2_1_14, _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_, _dta_stat_446624634_2_86_70, _dta_stat_446624634_70_6, _dta_stat_446624634_6_86_70_2](../../../../Images/Index.png)](#indexes)(5) | Status | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | StatusDescription | varchar(2000) | 2000 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | ReportTo | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | BillingStatus | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | UpdateDateTime | datetime | 8 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | UpdateUser | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | UpdateComputer | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_, _dta_stat_446624634_6_77_2_5_4_3, _dta_stat_446624634_6_77_5_4_3](../../../../Images/Index.png)](#indexes)(3) | Location | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | Destination | varchar(50) | 50 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | AirPermitTracking | varchar(3) | 3 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | HandlingCode | varchar(10) | 10 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | PcntRags | decimal(18,2) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | PrePetroleumPour | varchar(5) | 5 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | PetroleumPour | decimal(18,0) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | PreAqueousToc | varchar(5) | 5 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | AqueousToc | decimal(18,0) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K86_K70_K6_K2_1_14, _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_, _dta_stat_446624634_2_86_70, _dta_stat_446624634_2_6_86, _dta_stat_446624634_6_86_70_2](../../../../Images/Index.png)](#indexes)(5) | LatentEmailSent | varchar(3) | 3 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | ActualQuantity | decimal(18,0) | 9 | NULL allowed |  |
| [![Indexes _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_](../../../../Images/Index.png)](#indexes) | ActualUnits | varchar(50) | 50 | NULL allowed |  |
|  | PCNumber | decimal(18,0) | 9 | NULL allowed |  |
|  | TreatmentCode | varchar(50) | 50 | NULL allowed |  |
|  | PrePCB | varchar(3) | 3 | NULL allowed |  |
|  | PCB | decimal(18,3) | 9 | NULL allowed |  |
|  | PreVOC | varchar(3) | 3 | NULL allowed |  |
|  | VOC | decimal(18,3) | 9 | NULL allowed |  |
|  | PetroleumSulfurMType | varchar(10) | 10 | NULL allowed |  |
|  | PetroleumSulfur | decimal(18,2) | 9 | NULL allowed |  |
|  | PetroleumSeds | decimal(18,2) | 9 | NULL allowed |  |
|  | PetroleumViscosity | decimal(18,2) | 9 | NULL allowed |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Included Columns | Unique |
|---|---|---|---|---|
| [![Cluster Primary Key PK_LabTest: Id](../../../../Images/pkcluster.png)](#indexes) | PK_LabTest | Id |  | YES |
|  | _dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_ | LoadId | Id, CustomerId, GeneratorId, ProfileId, TestDate, AqueousToc, LatentEmailSent, ActualQuantity, ActualUnits, AirPermitTracking, HandlingCode, PcntRags, PrePetroleumPour, PetroleumPour, PreAqueousToc, BillingStatus, UpdateDateTime, UpdateUser, UpdateComputer, Location, Destination, AqueousCopper, WeightTicketNumber, Notes, Status, StatusDescription, ReportTo, AqueousPH, PreAqueousAmmonia, AqueousAmmonia, PreAqueousZinc, AqueousZinc, PreAqueousCopper, AqueousTemp, PreAqueousAdjAPI, AqueousAdjAPI, PreAqueousFlashPoint, AqueousFlashPoint, PreAqueousPH, PetroleumPcntWater, PreAqueousCOD, AqueousCOD, PreAqueousAPI, AqueousAPI, PreAqueousTemp, PetroleumFlashPoint, PrePetroleumChlordetect, PetroleumChlordetect, PrePetroleumAsh, PetroleumAsh, PrePetroleumPcntWater, PetroleumAPI, PrePetroleumTemp, PetroleumTemp, PrePetroleumAdjAPI, PetroleumAdjAPI, PrePetroleumFlashPoint, NetWeight, WashOut, Compatibility, PrePetroleumCOD, PetroleumCOD, PrePetroleumAPI, PreTemperature, Temperature, PreAdjAPI, AdjAPI, GrossWeight, TareWeight, PcntOil, PcntSolids, PreFlashPoint, FlashPoint, PreAPI, API, ApprovedById, StartTime, EndTime, Quantity, Units, PcntWater, DocumentNumber, DocumentType, TruckNumber, TransporterId, DriverId, LabTechId |  |
|  | _dta_index_LabTest_5_446624634__K86_K70_K6_K2_1_14 | LatentEmailSent, Status, TestDate, LoadId | Id, StartTime |  |


---

## <a name="#statistics"></a>Statistics

| Name | Key Columns |
|---|---|
| _dta_stat_446624634_2_6_86 | LoadId, TestDate, LatentEmailSent |
| _dta_stat_446624634_2_86_70 | LoadId, LatentEmailSent, Status |
| _dta_stat_446624634_5_4_3_6_7 | ProfileId, GeneratorId, CustomerId, TestDate, DocumentNumber |
| _dta_stat_446624634_6_4_5 | TestDate, GeneratorId, ProfileId |
| _dta_stat_446624634_6_77_2_5_4_3 | TestDate, Location, LoadId, ProfileId, GeneratorId, CustomerId |
| _dta_stat_446624634_6_77_5_4_3 | TestDate, Location, ProfileId, GeneratorId, CustomerId |
| _dta_stat_446624634_6_7_5_4 | TestDate, DocumentNumber, ProfileId, GeneratorId |
| _dta_stat_446624634_6_86_70_2 | TestDate, LatentEmailSent, Status, LoadId |
| _dta_stat_446624634_70_6 | Status, TestDate |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[LabTest]
(
[Id] [bigint] NOT NULL IDENTITY(1, 1),
[LoadId] [decimal] (18, 0) NULL,
[CustomerId] [decimal] (18, 0) NULL,
[GeneratorId] [decimal] (18, 0) NULL,
[ProfileId] [decimal] (18, 0) NULL,
[TestDate] [datetime] NULL,
[DocumentNumber] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[DocumentType] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[TruckNumber] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[TransporterId] [decimal] (18, 0) NULL,
[DriverId] [decimal] (18, 0) NULL,
[LabTechId] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ApprovedById] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[StartTime] [datetime] NULL,
[EndTime] [datetime] NULL,
[Quantity] [decimal] (18, 0) NULL,
[Units] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PcntWater] [decimal] (18, 2) NULL,
[PcntOil] [decimal] (18, 2) NULL,
[PcntSolids] [decimal] (18, 2) NULL,
[PreFlashPoint] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[FlashPoint] [decimal] (18, 0) NULL,
[PreAPI] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[API] [decimal] (18, 1) NULL,
[PreTemperature] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Temperature] [decimal] (18, 0) NULL,
[PreAdjAPI] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[AdjAPI] [decimal] (18, 1) NULL,
[GrossWeight] [decimal] (18, 0) NULL,
[TareWeight] [decimal] (18, 0) NULL,
[NetWeight] [decimal] (18, 0) NULL,
[WashOut] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Compatibility] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PrePetroleumCOD] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PetroleumCOD] [decimal] (18, 0) NULL,
[PrePetroleumAPI] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PetroleumAPI] [decimal] (18, 1) NULL,
[PrePetroleumTemp] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PetroleumTemp] [decimal] (18, 0) NULL,
[PrePetroleumAdjAPI] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PetroleumAdjAPI] [decimal] (18, 1) NULL,
[PrePetroleumFlashPoint] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PetroleumFlashPoint] [decimal] (18, 0) NULL,
[PrePetroleumChlordetect] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PetroleumChlordetect] [decimal] (18, 0) NULL,
[PrePetroleumAsh] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PetroleumAsh] [decimal] (18, 4) NULL,
[PrePetroleumPcntWater] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PetroleumPcntWater] [decimal] (18, 1) NULL,
[PreAqueousCOD] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[AqueousCOD] [decimal] (18, 0) NULL,
[PreAqueousAPI] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[AqueousAPI] [decimal] (18, 1) NULL,
[PreAqueousTemp] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[AqueousTemp] [decimal] (18, 0) NULL,
[PreAqueousAdjAPI] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[AqueousAdjAPI] [decimal] (18, 1) NULL,
[PreAqueousFlashPoint] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[AqueousFlashPoint] [decimal] (18, 0) NULL,
[PreAqueousPH] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[AqueousPH] [decimal] (18, 1) NULL,
[PreAqueousAmmonia] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[AqueousAmmonia] [decimal] (18, 0) NULL,
[PreAqueousZinc] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[AqueousZinc] [decimal] (18, 2) NULL,
[PreAqueousCopper] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[AqueousCopper] [decimal] (18, 2) NULL,
[WeightTicketNumber] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Notes] [varchar] (5000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Status] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[StatusDescription] [varchar] (2000) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ReportTo] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[BillingStatus] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateDateTime] [datetime] NULL,
[UpdateUser] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[UpdateComputer] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Location] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[Destination] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[AirPermitTracking] [varchar] (3) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[HandlingCode] [varchar] (10) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PcntRags] [decimal] (18, 2) NULL,
[PrePetroleumPour] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PetroleumPour] [decimal] (18, 0) NULL,
[PreAqueousToc] [varchar] (5) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[AqueousToc] [decimal] (18, 0) NULL,
[LatentEmailSent] [varchar] (3) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[ActualQuantity] [decimal] (18, 0) NULL,
[ActualUnits] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PCNumber] [decimal] (18, 0) NULL,
[TreatmentCode] [varchar] (50) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PrePCB] [varchar] (3) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PCB] [decimal] (18, 3) NULL,
[PreVOC] [varchar] (3) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[VOC] [decimal] (18, 3) NULL,
[PetroleumSulfurMType] [varchar] (10) COLLATE SQL_Latin1_General_CP1_CI_AS NULL,
[PetroleumSulfur] [decimal] (18, 2) NULL,
[PetroleumSeds] [decimal] (18, 2) NULL,
[PetroleumViscosity] [decimal] (18, 2) NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[LabTest] ADD CONSTRAINT [PK_LabTest] PRIMARY KEY CLUSTERED ([Id]) ON [PRIMARY]
GO
CREATE NONCLUSTERED INDEX [_dta_index_LabTest_5_446624634__K86_K70_K6_K2_1_14] ON [dbo].[LabTest] ([LatentEmailSent], [Status], [TestDate], [LoadId]) INCLUDE ([Id], [StartTime]) ON [PRIMARY]
GO
CREATE NONCLUSTERED INDEX [_dta_index_LabTest_5_446624634__K2_1_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30_31_32_33_34_] ON [dbo].[LabTest] ([LoadId]) INCLUDE ([Id], [CustomerId], [GeneratorId], [ProfileId], [TestDate], [DocumentNumber], [DocumentType], [TruckNumber], [TransporterId], [DriverId], [LabTechId], [ApprovedById], [StartTime], [EndTime], [Quantity], [Units], [PcntWater], [PcntOil], [PcntSolids], [PreFlashPoint], [FlashPoint], [PreAPI], [API], [PreTemperature], [Temperature], [PreAdjAPI], [AdjAPI], [GrossWeight], [TareWeight], [NetWeight], [WashOut], [Compatibility], [PrePetroleumCOD], [PetroleumCOD], [PrePetroleumAPI], [PetroleumAPI], [PrePetroleumTemp], [PetroleumTemp], [PrePetroleumAdjAPI], [PetroleumAdjAPI], [PrePetroleumFlashPoint], [PetroleumFlashPoint], [PrePetroleumChlordetect], [PetroleumChlordetect], [PrePetroleumAsh], [PetroleumAsh], [PrePetroleumPcntWater], [PetroleumPcntWater], [PreAqueousCOD], [AqueousCOD], [PreAqueousAPI], [AqueousAPI], [PreAqueousTemp], [AqueousTemp], [PreAqueousAdjAPI], [AqueousAdjAPI], [PreAqueousFlashPoint], [AqueousFlashPoint], [PreAqueousPH], [AqueousPH], [PreAqueousAmmonia], [AqueousAmmonia], [PreAqueousZinc], [AqueousZinc], [PreAqueousCopper], [AqueousCopper], [WeightTicketNumber], [Notes], [Status], [StatusDescription], [ReportTo], [BillingStatus], [UpdateDateTime], [UpdateUser], [UpdateComputer], [Location], [Destination], [AirPermitTracking], [HandlingCode], [PcntRags], [PrePetroleumPour], [PetroleumPour], [PreAqueousToc], [AqueousToc], [LatentEmailSent], [ActualQuantity], [ActualUnits]) ON [PRIMARY]
GO
CREATE STATISTICS [_dta_stat_446624634_2_86_70] ON [dbo].[LabTest] ([LoadId], [LatentEmailSent], [Status])
GO
CREATE STATISTICS [_dta_stat_446624634_2_6_86] ON [dbo].[LabTest] ([LoadId], [TestDate], [LatentEmailSent])
GO
CREATE STATISTICS [_dta_stat_446624634_5_4_3_6_7] ON [dbo].[LabTest] ([ProfileId], [GeneratorId], [CustomerId], [TestDate], [DocumentNumber])
GO
CREATE STATISTICS [_dta_stat_446624634_70_6] ON [dbo].[LabTest] ([Status], [TestDate])
GO
CREATE STATISTICS [_dta_stat_446624634_6_7_5_4] ON [dbo].[LabTest] ([TestDate], [DocumentNumber], [ProfileId], [GeneratorId])
GO
CREATE STATISTICS [_dta_stat_446624634_6_4_5] ON [dbo].[LabTest] ([TestDate], [GeneratorId], [ProfileId])
GO
CREATE STATISTICS [_dta_stat_446624634_6_86_70_2] ON [dbo].[LabTest] ([TestDate], [LatentEmailSent], [Status], [LoadId])
GO
CREATE STATISTICS [_dta_stat_446624634_6_77_2_5_4_3] ON [dbo].[LabTest] ([TestDate], [Location], [LoadId], [ProfileId], [GeneratorId], [CustomerId])
GO
CREATE STATISTICS [_dta_stat_446624634_6_77_5_4_3] ON [dbo].[LabTest] ([TestDate], [Location], [ProfileId], [GeneratorId], [CustomerId])
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[vwExportLoadLabVolume]](../Views/dbo_vwExportLoadLabVolume.md)
* [[dbo].[vwExportLoadVolume]](../Views/dbo_vwExportLoadVolume.md)
* [[dbo].[vwRptLabTestForm]](../Views/dbo_vwRptLabTestForm.md)
* [[dbo].[vwRptLoadAccounting]](../Views/dbo_vwRptLoadAccounting.md)
* [[dbo].[vwRptLoadInternalTruck]](../Views/dbo_vwRptLoadInternalTruck.md)
* [[dbo].[vwRptLoadInternalTruckNew]](../Views/dbo_vwRptLoadInternalTruckNew.md)
* [[dbo].[vwRptLoadInventoryDetails]](../Views/dbo_vwRptLoadInventoryDetails.md)
* [[dbo].[vwRptLoadMaterialGeneratorKStarks]](../Views/dbo_vwRptLoadMaterialGeneratorKStarks.md)
* [[dbo].[vwRptLoadMaterialGeneratorKStarksProfileNo]](../Views/dbo_vwRptLoadMaterialGeneratorKStarksProfileNo.md)
* [[dbo].[vwRptWasteLoads]](../Views/dbo_vwRptWasteLoads.md)
* [[dbo].[vwSaturnTestLabTest]](../Views/dbo_vwSaturnTestLabTest.md)
* [[dbo].[vwSelectAvailableForScheduledLoadsAll]](../Views/dbo_vwSelectAvailableForScheduledLoadsAll.md)
* [[dbo].[vwSelectAvailableForScheduledLoadsPending]](../Views/dbo_vwSelectAvailableForScheduledLoadsPending.md)
* [[dbo].[vwSelectAvailableForScheduledLoadsScheduled]](../Views/dbo_vwSelectAvailableForScheduledLoadsScheduled.md)
* [[dbo].[vwSelectEManifest]](../Views/dbo_vwSelectEManifest.md)
* [[dbo].[vwSelectExportBayportTimes]](../Views/dbo_vwSelectExportBayportTimes.md)
* [[dbo].[vwSelectExportLoadLabVolume]](../Views/dbo_vwSelectExportLoadLabVolume.md)
* [[dbo].[vwSelectExportLoadLabVolumeNew]](../Views/dbo_vwSelectExportLoadLabVolumeNew.md)
* [[dbo].[vwSelectExportLoadsForEBE]](../Views/dbo_vwSelectExportLoadsForEBE.md)
* [[dbo].[vwSelectExportLoadsForEBETemp]](../Views/dbo_vwSelectExportLoadsForEBETemp.md)
* [[dbo].[vwSelectExportLoadsForSteers]](../Views/dbo_vwSelectExportLoadsForSteers.md)
* [[dbo].[vwSelectExportProfileVolume]](../Views/dbo_vwSelectExportProfileVolume.md)
* [[dbo].[vwSelectExportStrangTimes]](../Views/dbo_vwSelectExportStrangTimes.md)
* [[dbo].[vwSelectExportToSage]](../Views/dbo_vwSelectExportToSage.md)
* [[dbo].[vwSelectExportToSageAccrual]](../Views/dbo_vwSelectExportToSageAccrual.md)
* [[dbo].[vwSelectExportToSageTest]](../Views/dbo_vwSelectExportToSageTest.md)
* [[dbo].[vwSelectLabTest]](../Views/dbo_vwSelectLabTest.md)
* [[dbo].[vwSelectLabTestDisbursement]](../Views/dbo_vwSelectLabTestDisbursement.md)
* [[dbo].[vwSelectLabTestLatentTests]](../Views/dbo_vwSelectLabTestLatentTests.md)
* [[dbo].[vwSelectLastLoadInformation]](../Views/dbo_vwSelectLastLoadInformation.md)
* [[dbo].[vwSelectLoadLabCopper06087]](../Views/dbo_vwSelectLoadLabCopper06087.md)
* [[dbo].[vwSelectLoads4thQtrBayportLoadTimes]](../Views/dbo_vwSelectLoads4thQtrBayportLoadTimes.md)
* [[dbo].[vwSelectLoadsEManifestCheck]](../Views/dbo_vwSelectLoadsEManifestCheck.md)
* [[dbo].[vwSelectLoadsForBayportCWaste]](../Views/dbo_vwSelectLoadsForBayportCWaste.md)
* [[dbo].[vwSelectLoadsForBayportTurnTimes]](../Views/dbo_vwSelectLoadsForBayportTurnTimes.md)
* [[dbo].[vwSelectLoadsLabForAProfile]](../Views/dbo_vwSelectLoadsLabForAProfile.md)
* [[dbo].[vwSelectLoadsMotiva20121001]](../Views/dbo_vwSelectLoadsMotiva20121001.md)
* [[dbo].[vwSelectMonthlyDischarge]](../Views/dbo_vwSelectMonthlyDischarge.md)
* [[dbo].[vwSelectProfileVolumeQuantity]](../Views/dbo_vwSelectProfileVolumeQuantity.md)
* [[dbo].[vwSelectProfileVolumeTest]](../Views/dbo_vwSelectProfileVolumeTest.md)
* [[dbo].[vwSelectSaturnTransactions]](../Views/dbo_vwSelectSaturnTransactions.md)
* [[dbo].[vwSelectSaturnTransactionsBackup]](../Views/dbo_vwSelectSaturnTransactionsBackup.md)
* [[dbo].[vwSelectSaturnTransactionsLoads]](../Views/dbo_vwSelectSaturnTransactionsLoads.md)
* [[dbo].[vwSelectScheduledLoads]](../Views/dbo_vwSelectScheduledLoads.md)
* [[dbo].[vwSelectWashoutAllTables]](../Views/dbo_vwSelectWashoutAllTables.md)
* [[dbo].[vwSteersTest]](../Views/dbo_vwSteersTest.md)
* [[dbo].[fnSelectLabTest]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectLabTest.md)
* [[dbo].[fnSelectOneLabTest]](../Programmability/Functions/Table-valued_Functions/dbo_fnSelectOneLabTest.md)
* [[dbo].[fnSelectProfileVolume]](../Programmability/Functions/Scalar-valued_Functions/dbo_fnSelectProfileVolume.md)


---

###### Author:  Sastry

###### Copyright 2023 - All Rights Reserved

###### Created: Thursday, October 5, 2023 9:55:17 PM

