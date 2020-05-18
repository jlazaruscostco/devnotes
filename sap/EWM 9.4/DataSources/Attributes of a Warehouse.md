### Attributes of a Warehouse

![DataSource Attributes](https://help.sap.com/doc/saphelp_ewm94/9.4/en-US/graphics/BICObjDataSourceAttributesMasterData.gif) DataSource Attributes: `0WM_LGNUM_ATTR`

This DataSource provides you with the attributes of a warehouse.

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
| LGNUM                           | Warehouse Number/Warehouse Complex                | /SCWM/T300      | LGNUM                        |
| TZONE                           | Time Zone                                         |                 |                              |

##### Extractor Logic

The fields in the table of origin for the extract structure largely consist of a 1:1 relation to data-based fields. For an explanation of how the other fields are instead determined by the extractor, see the table below.

| Fields in the Extract Structure | Field Determined by Extractor                                |
| ------------------------------- | ------------------------------------------------------------ |
| TZONE                           | Determined by extractor of the supply chain unit of the warehouse. |