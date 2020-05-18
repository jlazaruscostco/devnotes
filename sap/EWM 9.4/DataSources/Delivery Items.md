### Delivery Items

![DataSource Transactional Data](https://help.sap.com/doc/saphelp_ewm94/9.4/en-US/graphics/BICObjDataSourceTransactionalData.gif) DataSource Transactional Data: `0WM_DLVI`

 This DataSource provides you with completed inbound and outbound delivery items.

![Note](https://help.sap.com/doc/saphelp_ewm94/9.4/en-US/graphics/note.gif) Note

The cancellation of a completed outbound delivery order (for example, the cancellation of a goods issue) is also extracted.

#### Technical Data

| Application Component    | Warehouse Management (0WM)              |
| ------------------------ | --------------------------------------- |
| Available as of Release  | SAP SCM 5.1 and SAP EWM 5.1             |
| Shipment                 | SAP NewWeaver 2004s BI Content Add-On 3 |
| Content Versions         | EWM900                                  |
| RemoteCube-Capable       | No                                      |
| Delta-Capable            | Yes, delta process AIMD                 |
| Extraction from Archives | No                                      |
| Verifiable               | No                                      |

#### Data Modeling

| Fields in the Extract Structure | Description of the Field in the Extract Structure | Table of Origin                   | Field in the Table of Origin |
| ------------------------------- | ------------------------------------------------- | --------------------------------- | ---------------------------- |
| DOCID                           | Document ID                                       | /SCDL/DB_PROCH_I;/SCDL/DB_DLVI_O  | DOCID                        |
| ITEMID                          | Item ID                                           | /SCDL/DB_PROCI_I;/SCDL/DB_DLVI_O  | ITEMID                       |
| DOCNO                           | Document Number                                   | /SCDL/DB_PROCH_I;/SCDL/DB_DLVH_O  | DOCNO                        |
| ITEMNO                          | Item Number                                       | /SCDL/DB_PROCI_I;/SCDL/DB_DLVI_O  | ITEMNO                       |
| DOCTYPE                         | Document Type                                     | /SCDL/DB_PROCH_I;/SCDL/DB_DLVH_O  | DOCTYPE                      |
| DOCCAT                          | Document Category                                 | /SCDL/DB_PROCH_I;/SCDL/DB_DLVI_O  | DOCCAT                       |
| ITEMTYPE                        | Item Type                                         | /SCDL/DB_PROCI_I;/SCDL/DB_DLVI_O  | ITEMTYPE                     |
| ITEMCAT                         | Item Category                                     | /SCDL/DB_PROCI_I;/SCDL/DB_DLVI_O  | ITEMCAT                      |
| INCO1                           | Incoterms Part 1                                  | /SCDL/DB_PROCH_I;/SCDL/DB_DLVH_O  | INCO1                        |
| INCO2                           | Incoterms Part 2                                  | /SCDL/DB_PROCH_I;/SCDL/DB_DLVH_O  | INCO2                        |
| PRODUCTID                       | Product ID                                        | /SCDL/DB_PROCI_I;/SCDL/DB_PROCI_O | PRODUCTID                    |
| PRODUCTNO                       | Product                                           | /SCDL/DB_PROCI_I;/SCDL/DB_PROCI_O | PRODUCTNO                    |
| PRODUCTENT                      | Product Entered                                   | /SCDL/DB_PROCI_I;/SCDL/DB_PROCI_O | PRODUCTENT                   |
| CREUSER                         | Created By                                        | /SCDL/DB_PROCH_I;/SCDL/DB_PROCH_O | CREUSER                      |
| CRETST                          | Created On                                        | /SCDL/DB_PROCH_I;/SCDL/DB_PROCH_O | CRETST                       |
| PRIORITY                        | Delivery Priority                                 | /SCDL/DB_PROCI_I;/SCDL/DB_PROCI_O | PRIORITY                     |
| SERVICELEVEL                    | Shipping Condition                                | /SCDL/DB_PROCI_I;/SCDL/DB_PROCI_O | SERVICE_LEVEL_CODE           |
| BATCHNO                         | Batch Number                                      | /SCDL/DB_PROCI_I;/SCDL/DB_PROCI_O | BATCHNO                      |
| STOCK_USAGE                     | Stock Usage                                       | /SCDL/DB_PROCI_I;/SCDL/DB_PROCI_O | STOCK_USAGE                  |
| STOCK_CATEGORY                  | Stock Type                                        | /SCDL/DB_PROCI_I;/SCDL/DB_PROCI_O | STOCK_CATEGORY               |
| STOCK_OWNER                     | Owner                                             | /SCDL/DB_PROCI_I;/SCDL/DB_PROCI_O | STOCK_OWNER                  |
| STOCK_OWNER_ROLE                | Owner Role                                        | /SCDL/DB_PROCI_I;/SCDL/DB_PROCI_O | STOCK_OWNER_ROLE             |
| ENTITLED                        | Party Entitled to Dispose                         | /SCDL/DB_PROCI_I;/SCDL/DB_PROCI_O | ENTITLED                     |
| ENTITLED_ROLE                   | Partner Role of Party Entitled to Dispose         | /SCDL/DB_PROCI_I;/SCDL/DB_PROCI_O | ENTITLED_ROLE                |
| LGNUM                           | Warehouse Number/Warehouse Complex                | /SCDL/DB_PROCI_I;/SCDL/DB_PROCI_O | /SCWM/WHNO                   |
| VENDORID                        | Partner ID                                        | /SCDL/DB_BPLOC                    | PARTYID                      |
| VENDORNO                        | Business Partner Number                           | /SCDL/DB_BPLOC                    | PARTYNO                      |
| BUYERID                         | Partner ID                                        | /SCDL/DB_BPLOC                    | PARTYID                      |
| BUYERNO                         | Business Partner Number                           | /SCDL/DB_BPLOC                    | PARTYNO                      |
| CARRIERID                       | Partner ID                                        | /SCDL/DB_BPLOC                    | PARTYID                      |
| CARRIERNO                       | Business Partner Number                           | /SCDL/DB_BPLOC                    | PARTYNO                      |
| WHID                            | Location ID                                       | /SCDL/DB_BPLOC                    | LOCATIONID                   |
| WHNO                            | Location Number                                   | /SCDL/DB_BPLOC                    | LOCATIONNO                   |
| SHIP_FROM_ID                    | Partner ID                                        | /SCDL/DB_BPLOC                    | PARTYID                      |
| SHIP_FROM_NO                    | Business Partner Number                           | /SCDL/DB_BPLOC                    | PARTYNO                      |
| SHIP_TO_ID                      | Partner ID                                        | /SCDL/DB_BPLOC                    | PARTYID                      |
| SHIP_TO_NO                      | Business Partner Number                           | /SCDL/DB_BPLOC                    | PARTYNO                      |
| PARTYID                         | Partner ID                                        | /SCDL/DB_BPLOC                    | PARTYNO                      |
| GROSW                           | Weight of Delivery                                | /SCDL/DB_ADDMEAS                  | QTY                          |
| GWUOM                           | Unit of Measure                                   | /SCDL/DB_ADDMEAS                  | UOM                          |
| NETW                            | Weight of Delivery                                | /SCDL/DB_ADDMEAS                  | QTY                          |
| NWUOM                           | Unit of Measure                                   | /SCDL/DB_ADDMEAS                  | UOM                          |
| NETV                            | Quantity                                          | /SCDL/DB_ADDMEAS                  | QTY                          |
| NVUOM                           | Unit of Measure                                   | /SCDL/DB_ADDMEAS                  | UOM                          |
| GROSV                           | Quantity                                          | /SCDL/DB_ADDMEAS                  | QTY                          |
| GVUOM                           | Unit of Measure                                   | /SCDL/DB_ADDMEAS                  | UOM                          |
| GRQTY                           | Quantity                                          | /SCDL/DB_ADDMEAS                  | QTY                          |
| GRUOM                           | Unit of Measure                                   | /SCDL/DB_ADDMEAS                  | UOM                          |
| PUTAQTY                         | Quantity                                          | /SCDL/DB_ADDMEAS                  | QTY                          |
| PUTAUOM                         | Unit of Measure                                   | /SCDL/DB_ADDMEAS                  | UOM                          |
| UNLQTY                          | Quantity                                          | /SCDL/DB_ADDMEAS                  | QTY                          |
| UNLUOM                          | Unit of Measure                                   | /SCDL/DB_ADDMEAS                  | UOM                          |
| GIQTY                           | Quantity                                          | /SCDL/DB_ADDMEAS                  | QTY                          |
| GIUOM                           | Unit of Measure                                   | /SCDL/DB_ADDMEAS                  | UOM                          |
| PICKQTY                         | Quantity                                          | /SCDL/DB_ADDMEAS                  | QTY                          |
| PICKUOM                         | Unit of Measure                                   | /SCDL/DB_ADDMEAS                  | UOM                          |
| LOADQTY                         | Quantity                                          | /SCDL/DB_ADDMEAS                  | QTY                          |
| LOADUOM                         | Unit of Measure                                   | /SCDL/DB_ADDMEAS                  | UOM                          |
| OPLANQTY                        | Quantity                                          | /SCDL/DB_ADDMEAS                  | QTY                          |
| OPLANUOM                        | Unit of Measure                                   | /SCDL/DB_ADDMEAS                  | UOM                          |
| VALQTY                          | Quantity                                          | /SCDL/DB_ADDMEAS                  | VALQTY                       |
| VALUOM                          | Unit of Measure                                   | /SCDL/DB_ADDMEAS                  | VALUOM                       |
| REQQTY                          | Quantity                                          |                                   |                              |
| REQUOM                          | Unit of Measure                                   | /SCDL/DB_ADDMEAS                  | REQUOM                       |
| GRSTZ                           | Time Zone                                         | /SCDL/DB_DATE                     | TZONE                        |
| GRSTSLB                         | Start Date/Time                                   | /SCDL/DB_DATE                     | TSTFR                        |
| GRSTSHB                         | Finish Date/Time                                  | /SCDL/DB_DATE                     | TSTTO                        |
| GRETZ                           | Time Zone                                         | /SCDL/DB_DATE                     | TZONE                        |
| GRETSLB                         | Start Date/Time                                   | /SCDL/DB_DATE                     | TSTFR                        |
| GRETSHB                         | Finish Date/Time                                  | /SCDL/DB_DATE                     | TSTTO                        |
| GISTZ                           | Time Zone                                         | /SCDL/DB_DATE                     | TZONE                        |
| GISTSLB                         | Start Date/Time                                   | /SCDL/DB_DATE                     | TSTFR                        |
| GISTSHB                         | Finish Date/Time                                  | /SCDL/DB_DATE                     | TSTTO                        |
| GIETZ                           | Time Zone                                         | /SCDL/DB_DATE                     | TZONE                        |
| GIETSLB                         | Start Date/Time                                   | /SCDL/DB_DATE                     | TSTFR                        |
| GIETSHB                         | Finish Date/Time                                  | /SCDL/DB_DATE                     | TSTTO                        |
| UNLSTZ                          | Time Zone                                         | /SCDL/DB_DATE                     | TZONE                        |
| UNLSTSLB                        | Start Date/Time                                   | /SCDL/DB_DATE                     | TSTFR                        |
| UNLSTSHB                        | Finish Date/Time                                  | /SCDL/DB_DATE                     | TSTTO                        |
| UNLETZ                          | Time Zone                                         | /SCDL/DB_DATE                     | TZONE                        |
| UNLETSLB                        | Start Date/Time                                   | /SCDL/DB_DATE                     | TSTFR                        |
| UNLETSHB                        | Finish Date/Time                                  | /SCDL/DB_DATE                     | TSTTO                        |
| LDSTZ                           | Time Zone                                         | /SCDL/DB_DATE                     | TZONE                        |
| LDSTSLB                         | Start Date/Time                                   | /SCDL/DB_DATE                     | TSTFR                        |
| LDSTSHB                         | Finish Date/Time                                  | /SCDL/DB_DATE                     | TSTTO                        |
| LDETZ                           | Time Zone                                         | /SCDL/DB_DATE                     | TZONE                        |
| LDETSLB                         | Start Date/Time                                   | /SCDL/DB_DATE                     | TSTFR                        |
| LDETSHB                         | Finish Date/Time                                  | /SCDL/DB_DATE                     | TSTTO                        |
| PATZ                            | Time Zone                                         | /SCDL/DB_DATE                     | TZONE                        |
| PATSLB                          | Start Date/Time                                   | /SCDL/DB_DATE                     | TSTFR                        |
| PATSHB                          | Finish Date/Time                                  | /SCDL/DB_DATE                     | TSTTO                        |
| PAETZ                           | Time Zone                                         | /SCDL/DB_DATE                     | TZONE                        |
| PATSLB                          | Start Date/Time                                   | /SCDL/DB_DATE                     | TSTFR                        |
| PATSHB                          | Finish Date/Time                                  | /SCDL/DB_DATE                     | TSTTO                        |
| PICKSTZ                         | Time Zone                                         | /SCDL/DB_DATE                     | TZONE                        |
| PICKSTSLB                       | Start Date/Time                                   | /SCDL/DB_DATE                     | TSTFR                        |
| PICKSTSHB                       | Finish Date/Time                                  | /SCDL/DB_DATE                     | TSTTO                        |
| PICKETZ                         | Time Zone                                         | /SCDL/DB_DATE                     | TZONE                        |
| PICKETSLB                       | Start Date/Time                                   | /SCDL/DB_DATE                     | TSTFR                        |
| PICKETSHB                       | Finish Date/Time                                  | /SCDL/DB_DATE                     | TSTTO                        |
| PLTZ                            | Time Zone                                         | /SCDL/DB_DATE                     | TZONE                        |
| PLTSLB                          | Start Date/Time                                   | /SCDL/DB_DATE                     | TSTFR                        |
| PLTSHB                          | Finish Date/Time                                  | /SCDL/DB_DATE                     | TSTTO                        |
| COMPLTZ                         | Time Zone                                         | /SCDL/DB_STATUS                   | TZONE                        |
| COMPLTSLB                       | Start Date/Time                                   | /SCDL/DB_STATUS                   | TSTFR                        |
| WHS_TZONE                       | Time Zone of Warehouse                            | /SCMB/TOENTITY                    | TZONE                        |
| ROCANCEL                        | Indicator: Cancel Data Record                     |                                   |                              |

##### Extractor Logic

The fields in the table of origin for the extract structure largely consist of a 1:1 relation to data-based fields. For an explanation of how the other fields are instead determined by the extractor, see the table below.

| Fields in the Extract Structure | Field Determined by Extractor                                |
| ------------------------------- | ------------------------------------------------------------ |
| REQQTY                          | Determined by extractor: calculated by actual quantity minus adapted quantity. |
| ROCANCEL                        | Determined by extractor: indicator is set if delivery is deleted. |