### Proof of Delivery

![DataSource Transactional Data](https://help.sap.com/doc/saphelp_ewm94/9.4/en-US/graphics/BICObjDataSourceTransactionalData.gif) DataSource Transactional Data: `0WM_POD`

 This DataSource provides you with proof-of-delivery data.

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

| Fields in the Extract Structure | Description of the Field in the Extract Structure         | Table of Origin | Field in the Table of Origin |
| ------------------------------- | --------------------------------------------------------- | --------------- | ---------------------------- |
| LGNUM                           | Warehouse Number/Warehouse Complex                        | /SCWM/POD       | LGNUM                        |
| DOCID                           | Document ID                                               | /SCWM/POD       | DOCID                        |
| ITEMID                          | Item ID                                                   | /SCWM/POD       | ITEMID                       |
| REASON                          | Reason for Difference in Proof of Delivery                | /SCWM/POD       | REASON                       |
| DOCNO                           | Outbound Delivery                                         | /SCWM/POD       | DOCNO                        |
| ITEMNO                          | Item Number                                               | /SCWM/POD       | ITEMNO                       |
| ERP_DOCNO                       | Reference Document Number                                 | /SCWM/POD       | ERP_DOCNO                    |
| ERP_ITEM_NO                     | Reference Item Number                                     | /SCWM/POD       | ERP_ITEM_NO                  |
| ERP_BSKEY                       | Key Name of Business System                               | /SCWM/POD       | ERP_BSKEY                    |
| DOCTYPE                         | Document Type                                             | /SCWM/POD       | DOCTYPE                      |
| ITEMTYPE                        | Item Type                                                 | /SCWM/POD       | ITEMTYPE                     |
| PDO_DOCID                       | Document ID                                               | /SCWM/POD       | PDO_DOCID                    |
| PDO_ITEMID                      | Item ID                                                   | /SCWM/POD       | PDO_ITEMID                   |
| PDO_DOCNO                       | Outbound Delivery Order                                   | /SCWM/POD       | PDO_DOCNO                    |
| PDO_ITEMNO                      | Reference to Outbound Delivery Order (Item)               | /SCWM/POD       | PDO_ITEMNO                   |
| PDO_ITEMID_PCKWT                | Proof of Delivery: Relevant Dlv. Item ID for Pick WTs     | /SCWM/POD       | PDO_ITEMID_PCKWT             |
| PDO_ITEMNO_PCKWT                | Proof of Delivery: Relevant Deliv. Item No. for Pick WTs  | /SCWM/POD       | PDO_ITEMNO_PCKWT             |
| PDO_ITEMID_WT                   | Proof of Delivery: Relevant Dlv. Item ID for Other WTs    | /SCWM/POD       | PDO_ITEMID_WT                |
| PDO_ITEMNO_WT                   | Proof of Delivery: Relevant Deliv. Item No. for Other WTs | /SCWM/POD       | PDO_ITEMNO_WT                |
| MTR                             | Means of Transport                                        | /SCWM/POD       | MTR                          |
| ROUTE                           | Route Name (Identification)                               | /SCWM/POD       | ROUTE                        |
| SHIP_TO_PARTY                   | Business Partner Number                                   | /SCWM/POD       | SHIP_TO_PARTY                |
| TSP                             | Business Partner Number                                   | /SCWM/POD       | TSP                          |
| SERVICE_LEVEL                   | Shipping Condition                                        | /SCWM/POD       | SERVICE_LEVEL                |
| GI_TSTMP                        | UTC Time Stamp in Short Form (YYYYMMDDhhmmss)             | /SCWM/POD       | GI_TSTMP                     |
| DCO_TSTMP                       | UTC Time Stamp in Short Form (YYYYMMDDhhmmss)             | /SCWM/POD       | DCO_TSTMP                    |
| POD_TSTMP                       | UTC Time Stamp in Short Form (YYYYMMDDhhmmss)             | /SCWM/POD       | POD_TSTMP                    |
| PODQTY_BUOM                     | POD Deviation in Quantity in Base Unit of Measure         | /SCWM/POD       | PODQTY_BUOM                  |
| BUOM                            | Base Unit of Measure                                      | /SCWM/POD       | BUOM                         |
| PODQTY_AUOM                     | POD Deviation in Quantity in Alternative Unit of Measure  | /SCWM/POD       | PODQTY_AUOM                  |
| AUOM                            | Alternative Unit of Measure for Stock Keeping Unit        | /SCWM/POD       | AUOM                         |
| DIFF_SIGN                       | Difference Type in Proof of Delivery                      | /SCWM/POD       | DIFF_SIGN                    |
| VALUE                           | Value of the Proof-of-Delivery Difference                 | /SCWM/POD       | VALUE                        |
| WAERS                           | Currency for a Warehouse                                  | /SCWM/POD       | WAERS                        |
| ENTITLED                        | Party Entitled to Dispose                                 | /SCWM/POD       | ENTITLED                     |
| MATID                           | Product                                                   | /SCWM/POD       | MATID                        |
| PICK_VLTYP                      | Source Storage Type for Picking                           | /SCWM/POD       | PICK_VLTYP                   |
| PICK_SOURCE_AREA                | Source Activity Area for Picking                          | /SCWM/POD       | PICK_SOURCE_AREA             |
| PICK_CONFRMD_BY                 | Picking Confirmed By                                      | /SCWM/POD       | PICK_CONFRMD_BY              |
| PICK_PROCESSOR                  | Picking Processor                                         | /SCWM/POD       | PICK_PROCESSOR               |
| PICK_PRSRC                      | Resource for Picking                                      | /SCWM/POD       | PICK_PRSRC                   |
| PICK_HUTYPE                     | Pick-HU Type                                              | /SCWM/POD       | PICK_HUTYPE                  |
| PICK_CONF_TSTMP                 | Confirmation Time for Picking                             | /SCWM/POD       | PICK_CONF_TSTMP              |
| PICK_WT_EXISTS                  | Proof of Delivery: Existing Whse Task Data for Picking    | /SCWM/POD       | PICK_WT_EXISTS               |
| PAC_IN_LGTYP                    | Storage Type of Inbound Packing Bin                       | /SCWM/POD       | PAC_IN_LGTYP                 |
| PAC_IN_LGPLA                    | Inbound Packing Bin                                       | /SCWM/POD       | PAC_IN_LGPLA                 |
| PAC_OUT_LGTYP                   | Storage Type of Outbound Packing Bin                      | /SCWM/POD       | PAC_OUT_LGTYP                |
| PAC_OUT_LGPLA                   | Outbound Packing Bin                                      | /SCWM/POD       | PAC_OUT_LGPLA                |
| PAC_WORKSTATION                 | Work Center (Packing)                                     | /SCWM/POD       | PAC_WORKSTATION              |
| PAC_CONFIRMED_BY                | Packing Confirmed By                                      | /SCWM/POD       | PAC_CONFIRMED_BY             |
| PAC_PROCESSOR                   | Packing Processor                                         | /SCWM/POD       | PAC_PROCESSOR                |
| PAC_PRSRC                       | Resource for Packing                                      | /SCWM/POD       | PAC_PRSRC                    |
| PAC_HUTYPE                      | Shipping HU Type                                          | /SCWM/POD       | PAC_HUTYPE                   |
| PAC_CONF_TSTMP                  | Confirmation Time for Packing                             | /SCWM/POD       | PAC_CONF_TSTMP               |
| PAC_WT_EXISTS                   | Proof of Delivery: Existing Whse Task Data for Packing    | /SCWM/POD       | PAC_WT_EXISTS                |
| STAG_LGTYP                      | Storage Type of Staging Area Bin                          | /SCWM/POD       | STAG_LGTYP                   |
| STAG_LGPLA                      | Staging Area Bin                                          | /SCWM/POD       | STAG_LGPLA                   |
| STAG_PRSRC                      | Resource for Staging                                      | /SCWM/POD       | STAG_PRSRC                   |
| STAG_CONFRMD_BY                 | Staging Confirmed By                                      | /SCWM/POD       | STAG_CONFRMD_BY              |
| STAG_PROCESSOR                  | Staging Processor                                         | /SCWM/POD       | STAG_PROCESSOR               |
| STAG_CONF_TSTMP                 | Confirmation Time for Staging                             | /SCWM/POD       | STAG_CONF_TSTMP              |
| STAG_WT_EXISTS                  | Proof of Delivery: Existing Whse Task Data for Staging    | /SCWM/POD       | STAG_WT_EXISTS               |
| LOAD_PRSRC                      | Resource for Loading                                      | /SCWM/POD       | LOAD_PRSRC                   |
| LOAD_CONFRMD_BY                 | Loading Confirmed By                                      | /SCWM/POD       | LOAD_CONFRMD_BY              |
| LOAD_PROCESSOR                  | Loading Processor                                         | /SCWM/POD       | LOAD_PROCESSOR               |
| LOAD_DOOR                       | Door                                                      | /SCWM/POD       | LOAD_DOOR                    |
| LOAD_CONF_TSTMP                 | Confirmation Time for Loading                             | /SCWM/POD       | LOAD_CONF_TSTMP              |
| LOAD_WT_EXISTS                  | Proof of Delivery: Existing Whse Task Data for Loading    | /SCWM/POD       | LOAD_WT_EXISTS               |
| CHG_TSTMP                       | Time of Change                                            | /SCWM/POD       | CHG_TSTMP                    |
| WHS_TZONE                       | Time Zone of Warehouse                                    | /SCMB/TOENTITY  | TZONE                        |