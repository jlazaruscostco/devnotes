### Storage Bins Full Upload

![DataSource Transactional Data](https://help.sap.com/doc/saphelp_ewm94/9.4/en-US/graphics/BICObjDataSourceTransactionalData.gif) DataSource Transactional Data: `0WM_BIN_FULL`

 This DataSource provides you with storage bin data.

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

| Fields in the Extract Structure | Description of the Field in the Extract Structure | Table of Origin | Field in the Table of Origin |
| ------------------------------- | ------------------------------------------------- | --------------- | ---------------------------- |
| LGNUM                           | Warehouse Number/Warehouse Complex                | /SCWM/LAGP      | LGNUM                        |
| LGTYP                           | Storage Type                                      | /SCWM/LAGP      | LGTYP                        |
| LGPLA                           | Storage Bin                                       | /SCWM/LAGP      | LGPLA                        |
| LGBER                           | Storage Section                                   | /SCWM/LAGP      | LGBER                        |
| LPTYP                           | Storage Bin Type                                  | /SCWM/LAGP      | LPTYP                        |
| BIN_AT                          | Bin Access Type                                   | /SCWM/LAGP      | BIN_AT                       |
| FLGSBIN                         | Storage Bin is Subdivided                         | /SCWM/LAGP      | FLGSBIN                      |
| ANZLE                           | Number of Handling Units in Storage Bin           | /SCWM/LAGP      | ANZLE                        |
| MAXLE                           | Maximum Number of Handling Units in Storage Bin   | /SCWM/LAGP      | MAXLE                        |
| KZLER                           | Indicates Whether Storage Bin is Empty            | /SCWM/LAGP      | KZLER                        |
| AISLE                           | Aisle in a Storage Bin                            | /SCWM/LAGP      | AISLE                        |
| STACK                           | Stack in a Storage Bin                            | /SCWM/LAGP      | STACK                        |
| LVL_V                           | Level in a Storage Bin                            | /SCWM/LAGP      | LVL_V                        |
| FIXBINTYP                       | Fixed Storage Bin Type                            | /SCWM/LAGP      | FIXBINTYP                    |
| ST_ROLE                         | Storage Type Role                                 | /SCWM/T331      | ST_ROLE                      |
| BEHAV                           | Storage Behavior                                  | /SCWM/T331      | BEHAV                        |
| NOCAPAUPD                       | No Update of Capacity Data and Empty Flag         | /SCWM/T331      | NOCAPAUPD                    |
| EXTRACT_DATE                    | Extraction Date                                   |                 |                              |
| EXTRACT_TIME                    | Extraction Time                                   |                 |                              |

##### Extractor Logic

The fields in the table of origin for the extract structure largely consist of a 1:1 relation to data-based fields. For an explanation of how the other fields are instead determined by the extractor, see the table below.

| Fields in the Extract Structure | Field Determined by Extractor                          |
| ------------------------------- | ------------------------------------------------------ |
| EXTRACT_DATE                    | Determined by extractor, given in warehouse time zone. |
| EXTRACT_TIME                    | Determined by extractor, given in warehouse time zone. |