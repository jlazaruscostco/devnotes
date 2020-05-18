### Warehouse Orders

![DataSource Transactional Data](https://help.sap.com/doc/saphelp_ewm94/9.4/en-US/graphics/BICObjDataSourceTransactionalData.gif) DataSource Transactional Data: `0WM_WO`

 This DataSource provides you with confirmed and canceled warehouse orders.

#### Technical Data

| Application Component    | Warehouse Management (0WM)              |
| ------------------------ | --------------------------------------- |
| Available as of Release  | SAP SCM 5.1 and SAP EWM 5.1             |
| Shipment                 | SAP NetWeaver 2004s BI Content Add-On 3 |
| Content Versions         | EWM900                                  |
| RemoteCube-Capable       | No                                      |
| Delta-Capable            | Yes, delta process AIM                  |
| Extraction from Archives | No                                      |
| Verifiable               | No                                      |

#### Data Modeling

| Fields in the Extract Structure | Description of the Field in the Extract Structure | Table of Origin | Field in the Table of Origin |
| ------------------------------- | ------------------------------------------------- | --------------- | ---------------------------- |
| MANDT                           | Client                                            | /SCWM/WHO       | MANDT                        |
| LGNUM                           | Warehouse Number/Warehouse Complex                | /SCWM/WHO       | LGNUM                        |
| WHO                             | Warehouse Order Number                            | /SCWM/WHO       | WHO                          |
| WCR                             | Warehouse Order Creation Rule                     | /SCWM/WHO       | WCR                          |
| TYPE                            | Category of Warehouse Order Creation Rule         | /SCWM/WHO       | TYPE                         |
| HDR_PROCTY                      | Document Header Warehouse Process Type            | /SCWM/WHO       | HDR_PROCTY                   |
| WAVE                            | Wave                                              | /SCWM/WHO       | WAVE                         |
| STATUS                          | Warehouse Order Status                            | /SCWM/WHO       | STATUS                       |
| AREAWHO                         | Activity Area                                     | /SCWM/WHO       | AREAWHO                      |
| CREATED_AT                      | Created at                                        | /SCWM/WHO       | CREATED_AT                   |
| CREATED_DATE                    | Created On                                        |                 |                              |
| CREATED_TIME                    | Created At                                        |                 |                              |
| CREATED_BY                      | Created By                                        | /SCWM/WHO       | CREATED_BY                   |
| QUEUE                           | Queue                                             | /SCWM/WHO       | QUEUE                        |
| STARTED_AT                      | Start Time                                        | /SCWM/WHO       | STARTED_AT                   |
| STARTED_DATE                    | Start Date                                        |                 |                              |
| STARTED_TIME                    | Start Time                                        |                 |                              |
| CONFIRMED_AT                    | Time of Confirmation                              | /SCWM/WHO       | CONFIRMED_AT                 |
| CONFIRMED_DATE                  | Confirmation Date                                 |                 |                              |
| CONFIRMED_TIME                  | Confirmation Time                                 |                 |                              |
| CONFIRMED_BY                    | Confirmed by                                      | /SCWM/WHO       | CONFIRMED_BY                 |
| PROCESSOR                       | Processor                                         | /SCWM/WHO       | PROCESSOR                    |
| RSRC                            | Resource (Means of Transportation or User)        | /SCWM/WHO       | RSRC                         |
| MAN_ASSIGN                      | Manual Assignment of Processor                    | /SCWM/WHO       | MAN_ASSIGN                   |
| FLGINV                          | WO Contains Physical Inventory Document           | /SCWM/WHO       | FLGINV                       |
| FLGSPLIT                        | Warehouse Order Was Split                         | /SCWM/WHO       | FLGSPLIT                     |
| LSD                             | Latest Starting Date (LSD)                        | /SCWM/WHO       | LSD                          |
| PLANDURA                        | Planned Execution Time of Warehouse Order         | /SCWM/WHO       | PLANDURA                     |
| CHANGED_AT                      | Time of Change                                    | /SCWM/WHO       | CHANGED_AT                   |
| CHANGED_DATE                    | Changed On                                        |                 |                              |
| CHANGED_TIME                    | Changed At                                        |                 |                              |
| CHANGED_BY                      | Changed By                                        | /SCWM/WHO       | CHANGED_BY                   |
| UNIT_T                          | Warehouse Order: Time Unit                        | /SCWM/WHO       | UNIT_T                       |
| FLGTO                           | Warehouse Order Contains Warehouse Task           | /SCWM/WHO       | FLGTO                        |
| HAZMAT                          | Hazardous Substance Relevant for Storage          | /SCWM/WHO       | HAZMAT                       |
| WHOID                           | Unique Identification of the Warehouse Order      | /SCWM/WHO       | WHOID                        |
| ROCANCEL                        | Indicator: Cancel Data Record                     |                 |                              |
| ACT_TYPE                        | Activity                                          | /SCWM/T333      | ACT_TYPE                     |
| RSRC_TYPE                       | Resource Type                                     | /SCWM/RSRC      | RSRC_TYPE                    |

##### Extractor Logic

The fields in the table of origin for the extract structure largely consist of a 1:1 relation to data-based fields. For an explanation of how the other fields are instead determined by the extractor, see the table below.

| Fields in the Extract Structure | Field Determined by Extractor                                |
| ------------------------------- | ------------------------------------------------------------ |
| CREATED_DATE                    | Determined by extractor, given in warehouse time zone.       |
| CREATED_TIME                    | Determined by extractor, given in warehouse time zone.       |
| STARTED_DATE                    | Determined by extractor, given in warehouse time zone.       |
| STARTED_TIME                    | Determined by extractor, given in warehouse time zone.       |
| CONFIRMED_DATE                  | Determined by extractor, given in warehouse time zone.       |
| CONFIRMED_TIME                  | Determined by extractor, given in warehouse time zone.       |
| CHANGED_DATE                    | Determined by extractor, given in warehouse time zone.       |
| CHANGED_TIME                    | Determined by extractor, given in warehouse time zone.       |
| ROCANCEL                        | Determined by extractor: Indicator: Cancel Data Record.ROCANCEL is never set since warehouse orders are not deleted after confirmation or cancellation. |