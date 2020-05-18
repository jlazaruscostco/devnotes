### Executed Workload

![DataSource Transactional Data](https://help.sap.com/doc/saphelp_ewm94/9.4/en-US/graphics/BICObjDataSourceTransactionalData.gif) DataSource Transactional Data: `0WM_EWL`

 This DataSource provides you with the executed workload.

![Note](https://help.sap.com/doc/saphelp_ewm94/9.4/en-US/graphics/note.gif) Note

You have already activated Labor Management in Customizing.

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
| EWL_GUID                        | GUID in 'RAW' format                              | /SCWM/EWRKL     | EWL_GUID                     |
| STATUS                          | Executed Workload Status                          | /SCWM/EWRKL     | STATUS                       |
| LGNUM                           | Warehouse Number/Warehouse Complex                |                 |                              |
| PROCS                           | External Storage Process Step                     | /SCWM/EWRKL     | PROCS                        |
| LMAREA                          | LM Activity Area                                  | /SCWM/EWRKL     | LMAREA                       |
| LMOBJTY                         | Reference Obj. Type                               | /SCWM/EWRKL     | LMOBJTY                      |
| GUID_REF                        | GUID in 'RAW' format                              | /SCWM/EWRKL     | GUID_REF                     |
| PC_ID_REF                       | Identification of Partial Confirmation            | /SCWM/EWRKL     | PC_ID_REF                    |
| ID_REF                          | Reference Document                                | /SCWM/EWRKL     | ID_REF                       |
| DURA_PLAN                       | Planned Execution Duration                        | /SCWM/EWRKL     | DURA_PLAN                    |
| DURA_PLAN_ADJ                   | Adjusted Planned Execution Duration               | /SCWM/EWRKL     | DURA_PLAN_ADJ                |
| DURA_ACT                        | Actual Execution Duration                         | /SCWM/EWRKL     | DURA_ACT                     |
| UNIT_T                          | Time Unit                                         | /SCWM/EWRKL     | UNIT_T                       |
| START_ACT                       | Actual Start Date/Time                            | /SCWM/EWRKL     | START_ACT                    |
| FINISH_ACT                      | Actual End Date/Time                              | /SCWM/EWRKL     | FINISH_ACT                   |
| PRR_GUID                        | Business Partner GUID                             | /SCWM/EWRKL     | PRR_GUID                     |
| PRR                             | Processor                                         | /SCWM/EWRKL     | PRR                          |
| CREATED_AT                      | Created at                                        | /SCWM/EWRKL     | CREATED_AT                   |
| CREATED_BY                      | Created By                                        | /SCWM/EWRKL     | CREATED_BY                   |
| CHANGED_AT                      | Time of Data Entry/Data Change                    | /SCWM/EWRKL     | CHANGED_AT                   |
| CHANGED_BY                      | Changed by                                        | /SCWM/EWRKL     | CHANGED_BY                   |
| ALTERED_DIR                     | EWL Changed Manually                              | /SCWM/EWRKL     | ALTERED_DIR                  |
| ENTITLED                        | Party Entitled to Dispose                         | /SCWM/EWRKL     | ENTITLED                     |
| WEIGHT                          | Weight                                            | /SCWM/EWRKL     | WEIGHT                       |
| UNIT_W                          | Weight Unit                                       | /SCWM/EWRKL     | UNIT_W                       |
| VOLUM                           | Volume                                            | /SCWM/EWRKL     | VOLUM                        |
| UNIT_V                          | Volume Unit                                       | /SCWM/EWRKL     | UNIT_V                       |
| TRDIST                          | Calculated Travel Distance                        | /SCWM/EWRKL     | TRDIST                       |
| UNIT_D                          | Unit of Length                                    | /SCWM/EWRKL     | UNIT_D                       |
| QUANTITY                        | Quantity Field                                    | /SCWM/EWRKL     | QUANTITY                     |
| UNIT_Q                          | Unit of Measure                                   | /SCWM/EWRKL     | UNIT_Q                       |
| CAPA                            | Capacity Consumption                              | /SCWM/EWRKL     | CAPA                         |
| NUMSO                           | Number of Sublevel Documents/Items                | /SCWM/EWRKL     | NUMSO                        |
| WHS_TZONE                       | Time Zone of Warehouse                            | /SCMB/TOENTITY  | TZONE                        |

##### Extractor Logic

The fields in the table of origin for the extract structure largely consist of a 1:1 relation to data-based fields. For an explanation of how the other fields are instead determined by the extractor, see the table below.

| Fields in the Extract Structure | Field Determined by Extractor                                |
| ------------------------------- | ------------------------------------------------------------ |
| LGNUM                           | Determined by extractor of supply chain unit                 |
| QUANTITY                        | Note that the default setting leaves the quantity field unfilled, apart from data records for value-added service. To fill this field, BAdI /SCWM/EX_LM_EWRWL_QUAN in enhancement spot /SCWM/ES_LM_WL_QUAN must be implemented in the EWM system. |