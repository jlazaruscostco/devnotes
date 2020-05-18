### Value-Added Services

![DataSource Transactional Data](https://help.sap.com/doc/saphelp_ewm94/9.4/en-US/graphics/BICObjDataSourceTransactionalData.gif) DataSource Transactional Data: `0WM_VAS`

 This DataSource provides you with completed value-added services.

#### Technical Data

| Application Component    | Warehouse Management (0WM)              |
| ------------------------ | --------------------------------------- |
| Available as of Release  | SAP SCM 5.1 and SAP EMW 5.1             |
| Shipment                 | SAP NetWeaver 2004s BI Content Add-On 3 |
| Content Versions         | 1                                       |
| RemoteCube-Capable       | No                                      |
| Delta-Capable            | Yes, delta process AIMD                 |
| Extraction from Archives | No                                      |
| Verifiable               | No                                      |

#### Data Modeling

##### Delta Update

![Note](https://help.sap.com/doc/saphelp_ewm94/9.4/en-US/graphics/note.gif) Note

Order Data Management (ODM), which you are using to manage value-added services, dynamically generates details in the table of origin. Therefore, only work structures are specified below in the column for the table of origin.

| Fields in the Extract Structure | Description of the Field in the Extract Structure        | Table of Origin          | Field in the Table of Origin |
| ------------------------------- | -------------------------------------------------------- | ------------------------ | ---------------------------- |
| MANDT                           | Client                                                   |                          |                              |
| ROCANCEL                        | Indicator: Cancel Data Record                            |                          |                              |
| LGNUM                           | Warehouse Number/Warehouse Complex                       | /SCWM/S_VAS_HEADER_INT   | LGNUM                        |
| VAS_ID                          | Value-Added Service                                      | /SCWM/S_VAS_HEADER_INT   | VAS_ID                       |
| VAS_TYPE                        | VAS Order Category                                       | /SCWM/S_VAS_HEADER_INT   | VAS_TYPE                     |
| VAS_ART                         | VAS Order Type                                           | /SCWM/S_VAS_HEADER_INT   | VAS_ART                      |
| STATUS                          | Status of VAS Order                                      | /SCWM/S_VAS_HEADER_INT   | STATUS                       |
| EFFORT_CODE                     | Effort for Handling a VAS                                | /SCWM/S_VAS_HEADER_INT   | EFFORT_CODE                  |
| TZONE                           | Time Zone                                                | /SCWM/S_VAS_HEADER_INT   | TZONE                        |
| CREUSR                          | Created By (User)                                        | /SCWM/S_VAS_HEADER_INT   | CREUSR                       |
| CRETST                          | Created On                                               | /SCWM/S_VAS_HEADER_INT   | CRETST                       |
| CREDATE                         | Created On                                               | /SCWM/S_VAS_HEADER_INT   | CREDATE                      |
| CRETIME                         | Created At                                               | /SCWM/S_VAS_HEADER_INT   | CRETIME                      |
| CHGUSR                          | ODM: User, Changed By                                    | /SCWM/S_VAS_HEADER_INT   | CHGUSR                       |
| CHGTST                          | ODM: Date/Time Changed                                   | /SCWM/S_VAS_HEADER_INT   | CHGTST                       |
| CHGDATE                         | Changed On                                               | /SCWM/S_VAS_HEADER_INT   | CHGDATE                      |
| CHGTIME                         | Changed At                                               | /SCWM/S_VAS_HEADER_INT   | CHGTIME                      |
| PS_ID                           | Packaging Specification ID                               | /SCWM/S_VAS_HEADER_INT   | PS_ID                        |
| PLAN_START_DATE                 | Planned Start Date                                       | /SCWM/S_VAS_HEADER_INT   | PLAN_START_DATE              |
| PLAN_START_TIME                 | Planned Start Time                                       | /SCWM/S_VAS_HEADER_INT   | PLAN_START_TIME              |
| PL_END_TIME                     | ODM: Finish Date/Time                                    | /SCWM/S_VAS_HEADER_INT   | PL_COMPL_DATE                |
| PLAN_END_DATE                   | Planned End Date                                         | /SCWM/S_VAS_HEADER_INT   | PLAN_END_DATE                |
| PLAN_END_TIME                   | Planned End Time                                         | /SCWM/S_VAS_HEADER_INT   | PLAN_END_TIME                |
| ACT_SEQ                         | Sequence Number of VAS Activity or Item                  | /SCWM/S_VAS_ACTIVITY_INT | ACT_SEQ                      |
| ACT_STATUS                      | Status of VAS Order                                      | /SCWM/S_VAS_ACTIVITY_INT | ACT_STATUS                   |
| ACT_CHGUSR                      | ODM: User, Changed By                                    | /SCWM/S_VAS_ACTIVITY_INT | ACT_CHGUSR                   |
| ACT_PLAN_MATNR                  | Product                                                  | /SCWM/S_VAS_ACTIVITY_INT | ACT_PLAN_MATNR               |
| ACT_PLAN_QTY                    | Delivery Quantity                                        | /SCWM/S_VAS_ACTIVITY_INT | ACT_PLAN_QTY                 |
| ACT_COMPLQTY                    | VAS: Completed Quantity                                  | /SCWM/S_VAS_ACTIVITY_INT | ACT_COMPLQTY                 |
| ACT_PLAN_QTY_UOM                | Unit of Measure                                          | /SCWM/S_VAS_ACTIVITY_INT | ACT_PLAN_QTY_UOM             |
| WORKCENTER                      | Name of Work Center in Warehouse                         | /SCWM/S_VAS_ACTIVITY_INT | WORKCENTER                   |
| PROCS                           | External Storage Process Step                            | /SCWM/S_VAS_ACTIVITY_INT | PROCS                        |
| PROCTY                          | Warehouse Process Type                                   | /SCWM/S_VAS_ACTIVITY_INT | PROCTY                       |
| KIT_ACT                         | Kitting Activity                                         | /SCWM/S_VAS_ACTIVITY_INT | KIT_ACT                      |
| ACT_EFFORT_CODE                 | Effort for a VAS Activity                                | /SCWM/S_VAS_ACTIVITY_INT | ACT_EFFORT_CODE              |
| PLDURA                          | Planned Duration of a Workload Record                    | /SCWM/S_VAS_ACTIVITY_INT | PLDURA                       |
| UNIT_T                          | Time Unit                                                | /SCWM/S_VAS_ACTIVITY_INT | UNIT_T                       |
| ACT_STARTED_AT                  | ODM: Start Date/Time                                     | /SCWM/S_VAS_ACTIVITY_INT | ACT_STARTED_AT               |
| ACT_START_DATE                  | Start Date of Execution of VAS Activity                  | /SCWM/S_VAS_ACTIVITY_INT | ACT_START_DATE               |
| ACT_START_TIME                  | Start Time of Execution of VAS Activity                  | /SCWM/S_VAS_ACTIVITY_INT | ACT_START_TIME               |
| ACT_ENDED_AT                    | ODM: Finish Date/Time                                    | /SCWM/S_VAS_ACTIVITY_INT | ACT_ENDED_AT                 |
| ACT_END_DATE                    | End Date of Execution of VAS Activity                    | /SCWM/S_VAS_ACTIVITY_INT | ACT_END_DATE                 |
| ACT_END_TIME                    | End Time of Execution of VAS Activity                    | /SCWM/S_VAS_ACTIVITY_INT | ACT_END_TIME                 |
| ACT_PL_START_TIM                | ODM: Start Date/Time                                     | /SCWM/S_VAS_ACTIVITY_INT | ACT_PL_START_TIM             |
| ACT_PLAN_START_D                | Planned Start Date                                       | /SCWM/S_VAS_ACTIVITY_INT | ACT_PLAN_START_D             |
| ACT_PLAN_START_T                | Planned Start Time                                       | /SCWM/S_VAS_ACTIVITY_INT | ACT_PLAN_START_T             |
| ACT_PL_END_TIME                 | ODM: Finish Date/Time                                    | /SCWM/S_VAS_ACTIVITY_INT | ACT_PL_END_TIME              |
| ACT_PLAN_END_D                  | Planned End Date                                         | /SCWM/S_VAS_ACTIVITY_INT | ACT_PLAN_END_D               |
| ACT_PLAN_END_T                  | Planned End Time                                         | /SCWM/S_VAS_ACTIVITY_INT | ACT_PLAN_END_T               |
| ITM_SEQ                         | Sequence Number of VAS Activity or Item                  | /SCWM/S_VAS_ITM_INT      | ITM_SEQ                      |
| IT_MATNR                        | Product                                                  | /SCWM/S_VAS_ITM_INT      | IT_MATNR                     |
| IT_PLAN_QTY                     | Delivery Quantity                                        | /SCWM/S_VAS_ITM_INT      | IT_PLAN_QTY                  |
| IT_PLAN_QTY_UOM                 | Unit of Measure                                          | /SCWM/S_VAS_ITM_INT      | IT_PLAN_QTY_UOM              |
| IT_COMPLQTY                     | VAS: Completed Quantity                                  | /SCWM/S_VAS_ITM_INT      | IT_COMPLQTY                  |
| IT_RDOCCAT                      | Doc. Category for Doc. Reference and Doc.-Related Stocks | /SCWM/S_VAS_ITM_INT      | IT_RDOCCAT                   |
| IT_RDOCNO                       | Document Number of Document Reference                    | /SCWM/S_VAS_ITM_INT      | IT_RDOCNO                    |
| IT_RITMNO                       | Document Item of Document Reference                      | /SCWM/S_VAS_ITM_INT      | IT_RITMNO                    |
| AUX_SEQ                         | Sequence Number of VAS Activity or Item                  | /SCWM/S_VAS_AUXPROD_INT  | AUX_SEQ                      |
| AX_MATNR                        | Product                                                  | /SCWM/S_VAS_AUXPROD_INT  | AX_MATNR                     |
| AX_PLAN_QTY                     | VAS: Auxiliary Product Quantity to Be Posted             | /SCWM/S_VAS_AUXPROD_INT  | AX_PLAN_QTY                  |
| AX_POSTQTY                      | VAS Posted Quantity                                      | /SCWM/S_VAS_AUXPROD_INT  | AX_POSTQTY                   |
| AX_BASE_UNIT                    | Unit of Measure                                          | /SCWM/S_VAS_AUXPROD_INT  | AX_BASE_UNIT                 |
| HURELEVANT                      | Relevance for HU Creation                                | /SCWM/S_VAS_AUXPROD_INT  | HURELEVANT                   |
| AX_CHARG                        | Batch                                                    | /SCWM/S_VAS_AUXPROD_INT  | AX_CHARG                     |
| AX_CAT                          | Stock Type                                               | /SCWM/S_VAS_AUXPROD_INT  | AX_CAT                       |
| STOCK_USAGE                     | Stock Usage                                              | /SCWM/S_VAS_AUXPROD_INT  | STOCK_USAGE                  |
| STOCK_CNT                       | Counter for Stock Separation                             | /SCWM/S_VAS_AUXPROD_INT  | STOCK_CNT                    |
| STOCK_DOCCAT                    | Type Sales Order Stock or Project Stock                  | /SCWM/S_VAS_AUXPROD_INT  | STOCK_DOCCAT                 |
| STOCK_DOCNO                     | Number of the Sales Order or Project for Special Stock   | /SCWM/S_VAS_AUXPROD_INT  | STOCK_DOCNO                  |
| STOCK_ITMNO                     | Sales Order Item for Sales Order Stock                   | /SCWM/S_VAS_AUXPROD_INT  | STOCK_ITMNO                  |
| AX_OWNER_ROLE                   | Partner Role of Owner                                    | /SCWM/S_VAS_AUXPROD_INT  | AX_OWNER_ROLE                |
| AX_OWNER                        | Owner                                                    | /SCWM/S_VAS_AUXPROD_INT  | AX_OWNER                     |
| AX_ENTITLED_ROLE                | Partner Role of Party Entitled to Dispose                | /SCWM/S_VAS_AUXPROD_INT  | AX_ENTITLED_ROLE             |
| AX_ENTITLED                     | Party Entitled to Dispose                                | /SCWM/S_VAS_AUXPROD_INT  | AX_ENTITLED                  |

##### Extractor Logic

The fields in the table of origin for the extract structure largely consist of a 1:1 relation to data-based fields. For an explanation of how the other fields are instead determined by the extractor, see the table below.

| Fields in the Extract Structure | Field Determined by Extractor                                |
| ------------------------------- | ------------------------------------------------------------ |
| MANDT                           | This field is not filled.                                    |
| ROCANCEL                        | Determined by extractor: Indicator: Cancel Data Record.ROCANCEL is never set since value-added services cannot be deleted after completion. |