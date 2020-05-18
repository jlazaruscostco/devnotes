### Warehouse Tasks

![DataSource Transactional Data](https://help.sap.com/doc/saphelp_ewm94/9.4/en-US/graphics/BICObjDataSourceTransactionalData.gif) DataSource Transactional Data: `0WM_WT_WO`

 This DataSource provides you with confirmed warehouse tasks. It does not provide you with warehouse documents of goods movements or posting changes.

![Note](https://help.sap.com/doc/saphelp_ewm94/9.4/en-US/graphics/note.gif) Note

For this DataSource, the number of transferred data records per package may vary greatly between the individual packages.

The warehouse tasks can only be extracted once the relevant warehouse order has been confirmed.

#### Technical Data

| Application Component    | Warehouse Management (0WM)              |
| ------------------------ | --------------------------------------- |
| Available as of Release  | SAP SCM 5.1 and SAP EWM 5.1             |
| Shipment                 | SAP NetWeaver 2004s BI Content Add-On 3 |
| Content Versions         | EWM900                                  |
| RemoteCube-Capable       | No                                      |
| Delta-Capable            | Yes, delta process AIE; generic delta   |
| Extraction from Archives | No                                      |
| Verifiable               | No                                      |

#### Data Modeling

| Fields in the Extract Structure | Description of the Field in the Extract Structure        | Table of Origin | Field in the Table of Origin |
| ------------------------------- | -------------------------------------------------------- | --------------- | ---------------------------- |
| MANDT                           | Client                                                   | /SCWM/ORDIM_C   | MANDT                        |
| LGNUM                           | Warehouse Number/Warehouse Complex                       | /SCWM/ORDIM_C   | LGNUM                        |
| TANUM                           | Warehouse Task                                           | /SCWM/ORDIM_C   | TANUM                        |
| TAPOS                           | Warehouse Task Item                                      | /SCWM/ORDIM_C   | TAPOS                        |
| FLGHUTO                         | Handling Unit Warehouse Task                             | /SCWM/ORDIM_C   | FLGHUTO                      |
| PROCTY                          | Warehouse Process Type                                   | /SCWM/ORDIM_C   | PROCTY                       |
| TRART                           | Warehouse Process Category                               | /SCWM/ORDIM_C   | TRART                        |
| PRCES                           | Storage Process                                          | /SCWM/ORDIM_C   | PRCES                        |
| PROCS                           | External Storage Process Step                            | /SCWM/ORDIM_C   | PROCS                        |
| TOSTAT                          | Warehouse Task Status                                    | /SCWM/ORDIM_C   | TOSTAT                       |
| CREATED_BY                      | Created By                                               | /SCWM/ORDIM_C   | CREATED_BY                   |
| CREATED_AT                      | Created at                                               | /SCWM/ORDIM_C   | CREATED_AT                   |
| CREATED_DATE                    | Created On                                               |                 |                              |
| CREATED_TIME                    | Created At                                               |                 |                              |
| REASON                          | Reason for Movements in the Warehouse                    | /SCWM/ORDIM_C   | REASON                       |
| PRIORITY                        | Priority                                                 | /SCWM/ORDIM_C   | PRIORITY                     |
| MATNR                           | Product                                                  | /SCWM/ORDIM_C   | MATNR                        |
| CHARG                           | Batch Number                                             | /SCWM/ORDIM_C   | CHARG                        |
| CAT                             | Stock Type                                               | /SCWM/ORDIM_C   | CAT                          |
| STOCK_DOCCAT                    | Type Sales Order Stock or Project Stock                  | /SCWM/ORDIM_C   | STOCK_DOCCAT                 |
| STOCK_DOCNO                     | Number of the Sales Order or Project for Special Stock   | /SCWM/ORDIM_C   | STOCK_DOCNO                  |
| STOCK_ITMNO                     | Sales Order Item for Sales Order Stock                   | /SCWM/ORDIM_C   | STOCK_ITMNO                  |
| DOCCAT                          | Doc. Category for Doc. Reference and Doc.-Related Stocks | /SCWM/ORDIM_C   | DOCCAT                       |
| STOCK_USAGE                     | Stock Usage                                              | /SCWM/ORDIM_C   | STOCK_USAGE                  |
| OWNER                           | Owner                                                    | /SCWM/ORDIM_C   | OWNER                        |
| ENTITLED                        | Party Entitled to Dispose                                | /SCWM/ORDIM_C   | ENTITLED                     |
| MEINS                           | Base unit of measure                                     | /SCWM/ORDIM_C   | MEINS                        |
| ALTME                           | Alternative Unit of Measure for Stockkeeping Unit        | /SCWM/ORDIM_C   | ALTME                        |
| VSOLM                           | Target Quantity in Base Unit of Measure                  | /SCWM/ORDIM_C   | VSOLM                        |
| VSOLA                           | Target Quantity in Alternative Unit of Measure           | /SCWM/ORDIM_C   | VSOLA                        |
| KQUAN                           | Retention Quantity                                       | /SCWM/ORDIM_C   | KQUAN                        |
| LETYP                           | Handling Unit Type                                       | /SCWM/ORDIM_C   | LETYP                        |
| WEIGHT                          | Loading/Net Weight                                       | /SCWM/ORDIM_C   | WEIGHT                       |
| UNIT_W                          | Weight Unit                                              | /SCWM/ORDIM_C   | UNIT_W                       |
| VOLUM                           | Loading/Net Volume                                       | /SCWM/ORDIM_C   | VOLUM                        |
| UNIT_V                          | Volume Unit                                              | /SCWM/ORDIM_C   | UNIT_V                       |
| CAPA                            | Capacity Consumption                                     | /SCWM/ORDIM_C   | CAPA                         |
| VFDAT_TS                        | Shelf Life Expiration Date or Best-Before Date           |                 |                              |
| VFDAT                           | Shelf Life Expiration Date                               | /SCWM/ORDIM_C   | VFDAT                        |
| WDATU                           | Date of Goods Receipt                                    | /SCWM/ORDIM_C   | WDATU                        |
| WDATU_DATE                      | Date of Goods Receipt                                    |                 |                              |
| WDATU_TIME                      | Goods Receipt Time                                       |                 |                              |
| COO                             | Country of Origin                                        | /SCWM/ORDIM_C   | COO                          |
| HAZMAT                          | Hazardous Substance                                      | /SCWM/ORDIM_C   | HAZMAT                       |
| INSPTYP                         | Inspection Type                                          | /SCWM/ORDIM_C   | INSPTYP                      |
| INSPDOCNO                       | QIE Entity: External Identification                      | /SCWM/ORDIM_C   | INSPDOCNO                    |
| IDPLATE                         | Identification Number of Stock                           | /SCWM/ORDIM_C   | IDPLATE                      |
| VLTYP                           | Source Storage Type                                      | /SCWM/ORDIM_C   | VLTYP                        |
| VLBER                           | Source Storage Section                                   | /SCWM/ORDIM_C   | VLBER                        |
| VLPLA                           | Source Storage Bin                                       | /SCWM/ORDIM_C   | VLPLA                        |
| VPTYP                           | Source Bin Type                                          | /SCWM/LAGP      | LPTYP                        |
| SRSRC                           | Resource (Means of Transportation or User)               | /SCWM/ORDIM_C   | SRSRC                        |
| STU_NUM                         | Source Transportation Unit (Internal)                    | /SCWM/ORDIM_C   | STU_NUM                      |
| VLENR                           | Source Handling Unit                                     | /SCWM/ORDIM_C   | VLENR                        |
| NLTYP                           | Destination Storage Type                                 | /SCWM/ORDIM_C   | NLTYP                        |
| NLBER                           | Destination Storage Section                              | /SCWM/ORDIM_C   | NLBER                        |
| NLPLA                           | Destination Storage Bin                                  | /SCWM/ORDIM_C   | NLPLA                        |
| NPTYP                           | Destination Bin Type                                     | /SCWM/LAGP      | LPTYP                        |
| DRSRC                           | Resource (Means of Transportation or User)               | /SCWM/ORDIM_C   | DRSRC                        |
| DTU_NUM                         | Destination Transportation Unit (Internal)               | /SCWM/ORDIM_C   | DTU_NUM                      |
| NLENR                           | Destination Handling Unit                                | /SCWM/ORDIM_C   | NLENR                        |
| KZSUB                           | Indicator: Pass on Warehouse Task to Subsystem           | /SCWM/ORDIM_C   | KZSUB                        |
| SOLPO                           | Planned Proc. Time in Warehouse Task                     | /SCWM/ORDIM_C   | SOLPO                        |
| ZEIEI                           | Time Unit for Processing Time Determination              | /SCWM/ORDIM_C   | ZEIEI                        |
| VAS                             | Indicator: WT with Reference to a VAS                    | /SCWM/ORDIM_C   | VAS                          |
| RDOCCAT                         | Doc. Category for Doc. Reference and Doc.-Related Stocks | /SCWM/ORDIM_C   | RDOCCAT                      |
| RDOCNO                          | Document Number of Document Reference                    | /SCWM/ORDIM_C   | RDOCNO                       |
| RITMNO                          | Document Item of Document Reference                      | /SCWM/ORDIM_C   | RITMNO                       |
| WAVE                            | Wave                                                     | /SCWM/ORDIM_C   | WAVE                         |
| WAVE_ITEM                       | Wave Item                                                | /SCWM/ORDIM_C   | WAVE_ITEM                    |
| QDOCCAT                         | Doc. Category for Doc. Reference and Doc.-Related Stocks | /SCWM/ORDIM_C   | QDOCCAT                      |
| QDOCNO                          | Document Number for Stock Reference                      | /SCWM/ORDIM_C   | QDOCNO                       |
| QITMNO                          | Item Number of Stock Reference                           | /SCWM/ORDIM_C   | QITMNO                       |
| QIDPLATE                        | Identification Number of Stock                           | /SCWM/ORDIM_C   | QIDPLATE                     |
| CONFIRMED_BY                    | Confirmed by                                             | /SCWM/ORDIM_C   | CONFIRMED_BY                 |
| CONFIRMED_AT                    | Time of Confirmation                                     | /SCWM/ORDIM_C   | CONFIRMED_AT                 |
| CONFIRMED_DATE                  | Confirmation Date                                        |                 |                              |
| CONFIRMED_TIME                  | Confirmation Time                                        |                 |                              |
| EXCCODE                         | Exception Code                                           | /SCWM/ORDIM_C   | EXCCODE                      |
| BUSCON                          | Business Context                                         | /SCWM/ORDIM_C   | BUSCON                       |
| EXEC_STEP                       | Execution Step in Business Context                       | /SCWM/ORDIM_C   | EXEC_STEP                    |
| STARTED_AT                      | Start Time                                               | /SCWM/ORDIM_C   | STARTED_AT                   |
| STARTED_DATE                    | Start Date                                               |                 |                              |
| STARTED_TIME                    | Start Time                                               |                 |                              |
| NISTM                           | Actual Quantity in Base Unit of Measure                  | /SCWM/ORDIM_C   | NISTM                        |
| NISTA                           | Actual Quantity in Alternative Unit of Measure           | /SCWM/ORDIM_C   | NISTA                        |
| PLACE_INV                       | Inventory on Putaway Performed                           | /SCWM/ORDIM_C   | PLACE_INV                    |
| LOWCHK_INV                      | Low Stock Check Executed                                 | /SCWM/ORDIM_C   | LOWCHK_INV                   |
| HUENT                           | Indicator: Handling unit will be withdrawn completely    | /SCWM/ORDIM_C   | HUENT                        |
| SLGNUM_VIEW                     | Warehouse Number View for Global Stocks                  | /SCWM/ORDIM_C   | SLGNUM_VIEW                  |
| DLGNUM_VIEW                     | Warehouse Number View for Global Stocks                  | /SCWM/ORDIM_C   | DLGNUM_VIEW                  |
| DMENG                           | Quantity of Difference Posting in Stock Keeping Unit     | /SCWM/ORDIM_C   | DMENG                        |
| DMENA                           | Difference quantity in alternate unit of measure         | /SCWM/ORDIM_C   | DMENA                        |
| WHO                             | Warehouse Order Number                                   | /SCWM/ORDIM_C   | WHO                          |
| AAREA                           | Activity Area                                            | /SCWM/ORDIM_C   | AAREA                        |
| QUEUE                           | Queue                                                    | /SCWM/ORDIM_C   | QUEUE                        |
| ROCANCEL                        | Indicator: Cancel Data Record                            |                 |                              |
| CWQUAN                          | Valuation Quantity                                       | /SCWM/ORDIM_C   | CWQUAN                       |
| CWQUAN_DIFF                     | Valuation Quantity                                       | /SCWM/ORDIM_C   | CWQUAN_DIFF                  |
| CWUNIT                          | Unit for Valuation Quantity                              | /SCWM/ORDIM_C   | CWUNIT                       |
| PROCESS                         | Storage Process Step                                     |                 |                              |
| COUNTER                         | Index of Internal Tables                                 | /SCWM/ORDIM_C   | COUNTER                      |
| VLPLA_MAIN                      | Source Storage Bin                                       |                 |                              |
| NLPLA_MAIN                      | Destination Storage Bin                                  |                 |                              |
| PROCESSOR                       | Processor                                                | /SCWM/ORDIM_C   | PROCESSOR                    |
| FULL_PALLET                     | Indicator for Full Pallet Withdrawal                     |                 |                              |
| MATKL                           | Material Group                                           | /SAPAPO/MATKEY  | MATKL                        |
| VST_ROLE                        | Source Storage Type Role                                 | /SCWM/T331      | ST_ROLE                      |
| NST_ROLE                        | Target Storage Type Role                                 | /SCWM/T331      | ST_ROLE                      |

##### Extractor Logic

The fields in the table of origin for the extract structure largely consist of a 1:1 relation to data-based fields. For an explanation of how the other fields are instead determined by the extractor, see the table below.

| Fields in the Extract Structure | Field Determined by Extractor                                |
| ------------------------------- | ------------------------------------------------------------ |
| CREATED_DATE                    | Determined by extractor, given in warehouse time zone.       |
| CREATED_TIME                    | Determined by extractor, given in warehouse time zone.       |
| VFDAT_TS                        | Determined by extractor.                                     |
| WDATU_DATE                      | Determined by extractor, given in warehouse time zone.       |
| WDATU_TIME                      | Determined by extractor, given in warehouse time zone.       |
| CONFIRMED_DATE                  | Determined by extractor, given in warehouse time zone.       |
| CONFIRMED_TIME                  | Determined by extractor, given in warehouse time zone.       |
| STARTED_DATE                    | Determined by extractor, given in warehouse time zone.       |
| STARTED_TIME                    | Determined by extractor, given in warehouse time zone.       |
| ROCANCEL                        | Determined by extractor: Indicator: Cancel Data Record.ROCANCEL is never set since warehouse tasks cannot be deleted after confirmation or cancellation. |
| PROCESS                         | Determined by the extractor for the warehouse task, which executes mapping for the PROCESS field as indicated in the table below. |
| VLPLA_MAIN                      | Determined by extractor for source bin.                      |
| NLPLA_MAIN                      | Determined by extractor for destination bin.                 |
| FULL_PALLET                     | Determined by extractor in BAdI, Indicator Setting for Full Pallet Withdrawal: /SCWM/EX_BW_FILTER_FULL_PALLET. This BAdI provides a fallback class default implementation that sets the Indicator for Full Pallet Withdrawal to X when either the indicator Handling Unit Will Be Withdrawn Completely is set or when Alternative Unit of Measure is PAL.You can use this BAdI from Enhancement Spot /SCWM/ES_BW to implement your own logic for Indicator for Full Pallet Withdrawal. |

| Process                    | Internal Process Step / Warehouse Process Catagory | Value |
| -------------------------- | -------------------------------------------------- | ----- |
| Cross-Docking              | CD                                                 | CD    |
| Count                      | CNT                                                | CNT   |
| Correction for EWL         | CORR                                               | CORR  |
| Indirect Labor             | INDL                                               | INDL  |
| Physical Inventory         | INVE                                               | INVE  |
| Load                       | LOAD                                               | LOAD  |
| Movement w/o Stor. Control | NSCT                                               | NSCT  |
| Pack                       | PAC                                                | PAC   |
| Remove from Stock          | PICK                                               | PICK  |
| Put Away                   | PUT                                                | PUT   |
| Quality Inspection         | QIS                                                | QIS   |
| Deconsolidate              | SPR                                                | SPR   |
| Stage                      | STAG                                               | STAG  |
| Unload                     | UNLO                                               | UNLO  |
| Value-Added Service        | VAS                                                | VAS   |
| Posting Changes            | 7                                                  | POCH  |