### Delivery-Item-Related Execution Data

![DataSource Transactional Data](https://help.sap.com/doc/saphelp_ewm94/9.4/en-US/graphics/BICObjDataSourceTransactionalData.gif) DataSource Transactional Data: `0WM_PL_DLVI`

 This DataSource provides delivery items enriched with warehouse task data, such as the warehouse process type.

![Note](https://help.sap.com/doc/saphelp_ewm94/9.4/en-US/graphics/note.gif) Note

For this DataSource, the number of transferred data records per package may vary greatly between the individual packages.

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

| Fields in the Extract Structure | Description of the Field in the Extract Structure | Table of Origin                                   | Field in the Table of Origin |
| ------------------------------- | ------------------------------------------------- | ------------------------------------------------- | ---------------------------- |
| LGNUM                           | Warehouse Number/Warehouse Complex                | /SCDL/DB_PROCI_I;/SCDL/DB_PROCI_O                 | /SCWM/WHNO                   |
| DOCID                           | Document ID                                       | /SCDL/DB_PROCI_I;/SCDL/DB_PROCI_O;/SCDL/DB_DLVH_O | DOCID                        |
| ITEMID                          | Item ID                                           | /SCDL/DB_PROCI_I;/SCDL/DB_PROCI_O;/SCDL/DB_DLVI_O | ITEMID                       |
| COMPLTSLB                       | Start Date/Time                                   | /SCDL/DB_PROCI_I;/SCDL/DB_PROCI_O                 | CHGTST                       |
| AAREA                           | Activity Area                                     | /SCWM/ORDIM_C                                     | AAREA                        |
| LGTYP                           | Storage Type                                      | /SCWM/ORDIM_C                                     | VLTYP/NLTYP                  |
| PRCES                           | Storage Process                                   | /SCWM/ORDIM_C                                     | PRCES                        |
| PROCS                           | External Storage Process Step                     | /SCWM/ORDIM_C                                     | PROCS                        |
| PROCTY                          | Warehouse Process Type                            | /SCWM/ORDIM_C                                     | PROCTY                       |
| WHS_TZONE                       | Time Zone of Warehouse                            | /SCMB/TOENTITY                                    | TZONE                        |