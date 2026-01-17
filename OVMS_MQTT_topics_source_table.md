# OVMS MQTT topics

T26A/OBD2 -> use T26A if present, else use OBD2

| Tree Topic Row                                   | Name (Home Assistant)                   | Source      |
| ------------------------------------------------ | --------------------------------------- | ----------- |
| m (module/system metrics)                        | Module/System Metrics                   |             |
| ├─ m/egpio                                       | External GPIO                           |             |
| │   ├─ m/egpio/input                             | External GPIO Input                     |             |
| │   └─ m/egpio/output                            | External GPIO Output                    |             |
| ├─ m/freeram                                     | Free RAM                                |             |
| ├─ m/hardware                                    | Hardware Info                           |             |
| ├─ m/monotonic                                   | Monotonic Time                          |             |
| ├─ m/net                                         | Network Info                            |             |
| │   ├─ m/net/connected                           | Network Connected                       |             |
| │   ├─ m/net/good                                | Network Good                            |             |
| │   │   └─ m/net/good/sq                         | Network Good Signal Quality             |             |
| │   ├─ m/net/ip                                  | Network IP Address                      |             |
| │   ├─ m/net/mdm                                 | Modem Info                              |             |
| │   │   ├─ m/net/mdm/iccid                       | Modem ICCID                             |             |
| │   │   ├─ m/net/mdm/mode                        | Modem Mode                              |             |
| │   │   ├─ m/net/mdm/model                       | Modem Model                             |             |
| │   │   ├─ m/net/mdm/netreg                      | Modem Network Registration              |             |
| │   │   ├─ m/net/mdm/network                     | Modem Network Name                      |             |
| │   │   └─ m/net/mdm/sq                          | Modem Signal Quality                    |             |
| │   ├─ m/net/provider                            | Network Provider                        |             |
| │   ├─ m/net/sq                                  | Network Signal Quality                  |             |
| │   ├─ m/net/type                                | Network Type                            |             |
| │   └─ m/net/wifi                                | WiFi Info                               |             |
| │       ├─ m/net/wifi/network                    | WiFi Network Name                       |             |
| │       └─ m/net/wifi/sq                         | WiFi Signal Quality                     |             |
| ├─ m/tasks                                       | System Tasks                            |             |
| ├─ m/time                                        | System Time                             |             |
| │   └─ m/time/utc                                | UTC Time                                |             |
| └─ m/version                                     | Firmware Version                        |             |
| s (server/system namespace (OVMS server events)) | Server/System Events                    |             |
| └─ s/v3 (version of the OVMS protocol / API)     | OVMS Protocol v3                        |             |
| ├─ s/v3/connected                                | OVMS Server Connected                   |             |
| └─ s/v3/peers                                    | OVMS Server Peers                       |             |
| v (vehicle metrics)                              | Vehicle Metrics                         |             |
| ├─ v/b (Battery subsystem)                       | Battery Subsystem                       |             |
| │   ├─ v/b/12v                                   | 12V Battery Voltage (HA)                | [T26A]      |
| │   ├─ v/b/12v/current                           | 12V Battery Current (HA)                | [T26A]      |
| │   ├─ v/b/12v/voltage                           | 12V Battery Voltage (HA)                | [T26A]      |
| │   │   ├─ v/b/12v/voltage/alert                 | 12V Battery Alert (HA)                  | [T26A]      |
| │   │   └─ v/b/12v/voltage/ref                   | 12V Battery Reference Voltage           | [T26A]      |
| │   ├─ v/b/c                                     | Battery Cells                           | [OBD2]      |
| │   │   ├─ v/b/c/temp                            | Cell Temperature                        | [OBD2]      |
| │   │   │   ├─ v/b/c/temp/alert                  | Cell Temperature Alert                  | [OBD2]      |
| │   │   │   ├─ v/b/c/temp/dev                    | Cell Temperature Deviation              | [OBD2]      |
| │   │   │   │   └─ v/b/c/temp/dev/max            | Max Cell Temperature Deviation          | [OBD2]      |
| │   │   │   ├─ v/b/c/temp/max                    | Max Cell Temperature                    | [OBD2]      |
| │   │   │   └─ v/b/c/temp/min                    | Min Cell Temperature                    | [OBD2]      |
| │   │   └─ v/b/c/voltage                         | Cell Voltage                            | [OBD2]      |
| │   │       ├─ v/b/c/voltage/alert               | Cell Voltage Alert                      | [OBD2]      |
| │   │       ├─ v/b/c/voltage/dev                 | Cell Voltage Deviation                  | [OBD2]      |
| │   │       │   └─ v/b/c/voltage/dev/max         | Max Cell Voltage Deviation              | [OBD2]      |
| │   │       ├─ v/b/c/voltage/max                 | Max Cell Voltage                        | [OBD2]      |
| │   │       └─ v/b/c/voltage/min                 | Min Cell Voltage                        | [OBD2]      |
| │   ├─ v/b/cac                                   | Battery CAC (HA)                        | [OBD2]      |
| │   ├─ v/b/capacity                              | Battery Capacity (HA)                   | [OBD2]      |
| │   ├─ v/b/consumption                           | Battery Consumption (HA)                | [OBD2]      |
| │   ├─ v/b/coulomb                               | Battery Coulomb Count (HA)              | [OBD2]      |
| │   │   ├─ v/b/coulomb/recd                      | Battery Coulomb Received (HA)           | [OBD2]      |
| │   │   │   └─ v/b/coulomb/recd/total            | Battery Coulomb Received Total          | [OBD2]      |
| │   │   └─ v/b/coulomb/used                      | Battery Coulomb Used (HA)               | [OBD2]      |
| │   │       └─ v/b/coulomb/used/total            | Battery Coulomb Used Total              | [OBD2]      |
| │   ├─ v/b/current                               | Battery Current (HA)                    | [T26A]      |
| │   ├─ v/b/energy                                | Battery Energy (HA)                     | [OBD2]      |
| │   │   ├─ v/b/energy/recd                       | Battery Energy Received (HA)            | [OBD2]      |
| │   │   │   └─ v/b/energy/recd/total             | Battery Energy Received Total           | [OBD2]      |
| │   │   └─ v/b/energy/used                       | Battery Energy Used (HA)                | [OBD2]      |
| │   │       └─ v/b/energy/used/total             | Battery Energy Used Total               | [OBD2]      |
| │   ├─ v/b/p                                     | Battery Pack Metrics                    | [OBD2]      |
| │   │   ├─ v/b/p/temp                            | Pack Temperature                        | [OBD2]      |
| │   │   │   ├─ v/b/p/temp/avg                    | Average Pack Temperature                | [OBD2]      |
| │   │   │   ├─ v/b/p/temp/max                    | Max Pack Temperature                    | [OBD2]      |
| │   │   │   ├─ v/b/p/temp/min                    | Min Pack Temperature                    | [OBD2]      |
| │   │   │   └─ v/b/p/temp/stddev                 | Pack Temperature StdDev                 | [OBD2]      |
| │   │   │       └─ v/b/p/temp/stddev/max         | Max Pack Temperature StdDev             | [OBD2]      |
| │   │   └─ v/b/p/voltage                         | Pack Voltage                            | [OBD2]      |
| │   │       ├─ v/b/p/voltage/avg                 | Average Pack Voltage                    | [OBD2]      |
| │   │       ├─ v/b/p/voltage/grad                | Pack Voltage Gradient                   | [OBD2]      |
| │   │       ├─ v/b/p/voltage/max                 | Max Pack Voltage                        | [OBD2]      |
| │   │       ├─ v/b/p/voltage/min                 | Min Pack Voltage                        | [OBD2]      |
| │   │       └─ v/b/p/voltage/stddev              | Pack Voltage StdDev                     | [OBD2]      |
| │   │           └─ v/b/p/voltage/stddev/max      | Max Pack Voltage StdDev                 | [OBD2]      |
| │   ├─ v/b/power                                 | Battery Power (HA)                      | [T26A]      |
| │   ├─ v/b/range                                 | Battery Range                           |             |
| │   │   ├─ v/b/range/est                         | Estimated Range (HA)                    | [T26A]      |
| │   │   ├─ v/b/range/full                        | Full Range (HA)                         | [OBD2]      |
| │   │   ├─ v/b/range/ideal                       | Ideal Range (HA)                        | [T26A]      |
| │   │   └─ v/b/range/speed                       | Range at Speed                          | [OBD2]      |
| │   ├─ v/b/soc                                   | State of Charge (HA)                    | [T26A/OBD2] |
| │   ├─ v/b/soh                                   | State of Health (HA)                    | [OBD2]      |
| │   ├─ v/b/temp                                  | Battery Temperature (HA)                | [OBD2]      |
| │   └─ v/b/voltage                               | Battery Voltage (HA)                    | [T26A]      |
| ├─ v/c (Consumption/charging metrics)            | Consumption/Charging Metrics            |             |
| │   ├─ v/c/12v                                   | 12V Battery (HA)                        | [T26A]      |
| │   │   ├─ v/c/12v/current                       | 12V Battery Current (HA)                | [T26A]      |
| │   │   ├─ v/c/12v/power                         | 12V Battery Power (HA)                  | [T26A]      |
| │   │   ├─ v/c/12v/temp                          | 12V Battery Temperature (HA)            | [T26A]      |
| │   │   └─ v/c/12v/voltage                       | 12V Battery Voltage (HA)                | [T26A]      |
| │   ├─ v/c/charging                              | Charging State (HA)                     | [T26A]      |
| │   ├─ v/c/climit                                | Charge Limit (HA)                       | [T26A/OBD2] |
| │   ├─ v/c/current                               | Charge Current (HA)                     | [T26A]      |
| │   ├─ v/c/duration                              | Charge Duration (HA)                    | [T26A/OBD2] |
| │   │   ├─ v/c/duration/full                     | Charge Duration Full                    | [T26A/OBD2] |
| │   │   ├─ v/c/duration/range                    | Charge Duration Range                   | [T26A/OBD2] |
| │   │   └─ v/c/duration/soc                      | Charge Duration SOC                     | [T26A/OBD2] |
| │   ├─ v/c/efficiency                            | Charge Efficiency (HA)                  | [OBD2]      |
| │   ├─ v/c/kwh                                   | Charge kWh (HA)                         | [OBD2]      |
| │   │   ├─ v/c/kwh/grid                          | Charge kWh Grid (HA)                    | [OBD2]      |
| │   │   └─ v/c/kwh/grid/total                    | Charge kWh Grid Total                   | [OBD2]      |
| │   ├─ v/c/limit                                 | Charge Limit (HA)                       | [T26A/OBD2] |
| │   │   └─ v/c/limit/soc                         | Charge Limit SOC                        | [T26A/OBD2] |
| │   │       ├─ v/c/limit/soc/max                 | Charge Limit SOC Max                    | [T26A/OBD2] |
| │   │       └─ v/c/limit/soc/min                 | Charge Limit SOC Min                    | [T26A/OBD2] |
| │   ├─ v/c/mode                                  | Charge Mode (HA)                        | [T26A/OBD2] |
| │   ├─ v/c/pilot                                 | Charge Pilot (HA)                       | [T26A]      |
| │   ├─ v/c/power                                 | Charge Power (HA)                       | [T26A]      |
| │   ├─ v/c/state                                 | Charge State (HA)                       | [T26A/OBD2] |
| │   ├─ v/c/substate                              | Charge Substate                         | [T26A/OBD2] |
| │   ├─ v/c/temp                                  | Charge Temperature (HA)                 | [T26A]      |
| │   ├─ v/c/time                                  | Charge Time (HA)                        | [T26A]      |
| │   ├─ v/c/timermode                             | Charge Timer Mode                       | [T26A/OBD2] |
| │   └─ v/c/voltage                               | Charge Voltage (HA)                     | [T26A]      |
| ├─ v/d                                           | Door/Trunk/Hood Status                  |             |
| │   ├─ v/d/cp                                    | Charge Port Door                        | [T26A]      |
| │   ├─ v/d/fl                                    | Front Left Door                         | [T26A]      |
| │   ├─ v/d/fr                                    | Front Right Door                        | [T26A]      |
| │   ├─ v/d/hood                                  | Hood                                    | [T26A]      |
| │   ├─ v/d/rl                                    | Rear Left Door                          | [T26A]      |
| │   ├─ v/d/rr                                    | Rear Right Door                         | [T26A]      |
| │   └─ v/d/trunk                                 | Trunk                                   | [T26A]      |
| ├─ v/e (Energy / battery subsystem)              | Energy/Battery Subsystem                |             |
| │   ├─ v/e/aux12v                                | Aux 12V Battery                         | [T26A]      |
| │   ├─ v/e/awake                                 | Vehicle Awake                           | [T26A]      |
| │   ├─ v/e/cabintemp                             | Cabin Temperature (HA)                  | [T26A]      |
| │   ├─ v/e/charging12v                           | Charging 12V                            | [T26A]      |
| │   ├─ v/e/drivemode                             | Drive Mode                              | [T26A]      |
| │   ├─ v/e/drivetime                             | Drive Time                              | [T26A]      |
| │   ├─ v/e/gear                                  | Gear                                    | [OBD2]      |
| │   ├─ v/e/headlights                            | Headlights                              | [T26A]      |
| │   ├─ v/e/hvac                                  | HVAC                                    | [T26A]      |
| │   ├─ v/e/locked                                | Vehicle Locked                          | [T26A]      |
| │   ├─ v/e/on                                    | Vehicle On                              | [T26A]      |
| │   ├─ v/e/parktime                              | Park Time                               | [T26A]      |
| │   ├─ v/e/serv                                  | Service                                 | [OBD2]      |
| │   ├─ v/e/serv/range                            | Service Range                           | [OBD2]      |
| │   ├─ v/e/serv/time                             | Service Time                            | [OBD2]      |
| │   └─ v/e/temp                                  | Energy Temperature                      | [T26A]      |
| ├─ v/g                                           | Grid Metrics                            |             |
| │   └─ v/g/time                                  | Grid Time                               | [T26A]      |
| ├─ v/i                                           | Inverter Metrics                        |             |
| │   ├─ v/i/power                                 | Inverter Power                          | [T26A]      |
| │   └─ v/i/temp                                  | Inverter Temperature                    | [T26A]      |
| ├─ v/m                                           | Motor Metrics                           |             |
| │   └─ v/m/temp                                  | Motor Temperature                       | [T26A]      |
| ├─ v/p (position / trip metrics)                 | Position/Trip Metrics                   |             |
| │   ├─ v/p/acceleration                          | Acceleration (HA)                       | [OBD2]      |
| │   ├─ v/p/altitude                              | Altitude (HA)                           | [OBD2]      |
| │   ├─ v/p/direction                             | Direction (HA)                          | [OBD2]      |
| │   ├─ v/p/gpshdop                               | GPS HDOP (HA)                           | [OBD2]      |
| │   ├─ v/p/gpslock                               | GPS Lock (HA)                           | [OBD2]      |
| │   ├─ v/p/gpsmode                               | GPS Mode (HA)                           | [OBD2]      |
| │   ├─ v/p/gpsspeed                              | GPS Speed (HA)                          | [OBD2]      |
| │   ├─ v/p/gpssq                                 | GPS SQ (HA)                             | [OBD2]      |
| │   ├─ v/p/gpstime                               | GPS Time (HA)                           | [OBD2]      |
| │   ├─ v/p/latitude                              | Latitude (HA)                           | [OBD2]      |
| │   ├─ v/p/longitude                             | Longitude (HA)                          | [OBD2]      |
| │   ├─ v/p/odometer                              | Odometer (HA)                           | [T26A]      |
| │   ├─ v/p/satcount                              | Satellite Count (HA)                    | [OBD2]      |
| │   ├─ v/p.speed                                 | Speed (HA)                              | [T26A]      |
| │   ├─ v/p/odometer                              | Odometer (HA)                           | [T26A]      |
| │   └─ v/p/trip                                  | Trip (HA)                               | [T26A]      |
| ├─ v/t (Telematics / telemetry / transport)      | TPMS (tire pressure monitoring systems) |             |
| │   ├─ v/t/alert                                 | Vehicle Alert (HA)                      | [OBD2]      |
| │   └─ v/t/health                                | Vehicle Health (HA)                     | [OBD2]      |
| ├─ v/type                                        | Vehicle Type (HA)                       | [T26A/OBD2] |
| └─ v/vin                                         | Vehicle VIN (HA)                        | [T26A/OBD2] |
| xvu (extended VW e-Up metrics/vehicle-specific)  | Extended VW e-Up Metrics                |             |
| ├─ xvu/b (Battery subsystem)                     | Extended Battery Subsystem              |             |
| │   ├─ xvu/b/c                                   | Extended Battery Cells                  | [OBD2]      |
| │   │   ├─ xvu/b/c/soh                           | Extended Cell State of Health           | [OBD2]      |
| │   ├─ xvu/b/cap                                 | Extended Battery Capacity               | [OBD2]      |
| │   │   ├─ xvu/b/cap/ah                          | Extended Battery Capacity (Ah)          | [OBD2]      |
| │   │   │   ├─ xvu/b/cap/ah/abs                  | Extended Battery Capacity Abs (Ah)      | [OBD2]      |
| │   │   │   └─ xvu/b/cap/ah/norm                 | Extended Battery Capacity Norm (Ah)     | [OBD2]      |
| │   │   └─ xvu/b/cap/kwh                         | Extended Battery Capacity (kWh)         | [OBD2]      |
| │   │       ├─ xvu/b/cap/kwh/abs                 | Extended Battery Capacity Abs (kWh)     | [OBD2]      |
| │   │       ├─ xvu/b/cap/kwh/norm                | Extended Battery Capacity Norm (kWh)    | [OBD2]      |
| │   │       └─ xvu/b/cap/kwh/range               | Extended Battery Capacity Range         | [OBD2]      |
| │   ├─ xvu/b/cell                                | Extended Battery Cell Metrics           | [OBD2]      |
| │   │   └─ xvu/b/cell/delta                      | Extended Battery Cell Delta             | [OBD2]      |
| │   ├─ xvu/b/energy                              | Extended Battery Energy                 | [OBD2]      |
| │   │   └─ xvu/b/energy/range                    | Extended Battery Energy Range           | [OBD2]      |
| │   ├─ xvu/b/hist                                | Extended Battery History                | [OBD2]      |
| │   │   └─ xvu/b/hist/soh                        | Extended Battery History SOH            | [OBD2]      |
| │   │       └─ xvu/b/hist/soh/mod                | Extended Battery History SOH Mod        | [OBD2]      |
| │   │           └─ xvu/b/hist/soh/mod/01...14    | Extended Battery History SOH Mod N      | [OBD2]      |
| │   ├─ xvu/b/soc                                 | Extended Battery SOC                    | [OBD2]      |
| │   │   └─ xvu/b/soc/abs                         | Extended Battery SOC Abs                | [OBD2]      |
| │   ├─ xvu/b/soh                                 | Extended Battery SOH                    | [OBD2]      |
| │   │   ├─ xvu/b/soh/charge                      | Extended Battery SOH Charge             | [OBD2]      |
| │   │   ├─ xvu/b/soh/range                       | Extended Battery SOH Range              | [OBD2]      |
| │   │   └─ xvu/b/soh/vw                          | Extended Battery SOH VW                 | [OBD2]      |
| ├─ xvu/c (Charging subsystem)                    | Extended Charging Subsystem             |             |
| │   ├─ xvu/c/ac                                  | Extended AC Charging                    | [OBD2]      |
| │   │   ├─ xvu/c/ac/i1                           | Extended AC Charging Current 1          | [OBD2]      |
| │   │   ├─ xvu/c/ac/i2                           | Extended AC Charging Current 2          | [OBD2]      |
| │   │   ├─ xvu/c/ac/p                            | Extended AC Charging Power              | [OBD2]      |
| │   │   ├─ xvu/c/ac/u1                           | Extended AC Charging Voltage 1          | [OBD2]      |
| │   │   └─ xvu/c/ac/u2                           | Extended AC Charging Voltage 2          | [OBD2]      |
| │   ├─ xvu/c/ccs                                 | Extended CCS Charging                   | [OBD2]      |
| │   │   ├─ xvu/c/ccs/i                           | Extended CCS Charging Current           | [OBD2]      |
| │   │   ├─ xvu/c/ccs/p                           | Extended CCS Charging Power             | [OBD2]      |
| │   │   └─ xvu/c/ccs/u                           | Extended CCS Charging Voltage           | [OBD2]      |
| │   ├─ xvu/c/dc                                  | Extended DC Charging                    | [OBD2]      |
| │   │   ├─ xvu/c/dc/i1                           | Extended DC Charging Current 1          | [OBD2]      |
| │   │   ├─ xvu/c/dc/i2                           | Extended DC Charging Current 2          | [OBD2]      |
| │   │   ├─ xvu/c/dc/p                            | Extended DC Charging Power              | [OBD2]      |
| │   │   ├─ xvu/c/dc/u1                           | Extended DC Charging Voltage 1          | [OBD2]      |
| │   │   └─ xvu/c/dc/u2                           | Extended DC Charging Voltage 2          | [OBD2]      |
| │   ├─ xvu/c/eff                                 | Extended Charging Efficiency            | [OBD2]      |
| │   │   ├─ xvu/c/eff/calc                        | Extended Charging Efficiency Calc       | [OBD2]      |
| │   │   ├─ xvu/c/eff/ecu                         | Extended Charging Efficiency ECU        | [OBD2]      |
| │   ├─ xvu/c/limit                               | Extended Charging Limit                 | [OBD2]      |
| │   │   └─ xvu/c/limit/soc                       | Extended Charging Limit SOC             | [OBD2]      |
| │   │       ├─ xvu/c/limit/soc/max               | Extended Charging Limit SOC Max         | [OBD2]      |
| │   │       └─ xvu/c/limit/soc/min               | Extended Charging Limit SOC Min         | [OBD2]      |
| │   ├─ xvu/c/loss                                | Extended Charging Loss                  | [OBD2]      |
| │   │   ├─ xvu/c/loss/calc                       | Extended Charging Loss Calc             | [OBD2]      |
| │   │   └─ xvu/c/loss/ecu                        | Extended Charging Loss ECU              | [OBD2]      |
| │   ├─ xvu/c/soc                                 | Extended Charging SOC                   | [OBD2]      |
| │   │   └─ xvu/c/soc/norm                        | Extended Charging SOC Norm              | [OBD2]      |
| │   ├─ xvu/c/timermode                           | Extended Charging Timer Mode            | [OBD2]      |
| │   │   └─ xvu/c/timermode/def                   | Extended Charging Timer Mode Default    | [OBD2]      |
| ├─ xvu/e (Energy / battery subsystem)            | Extended Energy/Battery Subsystem       |             |
| │   ├─ xvu/e/hv                                  | Extended High Voltage Metrics           | [OBD2]      |
| │   │   └─ xvu/e/hv/chgmode                      | Extended HV Charging Mode               | [OBD2]      |
| │   ├─ xvu/e/lv                                  | Extended Low Voltage Metrics            | [OBD2]      |
| │   │   ├─ xvu/e/lv/autochg                      | Extended LV Auto Charge                 | [OBD2]      |
| │   │   └─ xvu/e/lv/pwrstate                     | Extended LV Power State                 | [OBD2]      |
| │   └─ xvu/e/serv                                | Extended Service Metrics                | [OBD2]      |
| │       └─ xvu/e/serv/days                       | Extended Service Days                   | [OBD2]      |
| ├─ xvu/m                                         | Extended Motor Metrics                  | [OBD2]      |
| │   ├─ xvu/m/soc                                 | Extended Motor SOC                      | [OBD2]      |
| │   │   ├─ xvu/m/soc/abs                         | Extended Motor SOC Abs                  | [OBD2]      |
| │   │   └─ xvu/m/soc/norm                        | Extended Motor SOC Norm                 | [OBD2]      |
| │   └─ xvu/m/version                             | Extended Motor Version                  | [OBD2]      |
| └─ xvu/v                                         | Extended Vehicle Metrics                | [OBD2]      |
| └─ xvu/v/t                                       | Extended Vehicle Transport Metrics      | [OBD2]      |
| ├─ xvu/v/t/diff                                  | Extended Vehicle Transport Diff         | [OBD2]      |
| └─ xvu/v/t/emgcy                                 | Extended Vehicle Transport Emergency    | [OBD2]      |
| notify                                           | Notifications                           |             |
| └─ notify/alert                                  | Alert Notifications                     |             |
| ├─ notify/alert/charge                           | Charge Alert Notification               |             |
| │   └─ notify/alert/charge/stopped               | Charge Stopped Alert                    |             |
| └─ notify/info                                   | Info Notifications                      |             |
| └─ notify/info/charge                            | Charge Info Notification                |             |
| └─ notify/info/charge/started                    | Charge Started Info                     |             |
| status                                           | Status                                  |             |
