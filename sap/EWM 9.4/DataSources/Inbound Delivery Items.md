### Inbound Delivery Items

![DataSource Transactional Data](https://help.sap.com/doc/saphelp_ewm94/9.4/en-US/graphics/BICObjDataSourceTransactionalData.gif) DataSource Transactional Data: `0WM_DLVI_IN`

 This DataSource provides you with completed inbound delivery items.

#### Technical Data

| Application Component    | Warehouse Management (0WM)            |
| ------------------------ | ------------------------------------- |
| Available as of Release  | SAP EWM 900                           |
| Shipment                 | SAP NetWeaver 7.0 BI Content Add-On 7 |
| Content Versions         | EWM900                                |
| RemoteCube-Capable       | No                                    |
| Delta-Capable            | Yes, delta process AIE; generic delta |
| Extraction from Archives | No                                    |
| Verifiable               | No                                    |

#### Data Modeling

| Fields in the Extract Structure | Description of the Field in the Extract Structure | Table of Origin                   | Field in the Table of Origin    |
| ------------------------------- | ------------------------------------------------- | --------------------------------- | ------------------------------- |
| DOCID                           | Document ID                                       | /SCDL/DB_PROCH_I                  | DOCID                           |
| ITEMID                          | Item ID                                           | /SCDL/DB_PROCI_I                  | ITEMID                          |
| DOCNO                           | Document Number                                   | /SCDL/DB_PROCH_I                  | DOCNO                           |
| ITEMNO                          | Item Number                                       | /SCDL/DB_PROCI_I                  | ITEMNO                          |
| ITEMCAT                         | Item Category                                     | /SCDL/DB_PROCI_I                  | ITEMCAT                         |
| ITEMTYPE                        | Item Type                                         | /SCDL/DB_PROCI_I                  | ITEMTYPE                        |
| DOCTYPE                         | Document Type                                     | /SCDL/DB_PROCH_I                  | DOCTYPE                         |
| LGNUM                           | Warehouse Number/Warehouse Complex                | /SCDL/DB_PROCI_I                  | /SCWM/WHNO                      |
| INCO1                           | Incoterms (Part 1)                                | /SCDL/DB_PROCH_I                  | INCO1                           |
| INCO2                           | Incoterms (Part 2)                                | /SCDL/DB_PROCH_I                  | INCO2                           |
| PRODUCTID                       | Product ID                                        | /SCDL/DB_PROCI_I                  | PRODUCTID                       |
| PRODUCTNO                       | Product                                           | /SCDL/DB_PROCI_I                  | PRODUCTNO                       |
| GROSW                           | Weight of Delivery                                | /SCDL/DB_ADDMEAS                  | QTY                             |
| GWUOM                           | Unit of Measure                                   | /SCDL/DB_ADDMEAS                  | UOM                             |
| GROSV                           | Volume of Delivery                                | /SCDL/DB_ADDMEAS                  | QTY                             |
| GVUOM                           | Unit of Measure                                   | /SCDL/DB_ADDMEAS                  | UOM                             |
| ITEM_QTY                        | Quantity                                          | /SCDL/DB_ADDMEAS                  | QTY                             |
| ITEM_QTY_UOM                    | Unit of Measure                                   | /SCDL/DB_ADDMEAS                  | UOM                             |
| BATCHNO                         | Batch Number                                      | /SCDL/DB_PROCI_I                  | BATCHNO                         |
| ENTITLED                        | Party Entitled to Dispose                         | /SCDL/DB_PROCI_I                  | ENTITLED                        |
| STOCK_USAGE                     | Stock Usage                                       | /SCDL/DB_PROCI_I                  | STOCK_USAGE                     |
| OWNER                           | Owner                                             | /SCDL/DB_PROCI_I                  | STOCK_OWNER                     |
| CARRIERNO                       | Carrier                                           | /SCDL/DB_BPLOC                    | PARTYNO                         |
| TRANS_MODE                      | Transportation Mode                               | /SCDL/DB_TRANS                    | TRANS_MODE                      |
| MTR                             | Means of Transport                                | /SCDL/DB_TRANS                    | TRANSMEANS_TYPE                 |
| REFDOCNO_ERO                    | Reference Document Number                         | /SCDL/DB_REFDOC                   | REFDOCNO                        |
| REFITEMNO_ERO                   | Reference Item Number                             | /SCDL/DB_REFDOC                   | REFITEMNO                       |
| COO                             | Country of Origin                                 | /SCDL/DB_PROCI_I                  | OCOUNTRY                        |
| VFDAT                           | Best-Before Date/Shelf Life Expiration Date       | /SCDL/DB_PROCI_I                  | BESTBEFORE_DATE/SHELFEXPIR_DATE |
| PSA                             | Production Supply Area (PSA)                      | /SCDL/DB_PROCI_I                  | /SCWM/PSA                       |
| VALUE                           | Product Value                                     |                                   |                                 |
| WAERS                           | Currency Key                                      | /SCWM/T_VALUATE //SCWM/T_VAL_SPLT | WAERS                           |
| COMPL_TS                        | Completion Date/Time                              | /SCDL/DB_STATUS                   | TSTFR                           |
| ZERO_QTY_DLVI                   | Delivery Item with Zero Quantity                  | /SCDL/DB_PROCI_I                  | QTY                             |
| DLV_PROC_IND                    | Delivery Item Business Process for BW reporting   |                                   |                                 |
| NOT_RELEVANT                    | Delivery Item Relevance Flag                      |                                   |                                 |
| SERVICE_LEVEL                   | Shipping Condition                                | /SCDL/DB_PROCI_I                  | SERVICE_LEVEL                   |
| WHS_TZONE                       | Time Zone of Warehouse                            | /SCMB/TOENTITY                    | TZONE                           |
| GR_TS                           | Goods Receipt Date/Time                           | /SCDL/DB_DATE                     | TSTFR                           |
| PL_DLV_TS                       | Planned Delivery Date/Time                        | /SCDL/DB_DATE                     | TSTFR                           |
| SHIP_FR_NO                      | Ship-From                                         | /SCDL/DB_BPLOC                    | PARTYNO                         |
| PROD_DAT                        | Production Date                                   | /SCDL/DB_PROCI_I                  | PRODUCTION_DATE                 |
| Q_REL                           | Q-Relevance                                       |                                   |                                 |
| STOCK_TYPE                      | Stock Type                                        | /SCDL/DB_PROCI_I                  | STOCK_CATEGORY                  |

##### Extractor Logic

The fields in the table of origin for the extract structure largely consist of a 1:1 relation to data-based fields. For an explanation of how the other fields are instead determined by the extractor, see the table below.

| Fields in the Extract Structure | Field Determined by Extractor                                |
| ------------------------------- | ------------------------------------------------------------ |
| VALUE                           | Determined by extractor with ITEM_QTY and material price (/SCWM/T_VALUATE-VERPR/-STPRS, /SCWM/T_VAL_SPLT-VERPR/-STPRS) |
| DLV_PROC_IND                    | Determined by extractor in BAdI, Determination of Business Process for Delivery: /SCWM/EX_BW_BUSINESS_PRCSS_IND. This BAdI provides a fallback class default implementation that sets the business process for a specific delivery item.You can use this BAdI from Enhancement Spot /SCWM/ES_BW to implement your own logic for the field Business Process. |
| NOT_RELEVANT                    | Determined by extractor in BAdI, Setting of Not Relevant Indicator for Delivery Items: /SCWM/EX_BW_FILTER_DLVI. This BAdI provides a fallback class default implementation that sets the Not Relevant indicator to X when the Goods Receipt status is other than 9 (Posted).You can use this BAdI from Enhancement Spot /SCWM/ES_BW to implement your own logic for the field Not Relevant. |
| Q_REL                           | Determined by extractor: If document flow type Q01 exists, then the field is set to X. |