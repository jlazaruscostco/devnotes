### Stock

![DataSource Transactional Data](https://help.sap.com/doc/saphelp_ewm94/9.4/en-US/graphics/BICObjDataSourceTransactionalData.gif) DataSource Transactional Data: `0WM_STOCK`

 This DataSource provides you with stock data.

#### Technical Data

| Application Component    | Warehouse Management (0WM)            |
| ------------------------ | ------------------------------------- |
| Available as of Release  | SAP EWM 900                           |
| Shipment                 | SAP NetWeaver 7.0 BI Content Add-On 7 |
| Content Versions         | EWM900                                |
| RemoteCube-Capable       | No                                    |
| Delta-Capable            | No                                    |
| Extraction from Archives | No                                    |
| Verifiable               | No                                    |

#### Data Modeling

| Fields in the Extract Structure | Description of the Field in the Extract Structure        | Table of Origin                                              | Field in the Table of Origin |
| ------------------------------- | -------------------------------------------------------- | ------------------------------------------------------------ | ---------------------------- |
| GUID_PARENT                     | Parent GUID                                              | /SCWM/LOC_IW01                                               | GUID_LOC                     |
| GUID_STOCK                      | GUID Stock Item                                          | /SCWM/STOCK_IW01, /SCWM/STOCK_IW02, /SCWM/STOCK_IW03, /SCWM/STOCK_IW04 | GUID_STOCK                   |
| LGNUM                           | Warehouse Number/Warehouse Complex                       | /SCWM/LOC_IW01                                               | LGNUM                        |
| LGTYP                           | Storage Type                                             | /SCWM/LOC_IW01                                               | LGTYP                        |
| LGBER                           | Storage Section                                          | /SCWM/LAGP                                                   | LGBER                        |
| LGPLA                           | Storage Bin                                              | /SCWM/LOC_IW01                                               | LGPLA                        |
| HUIDENT                         | Handling Unit Identification                             | /SCWM/HU_IW01                                                | HUIDENT                      |
| HUIDENT_TOP                     | Handling Unit Identification                             | /SCWM/HU_IW01                                                | HUIDENT                      |
| MATID                           | Product                                                  | /SCWM/STOCK_IW01, /SCWM/STOCK_IW02, /SCWM/STOCK_IW03, /SCWM/STOCK_IW04 | MATID                        |
| MATNR                           | Product                                                  | /SAPAPO/MATKEY                                               | MATNR                        |
| CHARG                           | Batch                                                    | /SAPAPO/VERSKEY                                              | VERSION                      |
| CAT                             | Stock Type                                               | /SCWM/STOCK_IW01, /SCWM/STOCK_IW02, /SCWM/STOCK_IW03, /SCWM/STOCK_IW04 | CAT                          |
| ENTITLED                        | Party Entitled to Dispose                                | /SCWM/STOCK_IW01, /SCWM/STOCK_IW02, /SCWM/STOCK_IW03, /SCWM/STOCK_IW04 | ENTITLED                     |
| OWNER                           | Owner                                                    | /SCWM/STOCK_IW01, /SCWM/STOCK_IW02, /SCWM/STOCK_IW03, /SCWM/STOCK_IW04 | OWNER                        |
| STOCK_DOCCAT                    | Type: Sales Order Stock or Project Stock                 | /SCWM/STOCK_IW04                                             | STOCK_DOCCAT                 |
| STOCK_DOCNO                     | Number of the Sales Order or Project for Special Stock   | /SCWM/STOCK_IW04                                             | STOCK_DOCNO                  |
| STOCK_DOCNO_EXT                 | External Number of Sales Order/Project (Special Stock)   | /SCWM/ERP_PSP                                                | STOCK_DOCNO_EXT              |
| STOCK_ITMNO                     | Sales Order Item for Sales Order Stock                   | /SCWM/STOCK_IW04                                             | STOCK_ITMNO                  |
| STOCK_USAGE                     | Stock Usage                                              | /SCWM/STOCK_IW01, /SCWM/STOCK_IW02, /SCWM/STOCK_IW03, /SCWM/STOCK_IW04 | STOCK_USAGE                  |
| STREF_DOCCAT                    | Doc. Category for Doc. Reference and Doc.-Related Stocks | /SCWM/STOCK_IW03                                             | DOCCAT                       |
| WDATU                           | Goods Receipt Date                                       | /SCWM/QUAN                                                   | WDATU                        |
| VFDAT                           | Best-Before Date / Shelf Life Expiration Date            | /SCWM/QUAN                                                   | VFDAT                        |
| COO                             | Country of Origin                                        | /SCWM/QUAN                                                   | COO                          |
| IDPLATE                         | Identification Number of Stock                           | /SCWM/QUAN                                                   | IDPLATE                      |
| QDOCCAT                         | Doc. Category for Doc. Reference and Doc.-Related Stocks | /SCWM/QUAN                                                   | QDOCCAT                      |
| QDOCNO                          | Document Number for Stock Reference                      | /SCDL/DB_PROCH_I, /SCDL/DB_PROCH_O                           | DOCNO                        |
| QITEMNO                         | Item Number of Stock Reference                           | /SCDL/DB_PROCI_I, /SCDL/DB_PROCI_O                           | ITEMNO                       |
| INSPTYP                         | Inspection Type                                          | /SCWM/QUAN                                                   | INSPTYP                      |
| INSPDOCNO                       | QIE Entity: External Identification                      | QIE_INSP_DOC                                                 | INSP_DOC_NUMBER              |
| WEIGHT                          | Loading/Net Weight                                       | /SCWM/QUAN                                                   | WEIGHT                       |
| UNIT_W                          | Weight Unit                                              | /SCWM/QUAN                                                   | UNIT_W                       |
| VOLUM                           | Loading/Net Volume                                       | /SCWM/QUAN                                                   | VOLUM                        |
| UNIT_V                          | Volume Unit                                              | /SCWM/QUAN                                                   | UNIT_V                       |
| CAPA                            | Capacity Consumption                                     | /SCWM/QUAN                                                   | CAPA                         |
| QUAN                            | Quantity                                                 | /LIME/NQUAN                                                  | QUAN                         |
| MEINS                           | Base Unit of Measure                                     | /LIME/NQUAN                                                  | UNIT                         |
| QUANA                           | Packed Quantity in Alternative Unit of Measure           |                                                              |                              |
| ALTME                           | Alternative Unit of Measure for Stock-keeping Unit       | /SCWM/QUAN                                                   | ALTME                        |
| CWQUAN                          | Actual Valuation Quantity (for UI)                       | /LIME/NQUAN                                                  | QUAN                         |
| CWUNIT                          | Unit for Valuation Quantity                              | /LIME/NQUAN                                                  | UNIT                         |
| VALUE                           | Product Value                                            |                                                              |                              |
| WAERS                           | Currency Key                                             | /SCWM/T_VALUATE, /SCWM/T_VAL_SPLT                            | WAERS                        |
| DSTGRP                          | Consolidation Group                                      | /SCWM/QUAN                                                   | DSTGRP                       |
| PSA                             | Production Supply Area (PSA)                             | /SCWM/TPSASTAGE                                              | PSA                          |
| LPTYP                           | Storage Bin Type                                         | /SCWM/LAGP                                                   | LPTYP                        |
| ST_ROLE                         | Storage Type Role                                        | /SCWM/T331                                                   | ST_ROLE                      |
| AISLE                           | Aisle in a Storage Bin                                   | /SCWM/LAGP                                                   | AISLE                        |
| STACK                           | Stack in a Storage Bin                                   | /SCWM/LAGP                                                   | STACK                        |
| LVL_V                           | Level in a Storage Bin                                   | /SCWM/LAGP                                                   | LVL_L                        |
| LETYP                           | Handling Unit Type                                       | /SCWM/HUHDR                                                  | LETYP                        |
| LETYP_TOP                       | Top Handling Unit Type                                   | /SCWM/HUHDR                                                  | LETYP                        |
| MATKL                           | Material Group                                           | /SAPAPO/MATKEY                                               | MATKL                        |
| STOKEY1                         | Hazard Rating                                            | HSMC_014                                                     | STOKEY                       |
| STOKEY2                         | Hazard Rating                                            | HSMC_014                                                     | STOKEY                       |
| EXTRACT_DATE                    | Extraction Date                                          |                                                              |                              |
| EXTRACT_TIME                    | Extraction Time                                          |                                                              |                              |

##### Extractor Logic

The fields in the table of origin for the extract structure largely consist of a 1:1 relation to data-based fields. For an explanation of how the other fields are instead determined by the extractor, see the table below.

| Fields in the Extract Structure | Field Determined by Extractor                                |
| ------------------------------- | ------------------------------------------------------------ |
| QUANA                           | Determined by extractor with QUAN,MEINS and ALTME.           |
| VALUE                           | Determined by extractor with QUAN and material price /SCWM/T_VALUATE-VERPR/-STPRS, /SCWM/T_VAL_SPLT-VERPR/-STPRS. |
| EXTRACT_DATE                    | Determined by extractor, given in warehouse time zone.       |
| EXTRACT_TIME                    | Determined by extractor, given in warehouse time zone.       |