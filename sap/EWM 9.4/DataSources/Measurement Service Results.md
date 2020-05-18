### Measurement Service Results

![DataSource Transactional Data](https://help.sap.com/doc/saphelp_ewm94/9.4/en-US/graphics/BICObjDataSourceTransactionalData.gif) DataSource Transactional Data: `0WM_MS_RESULT`

 This DataSource provides you with the results of the measurement services.

![Note](https://help.sap.com/doc/saphelp_ewm94/9.4/en-US/graphics/note.gif) Note

You have already scheduled the report Start Measurement Services with the setting Update Database Table on a regular basis.

#### Technical Data

| Application Component    | Warehouse Management (0WM)              |
| ------------------------ | --------------------------------------- |
| Available as of Release  | SAP SCM 5.1 and SAP EWM 5.1             |
| Shipment                 | SAP NetWeaver 2004s BI Content Add-On 3 |
| Content Versions         | EWM900                                  |
| RemoteCube-Capable       | No                                      |
| Delta-Capable            | Yes, delta process AIE, generic delta   |
| Extraction from Archives | No                                      |
| Verifiable               | No                                      |

#### Data Modeling

| Fields in the Extract Structure | Description of the Field in the Extract Structure | Table of Origin | Field in the Table of Origin |
| ------------------------------- | ------------------------------------------------- | --------------- | ---------------------------- |
| LGNUM                           | Warehouse Number/Warehouse Complex                | /SCWM/MS_RESULT | LGNUM                        |
| MEAS_SERV                       | Measurement Service                               | /SCWM/MS_RESULT | MEAS_SERV                    |
| MS_TYPE                         | Type of Measurement Service                       | /SCWM/MS_RESULT | MS_TYPE                      |
| TIMESTAMP                       | UTC Time Stamp in Short Form (YYYYMMDDhhmmss)     | /SCWM/MS_RESULT | TIMESTAMP                    |
| MS_RESULT                       | Result of a Measurement Service                   | /SCWM/MS_RESULT | RESULT                       |
| WHS_TZONE                       | Time Zone of Warehouse                            | /SCMB/TOENTITY  | TZONE                        |