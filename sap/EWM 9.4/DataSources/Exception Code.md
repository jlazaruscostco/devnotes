### Exception Code

![DataSource Transactional Data](https://help.sap.com/doc/saphelp_ewm94/9.4/en-US/graphics/BICObjDataSourceTransactionalData.gif) DataSource Transactional Data: `0WM_EXCCODE`

 This DataSource provides you with exception codes that were triggered in your source system.

![Note](https://help.sap.com/doc/saphelp_ewm94/9.4/en-US/graphics/note.gif) Note

You have already activated the history update for your exception codes in Customizing.

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

| Fields in the Extract Structure | Description of the Field in the Extract Structure | Table of Origin | Field in the Table of Origin |
| ------------------------------- | ------------------------------------------------- | --------------- | ---------------------------- |
| LGNUM                           | Warehouse Number/Warehouse Complex                | /SCWM/EXCEPHIST | LGNUM                        |
| EXCODE                          | Exception Code                                    | /SCWM/EXCEPHIST | EXCODE                       |
| BUSCON                          | Business Context                                  | /SCWM/EXCEPHIST | BUSCON                       |
| EXECSTEP                        | Execution Step                                    | /SCWM/EXCEPHIST | EXECSTEP                     |
| PROCESSOR                       | Processor                                         | /SCWM/EXCEPHIST | PROCESSOR                    |
| TIMESTAMP                       | UTC Time Stamp in Short Form (YYYYMMDDhhmmss)     | /SCWM/EXCEPHIST | TIMESTAMP                    |
| EXC_OBJTYPE                     | Object Type of Exception                          |                 |                              |
| EXC_OBJID                       | Object Key for Exception Code History             | /SCWM/EXCEPHIST | OBJID                        |
| WHS_TZONE                       | Time Zone of Warehouse                            | /SCMB/TOENTITY  | TZONE                        |

##### Extractor Logic

The fields in the table of origin for the extract structure largely consist of a 1:1 relation to data-based fields. For an explanation of how the other fields are instead determined by the extractor, see the table below.

| Fields in the Extract Structure | Field Determined by Extractor |
| ------------------------------- | ----------------------------- |
| EXC_OBJTYPE                     | Determined by extractor.      |