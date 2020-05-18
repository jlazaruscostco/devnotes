### Warehouse and Full-Time Equivalent Costs

![DataSource Attributes](https://help.sap.com/doc/saphelp_ewm94/9.4/en-US/graphics/BICObjDataSourceAttributesMasterData.gif) DataSource Attributes: `0WM_WHCOST`

 This DataSource provides you with data on warehouse and full-time equivalent costs.

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

| Fields in the Extract Structure | Description of the Field in the Extract Structure     | Table of Origin | Field in the Table of Origin |
| ------------------------------- | ----------------------------------------------------- | --------------- | ---------------------------- |
| LGNUM                           | Warehouse Number/Warehouse Complex                    | /SCWM/TWHCOST   | LGNUM                        |
| BEGDA                           | Start Date                                            | /SCWM/TWHCOST   | BEGDA                        |
| ENDDA                           | End Date                                              | /SCWM/TWHCOST   | ENDDA                        |
| DAILY_FTE                       | Average Number of Full Time Equivalents (FTE) per Day | /SCWM/TWHCOST   | DAILY_FTE                    |
| DAILY_COST_FTE                  | Daily Average Labor Costs per FTE                     | /SCWM/TWHCOST   | DAILY_COST_FTE               |
| DAILY_COST_FIX                  | Daily Average Fixed Costs per Warehouse               | /SCWM/TWHCOST   | DAILY_COST_FIX               |
| COST_CURRENCY                   | Currency Used for Warehouse Costs                     | /SCWM/TWHCOST   | COST_CURRENCY                |