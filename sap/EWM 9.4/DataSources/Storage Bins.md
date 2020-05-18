### Storage Bins

![DataSource Transactional Data](https://help.sap.com/doc/saphelp_ewm94/9.4/en-US/graphics/BICObjDataSourceTransactionalData.gif) DataSource Transactional Data: `0WM_BIN`

 This DataSource provides you with storage bins.

#### Technical Data

| Application Component    | Warehouse Management (0WM)              |
| ------------------------ | --------------------------------------- |
| Available as of Release  | SAP SCM 5.1 and EWM 5.1                 |
| Shipment                 | SAP NetWeaver 2004s BI Content Add-On 3 |
| Content Versions         | 2                                       |
| RemoteCube-Capable       | No                                      |
| Delta-Capable            | Yes, delta process AIMD                 |
| Extraction from Archives | No                                      |
| Verifiable               | No                                      |

#### Data Modeling

| Fields in the Extract Structure | Description of the Field in the Extract Structure | Table of Origin | Field in the Table of Origin |
| ------------------------------- | ------------------------------------------------- | --------------- | ---------------------------- |
| MANDT                           | Client                                            | /SCWM/LAGP      | MANDT                        |
| LGNUM                           | Warehouse Number/Warehouse Complex                | /SCWM/LAGP      | LGNUM                        |
| LGPLA                           | Storage Bin                                       | /SCWM/LAGP      | LGPLA                        |
| LGTYP                           | Storage Type                                      | /SCWM/LAGP      | LGTYP                        |
| LGBER                           | Storage Section                                   | /SCWM/LAGP      | LGBER                        |
| LPTYP                           | Storage Bin Type                                  | /SCWM/LAGP      | LPTYP                        |
| BIN_AT                          | Bin Access Type                                   | /SCWM/LAGP      | BIN_AT                       |
| PLAUF                           | Section of a Storage Bin                          | /SCWM/LAGP      | PLAUF                        |
| SKZUA                           | Block Indicator: For Stock Removals               | /SCWM/LAGP      | SKZUA                        |
| SKZUE                           | Block Indicator: For Putaways                     | /SCWM/LAGP      | SKZUE                        |
| ANZLE                           | Number of Handling Units in Storage Bin           | /SCWM/LAGP      | ANZLE                        |
| MAXLE                           | Maximum Number of Handling Units in Storage Bin   | /SCWM/LAGP      | MAXLE                        |
| WEIGHT                          | Weight of Materials in Storage Bin                | /SCWM/LAGP      | WEIGHT                       |
| MAX_WEIGHT                      | Load Capacity of Storage Bin                      | /SCWM/LAGP      | MAX_WEIGHT                   |
| UNIT_W                          | Weight Unit                                       | /SCWM/LAGP      | UNIT_W                       |
| VOLUM                           | Loading/Net Volume                                | /SCWM/LAGP      | VOLUM                        |
| MAX_VOLUME                      | Maximum Allowed Volume                            | /SCWM/LAGP      | MAX_VOLUME                   |
| UNIT_V                          | Volume Unit                                       | /SCWM/LAGP      | UNIT_V                       |
| MAX_CAPA                        | Total Capacity of Storage Bin                     | /SCWM/LAGP      | MAX_CAPA                     |
| FCAPA                           | Available Capacity in Storage Bin                 | /SCWM/LAGP      | FCAPA                        |
| KZLER                           | Indicator Whether Storage Bin is Empty            | /SCWM/LAGP      | KZLER                        |
| MOVED_AT                        | Last Movement to Bin                              | /SCWM/LAGP      | MOVED_AT                     |
| MOVED_DATE                      | Date of Last Movement                             |                 |                              |
| MOVED_TIME                      | Time of Last Movement                             |                 |                              |
| CLEARED_AT                      | Last Bin Clearing                                 | /SCWM/LAGP      | CLEARED_AT                   |
| CLEARED_DATE                    | Date of Last Bin Clearing                         |                 |                              |
| CLEARED_TIME                    | Time of Last Clearing                             |                 |                              |
| CHANGED_AT                      | Time of Change                                    | /SCWM/LAGP      | CHANGED_AT                   |
| CHANGED_DATE                    | Changed On                                        |                 |                              |
| CHANGED_TIME                    | Changed At                                        |                 |                              |
| AISLE                           | Aisle in a Storage Bin                            | /SCWM/LAGP      | AISLE                        |
| STACK                           | Stack in a Storage Bin                            | /SCWM/LAGP      | STACK                        |
| LVL_V                           | Level in a Storage Bin                            | /SCWM/LAGP      | LVL_V                        |
| BINSC                           | Bin Section of a Storage Bin                      | /SCWM/LAGP      | BINSC                        |
| DEPTH                           | Bin Depth                                         | /SCWM/LAGP      | DEPTH                        |
| X_CORD                          | X Coordinate                                      | /SCWM/LAGP      | X_CORD                       |
| Y_CORD                          | Y Coordinate                                      | /SCWM/LAGP      | Y_CORD                       |
| Z_CORD                          | Z Coordinate                                      | /SCWM/LAGP      | Z_CORD                       |
| FIXBINTYP                       | Fix Storage Bin Type                              | /SCWM/LAGP      | FIXBINTYP                    |
| ROCANCEL                        | Indicator: Cancel Data Record                     |                 |                              |

##### Extractor Logic

The fields in the table of origin for the extract structure largely consist of a 1:1 relation to data-based fields. For an explanation of how the other fields are instead determined by the extractor, see the table below.

| Fields in the Extract Structure | Field Determined by Extractor                                |
| ------------------------------- | ------------------------------------------------------------ |
| MOVED_DATE                      | Determined by extractor, given in warehouse time zone.       |
| MOVED_TIME                      | Determined by extractor, given in warehouse time zone.       |
| CLEARED_DATE                    | Determined by extractor, given in warehouse time zone.       |
| CLEARED_TIME                    | Determined by extractor, given in warehouse time zone.       |
| CHANGED_DATE                    | Determined by extractor, given in warehouse time zone.       |
| CHANGED_TIME                    | Determined by extractor, given in warehouse time zone.       |
| ROCANCEL                        | Determined by extractor: Indicator: Cancel Data Record.When you delete a storage bin, this information is also extracted. In this case, the system sets the indicator ROCANCEL. |