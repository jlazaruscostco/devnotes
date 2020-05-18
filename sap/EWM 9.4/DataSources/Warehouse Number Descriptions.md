### Warehouse Number Descriptions

![DataSource Texts](https://help.sap.com/doc/saphelp_ewm94/9.4/en-US/graphics/BICObjDataSourceTextsMasterData.gif) DataSource Texts: `0WM_LGNUM_TEXT`

 This DataSource provides you with the descriptions of the warehouse numbers.

#### Technical Data

| Application Component    | Warehouse Management (0WM-IO)           |
| ------------------------ | --------------------------------------- |
| Available as of Release  | SAP SCM 5.1 and SAP EWM 5.1             |
| Shipment                 | SAP NetWeaver 2004s BI Content Add-On 3 |
| Content Versions         | 1                                       |
| RemoteCube-Capable       | No                                      |
| Delta-Capable            | No                                      |
| Extraction from Archives | No                                      |
| Verifiable               | No                                      |

#### Data Modeling

| Fields in the Extract Structure | Description of the Field in the Extract Structure | Table of Origin | Field in the Table of Origin |
| ------------------------------- | ------------------------------------------------- | --------------- | ---------------------------- |
| SPRAS                           | Language Key                                      | /SCWM/T300T     | SPRAS                        |
| LGNUM                           | Warehouse Number/Warehouse Complex                | /SCWM/T300T     | LGNUM                        |
| LNUMT                           | Description                                       | /SCWM/T300T     | LNUMT                        |