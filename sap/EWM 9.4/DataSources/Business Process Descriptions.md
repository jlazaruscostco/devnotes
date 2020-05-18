### # Business Process Descriptions

![DataSource Texts](https://help.sap.com/doc/saphelp_ewm94/9.4/en-US/graphics/BICObjDataSourceTextsMasterData.gif) DataSource Texts: `0WM_DLVPROC_TEXT`

 This DataSource provides you with texts that define a business process for a delivery item.

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

| Fields in the Extract Structure | Description of the Field in the Extract Structure | Table of Origin  | Field in the Table of Origin |
| ------------------------------- | ------------------------------------------------- | ---------------- | ---------------------------- |
| LANGU                           | Language Key                                      | /SCWM/TBWDLVPROT | LANGU                        |
| DLVPROC                         | Business Process                                  | /SCWM/TBWDLVPROT | DLVPROC                      |
| DESCR                           | Description                                       | /SCWM/TBWDLVPROT | DESCR                        |