### Measurement Service Names

![DataSource Texts](https://help.sap.com/doc/saphelp_ewm94/9.4/en-US/graphics/BICObjDataSourceTextsMasterData.gif) DataSource Texts: `0WM_MS_TEXT`

 This DataSource provides you with the names of the measurement services.

#### Technical Data

| Application Component    | Warehouse Management — IO (0WM-IO)      |
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
| LANGU                           | Language Key                                      | /SCWM/TMS_TEXT  | LANGU                        |
| LGNUM                           | Warehouse Number/Warehouse Complex                | /SCWM/TMS_TEXT  | LGNUM                        |
| MEAS_SERV                       | Measurement Service                               | /SCWM/TMS_TEXT  | MEAS_SERV                    |
| MS_TYPE                         | Type of Measurement Service                       | /SCWM/TMS_TEXT  | MS_TYPE                      |
| MEAS_SERV_TXT                   | Measurement Service Description                   | /SCWM/TMS_TEXT  | MEAS_SERV_TXT                |