### Exception Code Descriptions

![DataSource Texts](https://help.sap.com/doc/saphelp_ewm94/9.4/en-US/graphics/BICObjDataSourceTextsMasterData.gif) DataSource Texts: `0WM_EXCCODE_TEXT`

 This DataSource provides descriptions for exception codes that were triggered in your source system.

#### Technical Data

| Application Component    | Warehouse Management — IO (0WM-IO)    |
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
| SPRAS                           | Language Key                                      | /SCWM/TEXCEPT   | SPRAS                        |
| LGNUM                           | Warehouse Number/Warehouse Complex                | /SCWM/TEXCEPT   | LGNUM                        |
| EXCCODE                         | Exception Code                                    | /SCWM/TEXCEPT   | EXCCODE                      |
| DESCR                           | Description                                       | /SCWM/TEXCEPT   | DESCR                        |