### Transportation Units

![DataSource Transactional Data](https://help.sap.com/doc/saphelp_ewm94/9.4/en-US/graphics/BICObjDataSourceTransactionalData.gif) DataSource Transactional Data: `0WM_TU`

 This DataSource provides you with transportation unit data.

#### Technical Data

| Application Component    | Warehouse Management 0WM              |
| ------------------------ | ------------------------------------- |
| Available as of Release  | SAP EWM 900                           |
| Shipment                 | SAP NetWeaver 7.0 BI Content Add-On 7 |
| Content Versions         | EWM900                                |
| RemoteCube-Capable       | No                                    |
| Delta-Capable            | Yes, delta process AIE; generic delta |
| Extraction from Archives | No                                    |
| Verifiable               | No                                    |

#### Data Modeling

| Fields in the Extract Structure | Description of the Field in the Extract Structure           | Table of Origin            | Field in the Table of Origin |
| ------------------------------- | ----------------------------------------------------------- | -------------------------- | ---------------------------- |
| TU_NUM                          | Internal Number of Transportation Unit                      | /SCWM/TUNIT                | TU_NUM                       |
| TU_SR_ACT_NUM                   | Shipping and Receiving Activity Number: Transportation Unit | /SCWM/TU_SR_ACT            | TU_SR_ACT_NUM                |
| TU_NUM_EXT                      | Transportation Unit                                         | /SCWM/TUNIT                | TU_NUM_EXT                   |
| MTR                             | Means of Transport                                          | /SCWM/TUNIT                | MTR                          |
| TSP                             | Carrier                                                     | /SCWM/TU_SR_ACT            | TSP_CURR                     |
| SCAC                            | Partner: Standard Carrier Alpha Code                        | /SCWM/TU_SR_ACT            | SCAC_CURR                    |
| LIC_PLATE_COUNTRY               | Country of Registration Number                              | /SCWM/TUNIT                | LIC_PLATE_CNTRY              |
| LIC_PLATE                       | License Plate Number for Transportation Unit                | /SCWM/TUNIT                | LIC_PLATE                    |
| ACT_DIR                         | Direction                                                   | /SCWM/TU_SR_ACT            | ACT_DIR                      |
| ROUTE                           | Route Name (Identification)                                 | /SCWM/TU_SR_ACT            | ROUTE_CURR                   |
| ROUTE_DEP                       | Departure Time Stamp for Route                              | /SCWM/TU_SR_ACT            | ROUTE_DEP                    |
| LOAD_WEIGHT                     | Loading Weight of Transportation Unit                       | /SCWM/TU_SR_ACT            | LOAD_WEIGHT                  |
| LOAD_WEIGHT_UOM                 | Weight Unit                                                 | /SCWM/TU_SR_ACT            | LOAD_WEIGHT_UOM              |
| LOAD_VOLUME                     | Loading Volume of Transportation Unit                       | /SCWM/TU_SR_ACT            | LOAD_VOLUME                  |
| LOAD_VOLUME_UOM                 | Volume Unit                                                 | /SCWM/TU_SR_ACT            | LOAD_VOLUME_UOM              |
| TU_WEIGHT                       | Weighed Total Weight of Transportation Unit                 | /SCWM/HUHDR                | T_WEIGHT                     |
| TU_WEIGHT_UOM                   | Weight Unit                                                 | /SCWM/HUHDR                | UNIT_TW                      |
| TU_VOLUME                       | Calculated Total Volume of Transportation Unit              | /SCWM/HUHDR                | T_VOLUME                     |
| TU_VOL_UOM                      | Volume Unit                                                 | /SCWM/HUHDR                | UNIT_TV                      |
| START_PLAN_TSTFR                | Start Time Stamp for Planned Start of S&R Activity          | /SCWM/TU_SR_ACT            | START_PLAN_TSTFR             |
| START_PLAN_TSTTO                | End Time Stamp for Planned Start of S& R Activity           | /SCWM/TU_SR_ACT            | START_PLAN_TSTTO             |
| END_PLAN_TSTFR                  | Start Time Stamp for Planned End of S&R Activity            | /SCWM/TU_SR_ACT            | END_PLAN_TSTFR               |
| END_PLAN_TSTTO                  | End Time Stamp for Planned End of S&R Activity              | /SCWM/TU_SR_ACT            | END_PLAN_TSTTO               |
| START_ACTUAL                    | Time Stamp for Actual Start of S&R Activity                 | /SCWM/TU_SR_ACT            | START_ACTUAL                 |
| END_ACTUAL                      | Time Stamp for Actual End of S&R Activity                   | /SCMB/DE_SR_ACT_END_ACTUAL | END_ACTUAL                   |
| YARD_LGNUM                      | Warehouse Number for Yard                                   | /SCWM/TU_SR_ACT            | YARD                         |
| LGNUM                           | Warehouse Number                                            | /SCWM/TU_DLV               | LGNUM                        |
| DOOR                            | Source Warehouse Door                                       | /SCWM/TU_DOOR              | DOOR                         |
| FRD_NUM                         | Freight Document Number                                     | /SCWM/TU_SR_ACT            | FRD_NUM                      |
| TRANSPL_TYPE                    | Transportation Planning Type                                | /SCWM/TU_SR_ACT            | TRANSPL_TYPE                 |
| LOGSYS                          | Receiving Logical System                                    | /SCWM/TU_SR_ACT            | LOGSYS                       |
| WHS_TZONE                       | Time Zone of Warehouse                                      | /SCMB/TOENTITY             | TZONE                        |
| VEH_NUM                         | Internal Vehicle Number                                     | /SCWM/TU_VEH               | VEH_NUM                      |
| VEH_NUM_EXT                     | Vehicle                                                     | /SCWM/VEHICLE              | VEH_NUM_EXT                  |
| COUNT_HU                        | Number of Assigned HUs                                      |                            |                              |
| COUNT_DLVH                      | Number of Assigned Deliveries                               |                            |                              |
| COUNT_DLVI                      | Number of Assigned Delivery Items                           |                            |                              |
| DURATION_IN_MIN                 | Time in Yard in Minutes                                     |                            |                              |

##### Extractor Logic

The fields in the table of origin for the extract structure largely consist of a 1:1 relation to data-based fields. For an explanation of how the other fields are instead determined by the extractor, see the table below.

| Fields in the Extract Structure | Field Determined by Extractor                                |
| ------------------------------- | ------------------------------------------------------------ |
| COUNT_HU                        | Determined by extractor.                                     |
| COUNT_DLVH                      | Determined by extractor.                                     |
| COUNT_DLVI                      | Determined by extractor.                                     |
| DURATION_IN_MIN                 | Determined by extractor in BAdI, Calculation of Time in Yard: /SCWM/EX_BW_TU_DURATION.This BAdI provides a fallback class default implementation that sets the Time in Yard in Minutes, based on actual start and end date.You can use this BAdI from Enhancement Spot /SCWM/ES_BW to implement your own logic for the field Time in Yard in Minutes. |