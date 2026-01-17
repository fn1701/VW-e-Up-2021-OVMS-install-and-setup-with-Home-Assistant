# OVMS Command Hierarchical Tree

## Core System Commands

```plain
├── help - Ask for help
├── exit - End console session  
├── enable - Enter secure mode (enable access to all commands)
├── disable - Leave secure mode (disable access to most commands)
├── sleep - Script utility: pause execution
├── echo - Script utility: output text
└── . - Run a script
```

## System Framework Commands

```plain
├── boot - BOOT framework
│   ├── status - Show boot system status
│   └── clear - Clear/reset boot system status
│
├── config - CONFIG framework
│   ├── list [<param>] - Show configuration parameters/instances
│   ├── set <param> <instance> <value> - Set parameter:instance=value
│   ├── rm <param> {<instance> | *} - Remove parameter:instance
│   ├── backup <zipfile> [password] - Backup to file
│   └── restore <zipfile> [password] - Restore from file
│   │
│   └── Available Parameters:
│       ├── auto - Auto init configuration
│       │   ├── init - Enable auto start
│       │   ├── dbc - Auto load DBC files
│       │   ├── ext12v - Auto start external 12V
│       │   ├── egpio - Auto start EGPIO
│       │   ├── modem - Auto start modem
│       │   ├── server.v2 - Auto start V2 server
│       │   ├── server.v3 - Auto start V3 server
│       │   ├── scripting - Auto start scripting
│       │   ├── vehicle.type - Vehicle type
│       │   ├── obd2ecu - OBD2ECU configuration
│       │   ├── wifi.mode - WiFi mode (ap/client)
│       │   ├── wifi.ssid.ap - WiFi AP SSID
│       │   └── wifi.ssid.client - WiFi client SSID
│       ├── can - CAN Configuration
│       ├── dbc - DBC Configuration
│       ├── egpio - EGPIO configuration
│       │   └── monitor.ports - Monitor ports
│       ├── log - Logging configuration
│       ├── modem - Modem configuration
│       │   ├── apn - APN
│       │   ├── apn.user - APN username
│       │   ├── apn.password - APN password
│       │   ├── pincode - PIN code
│       │   ├── enable.net - Enable network
│       │   ├── enable.sms - Enable SMS
│       │   ├── enable.gps - Enable GPS
│       │   ├── enable.gpstime - Enable GPS time sync
│       │   ├── gps.parkpause - GPS park pause
│       │   ├── gps.parkreactivate - GPS park reactivate
│       │   └── gps.parkreactlock - GPS park react lock
│       ├── module - Module configuration
│       ├── network - Network Configuration
│       │   ├── dns - DNS servers
│       │   ├── modem.sq.good - Good signal quality threshold
│       │   └── modem.sq.bad - Bad signal quality threshold
│       ├── notify - Notification filters
│       ├── obd2ecu - OBD2ECU configuration
│       ├── obd2ecu.map - OBD2ECU metric map
│       ├── ota - OTA setup and status
│       ├── password - Password store (protected)
│       │   ├── module - Module password
│       │   ├── pin - PIN code
│       │   └── server.v3 - Server V3 password
│       ├── plugin - Plugin configuration
│       ├── plugin.repos - Plugin repositories
│       ├── plugin.enabled - Plugin enabled
│       ├── plugin.disabled - Plugin disabled
│       ├── power - Power management
│       ├── server.v3 - V3 Server Configuration
│       │   ├── server - Server hostname/IP
│       │   ├── user - Username
│       │   ├── port - Port number
│       │   ├── tls - TLS enabled (true/false)
│       │   ├── topic.prefix - Topic prefix
│       │   ├── updatetime.connected - Update interval when connected (seconds)
│       │   ├── updatetime.idle - Update interval when idle (seconds)
│       │   ├── updatetime.awake - Update interval when awake (seconds)
│       │   ├── updatetime.on - Update interval when on (seconds)
│       │   ├── updatetime.charging - Update interval when charging (seconds)
│       │   ├── updatetime.sendall - Send all data interval (seconds)
│       │   ├── updatetime.keepalive - Keep alive interval (seconds)
│       │   ├── events.legacy_topic - Use legacy event topic
│       │   ├── metrics.include - Include metrics filter
│       │   └── metrics.exclude - Exclude metrics filter
│       ├── system.adc - ADC configuration
│       │   └── factor12v - 12V factor
│       ├── usr - Custom plugin configuration
│       ├── vehicle - Vehicle configuration
│       │   ├── id - Vehicle ID
│       │   ├── name - Vehicle name
│       │   ├── timezone - Timezone
│       │   ├── timezone_region - Timezone region
│       │   ├── stream - Streaming mode
│       │   ├── minsoc - Minimum SOC
│       │   ├── carbits - Car bits
│       │   ├── canwrite - CAN write enabled
│       │   ├── accel.smoothing - Acceleration smoothing
│       │   ├── batpwr.smoothing - Battery power smoothing
│       │   ├── brakelight.enable - Brake light enabled
│       │   ├── brakelight.port - Brake light port
│       │   ├── brakelight.on - Brake light on level
│       │   ├── brakelight.off - Brake light off level
│       │   ├── brakelight.ignftbrk - Ignore foot brake
│       │   ├── brakelight.basepwr - Base power
│       │   ├── 12v.ref - 12V reference voltage
│       │   ├── 12v.alert - 12V alert voltage
│       │   ├── 12v.shutdown - 12V shutdown voltage
│       │   ├── 12v.shutdown_delay - 12V shutdown delay
│       │   ├── 12v.wakeup - 12V wakeup voltage
│       │   └── 12v.wakeup_interval - 12V wakeup interval
│       └── Vehicle-Specific Parameters:
│           ├── xcb - Bolt EV configuration
│           ├── xhi - Hyundai Ioniq vFL configuration
│           ├── xiq - Ioniq 5/EV6 configuration
│           ├── xji - Jaguar I-Pace configuration
│           ├── xkn - Kia Niro / Hyundai Kona EV configuration
│           ├── xme - Maxus EV configuration
│           │   ├── suffsoc - Sufficient SOC
│           │   └── suffrange - Sufficient range
│           ├── xmg - MG EV configuration
│           │   ├── suffsoc - Sufficient SOC
│           │   └── suffrange - Sufficient range
│           ├── xnevo - NIU MQi GT EVO/100 configuration
│           ├── xnl - Nissan Leaf configuration
│           ├── xrt - Renault Twizy configuration
│           ├── xrz2 - Renault Zoe Ph2 configuration
│           ├── xse - Smart ED configuration
│           ├── xsq - SmartEQ configuration
│           │   ├── canwrite - CAN write enabled
│           │   ├── led - LED enabled
│           │   ├── ios_tpms_fix - iOS TPMS fix
│           │   ├── rebootnw - Reboot network
│           │   ├── resettrip - Reset trip
│           │   ├── resettotal - Reset total
│           │   ├── bcvalue - BC value
│           │   ├── full.km - Full km
│           │   ├── climate.system - Climate system
│           │   ├── gps.onoff - GPS on/off
│           │   ├── 12v.charge - 12V charge
│           │   ├── v2.check - V2 check
│           │   ├── modem.net.type - Modem network type
│           │   ├── unlock.warning - Unlock warning
│           │   ├── modem.check - Modem check
│           │   ├── extended.stats - Extended stats
│           │   ├── restart.wakeup - Restart wakeup
│           │   ├── reset.notify - Reset notify
│           │   ├── TPMS_FL - TPMS Front Left ID
│           │   ├── TPMS_FR - TPMS Front Right ID
│           │   ├── TPMS_RL - TPMS Rear Left ID
│           │   ├── TPMS_RR - TPMS Rear Right ID
│           │   ├── tpms.front.pressure - TPMS front pressure
│           │   ├── tpms.rear.pressure - TPMS rear pressure
│           │   ├── tpms.value.warn - TPMS warning value
│           │   └── tpms.value.alert - TPMS alert value
│           ├── xtc - Think City configuration
│           │   ├── canwrite - CAN write enabled
│           │   ├── remote_charge_port - Remote charge port
│           │   ├── cap_act_kwh - Actual capacity kWh
│           │   └── maxrange - Maximum range
│           ├── xtr - Tesla Roadster configuration
│           ├── xva - Volt/Ampera configuration
│           └── xvu - VW e-Up configuration
│               ├── chg_workaround - Charging workaround
│               ├── chg_soclimit - Charge SOC limit (default: 80)
│               ├── chg_climit - Charge current limit
│               ├── cc_onbat - Climate control on battery
│               └── cc_temp - Climate control temperature (default: 20)
│
├── dbc - DBC framework
│   ├── list - List DBC status
│   ├── load - Load DBC file
│   ├── unload - Unload DBC file
│   ├── save - Save DBC file
│   ├── dump - Dump DBC file
│   ├── show - Show DBC file
│   ├── autoload - Autoload DBC files
│   ├── select - Select DBC file for editing
│   ├── deselect - Deselect DBC file for editing
│   ├── set - DBC Set framework
│   │   ├── version - Set version for selected DBC file
│   │   ├── timing - Set bit timing for selected DBC file
│   │   ├── messagemux - Set message mux for selected DBC file
│   │   ├── signalmux - Set signal mux for selected DBC file
│   │   └── signalmuxext - Set extended signal mux link for selected DBC file
│   ├── add - DBC Add framework
│   │   ├── node - Add node for selected DBC file
│   │   ├── message - Add message for selected DBC file
│   │   └── signal - Add signal for selected DBC file
│   ├── remove - DBC Remove framework
│   │   ├── node - Remove node for selected DBC file
│   │   ├── message - Remove message for selected DBC file
│   │   └── signal - Remove signal for selected DBC file
│   └── clear - DBC Clear framework
│       ├── node - Clear all nodes for selected DBC file
│       ├── message - Clear all messages for selected DBC file
│       └── signal - Clear all signals for selected DBC file
│
├── event - EVENT framework
│   ├── status - Show status of event system
│   ├── list - List registered events
│   ├── raise - Raise a textual event
│   └── trace - EVENT trace framework
│       ├── on - Turn event tracing ON
│       └── off - Turn event tracing OFF
│
├── log - LOG framework
│   ├── file - Start logging to specified file
│   ├── open - Start file logging
│   ├── close - Stop file logging
│   ├── status - Show logging status
│   ├── expire - Expire old log files
│   ├── level - Set logging level
│   │   ├── verbose - Log at the VERBOSE level (5)
│   │   ├── debug - Log at the DEBUG level (4)
│   │   ├── info - Log at the INFO level (3)
│   │   ├── warn - Log at the WARN level (2)
│   │   ├── error - Log at the ERROR level (1)
│   │   └── none - No logging (0)
│   └── monitor - Monitor log on this console
│       ├── yes - Monitor log
│       └── no - Don't monitor log
│
├── metrics - METRICS framework
│   ├── list - Show all metrics
│   ├── persist - Show persistent metrics info
│   ├── set - Set the value of a metric
│   ├── get - Get the value of a metric
│   ├── units - List available units
│   └── trace - METRIC trace framework
│       ├── on - Turn metric tracing ON
│       └── off - Turn metric tracing OFF
│
├── module - MODULE framework
│   ├── memory - Show module memory usage
│   ├── leaks - Show module memory changes
│   ├── tasks - Show module task usage
│   │   ├── stack - Show module task usage with stack
│   │   └── data - Output module task stats record
│   ├── fault - Abort fault the module
│   ├── trigger - Trigger framework
│   │   └── twdt - Trigger task watchdog timeout
│   ├── reset - Reset module
│   ├── sleep - Enter sleep mode
│   ├── check - Check heap integrity
│   ├── summary - Show module summary
│   └── factory - MODULE FACTORY framework
│       └── reset - Factory Reset module
│
├── network - NETWORK framework
│   ├── status - Show network status
│   ├── restart - Restart network
│   ├── ping - Ping (ICMP) a hostname/IP address
│   ├── list - List network connections
│   ├── close - Close network connection(s)
│   └── cleanup - Close orphaned network connections
│
├── notify - NOTIFICATION framework
│   ├── status - Show notification status
│   ├── raise - NOTIFICATION raise framework
│   │   ├── text - Raise a textual notification
│   │   ├── command - Raise a command callback notification
│   │   └── errorcode - Raise an error code notification
│   ├── errorcode - NOTIFICATION error code framework
│   │   ├── list - List error codes raised
│   │   └── clear - Clear error code list
│   └── trace - NOTIFICATION trace framework
│       ├── on - Standard notification tracing (text, error & data)
│       ├── all - Full notification tracing (including streams)
│       └── off - Turn notification tracing OFF
│
├── ota - OTA framework
│   ├── status - Show OTA status
│   │   └── nocheck - skip check for available update
│   ├── flash - OTA flash
│   │   ├── vfs - OTA flash vfs
│   │   ├── http - OTA flash http
│   │   └── auto - Automatic regular OTA flash (over web)
│   │       └── force - force update (even if server version older)
│   ├── boot - OTA boot
│   │   ├── factory - Boot from factory image
│   │   ├── ota_0 - Boot from ota_0 image
│   │   └── ota_1 - Boot from ota_1 image
│   ├── erase - OTA erase
│   │   ├── factory - Erase factory image
│   │   ├── ota_0 - Erase ota_0 image
│   │   └── ota_1 - Erase ota_1 image
│   └── copy - OTA copy
│       ├── factory - OTA copy factory <to>
│       │   ├── ota_0 - Copy factory to ota_0 image
│       │   └── ota_1 - Copy factory to ota_1 image
│       ├── ota_0 - OTA copy ota_0 <to>
│       │   ├── factory - Copy ota_0 to factory image
│       │   └── ota_1 - Copy ota_0 to ota_1 image
│       └── ota_1 - OTA copy ota_1 <to>
│           ├── factory - Copy ota_1 to factory image
│           └── ota_0 - Copy ota_1 to ota_0 image
│
├── script - SCRIPT framework
│   ├── run - Run a script
│   ├── reload - Reload javascript framework
│   ├── eval - Eval some javascript code
│   ├── compact - Compact javascript heap
│   └── meminfo - Show heap memory status
│
├── store - STORE framework
│   ├── mount - Mount STORE
│   └── unmount - Unmount STORE
│
├── test - Test framework
│   ├── sleep - Test Deep Sleep
│   ├── sdcard - Test CD CARD
│   ├── javascript - Test Javascript
│   ├── chargen - Character generator
│   ├── echo - Test getchar
│   ├── watchdog - Test task spinning (and watchdog firing)
│   ├── stackoverflow - Test stack overflow detection (crashes)
│   ├── realloc - Test memory re-allocations
│   ├── spiram - Test SPI RAM memory usage
│   ├── strverscmp - Test strverscmp function
│   ├── cantx - Test CAN bus transmission
│   ├── canrx - Test CAN bus reception
│   ├── mkstemp - Test mkstemp function
│   ├── string - Test std::string memory corruption
│   └── commands - List command tree
│
├── time - TIME framework
│   ├── status - Show time status
│   └── set - Set current UTC time
│
└── vfs - Virtual File System framework
    ├── ls - VFS Directory Listing
    ├── rls - VFS Recursive Directory Listing
    ├── cat - VFS Display a file
    ├── head - VFS Display first 20 lines of a file
    ├── stat - VFS Status of a file
    ├── mkdir - VFS Create a directory
    ├── rmdir - VFS Delete a directory
    ├── rm - VFS Delete a file
    ├── mv - VFS Rename a file
    ├── cp - VFS Copy a file
    ├── append - VFS Append a line to a file
    ├── tail - VFS output tail of a file
    ├── df - VFS show disk usage
    └── edit - VFS edit a file
```

## Vehicle and Hardware Commands

```plain
├── vehicle - Vehicle framework
│   ├── module - Set (or clear) vehicle module
│   ├── list - Show list of available vehicle modules
│   ├── status - Show vehicle module status
│   └── aux - Aux battery
│       ├── status - Aux Battery Status
│       └── monitor - Aux Battery Monitor
│           ├── status - Aux Battery Status
│           ├── enable - Enable Aux Monitor
│           └── disable - Disable Aux Monitor
│
├── wakeup - Wake up vehicle
├── homelink - Activate specified homelink button
├── climatecontrol - (De)Activate Climate Control
│   ├── on - Activate Climate Control
│   └── off - Deactivate Climate Control
├── lock - Lock vehicle
├── unlock - Unlock vehicle
├── valet - Activate valet mode
├── unvalet - Deactivate valet mode
│
├── charge - Charging framework
│   ├── mode - Set vehicle charge mode
│   │   ├── standard - Set vehicle standard charge mode
│   │   ├── storage - Set vehicle standard charge mode
│   │   ├── range - Set vehicle standard charge mode
│   │   └── performance - Set vehicle standard charge mode
│   ├── start - Start a vehicle charge
│   ├── stop - Stop a vehicle charge
│   ├── current - Limit charge current
│   └── cooldown - Start a vehicle cooldown
│
├── stat - Show vehicle status
│   └── trip - Show trip status
│
├── bms - BMS framework
│   ├── status - Show BMS status
│   ├── temp - Show BMS temperature status
│   ├── volt - Show BMS voltage status
│   ├── reset - Reset BMS statistics
│   └── alerts - Show BMS alerts
│
├── obdii - OBDII framework
│   ├── can1 - select bus
│   │   └── request - Send OBD2/UDS request, output response
│   │       └── device - Send OBD2/ISOTP request to a device
│   ├── can2 - select bus
│   │   └── request - Send OBD2/UDS request, output response
│   │       └── device - Send OBD2/ISOTP request to a device
│   ├── can3 - select bus
│   │   └── request - Send OBD2/UDS request, output response
│   │       └── device - Send OBD2/ISOTP request to a device
│   └── can4 - select bus
│       └── request - Send OBD2/UDS request, output response
│           └── device - Send OBD2/ISOTP request to a device
```

## CAN Bus Commands

```plain
├── can - CAN framework
│   ├── list - List CAN buses
│   ├── can1 - CANx framework
│   │   ├── start - CAN start framework
│   │   │   ├── listen - Start CAN bus in listen mode
│   │   │   └── active - Start CAN bus in active mode
│   │   ├── stop - Stop CAN bus
│   │   ├── reset - Reset CAN bus
│   │   ├── dbc - CAN dbc framework
│   │   │   ├── attach - Attach a DBC file to a CAN bus
│   │   │   └── detach - Detach the DBC file from a CAN bus
│   │   ├── tx - CAN tx framework
│   │   │   ├── standard - Transmit standard CAN frame
│   │   │   └── extended - Transmit extended CAN frame
│   │   ├── rx - CAN rx framework
│   │   │   ├── standard - Simulate reception of standard CAN frame
│   │   │   └── extended - Simulate reception of extended CAN frame
│   │   ├── testtx - CAN test tx framework
│   │   │   ├── standard - Transmit test standard CAN frames
│   │   │   └── extended - Transmit test extended CAN frames
│   │   ├── status - Show CAN status
│   │   ├── clear - Clear CAN status
│   │   ├── explain - Explain CAN error flags
│   │   ├── viewregisters - view can controller registers
│   │   └── setregister - set can controller register
│   ├── can2 - CANx framework (same subcommands as can1)
│   ├── can3 - CANx framework (same subcommands as can1)
│   └── can4 - CANx framework (same subcommands as can1)
```

## Communication and Connectivity Commands

```plain
├── server - OVMS Server Connection framework
│   ├── v2 - OVMS Server V2 Protocol
│   │   ├── start - Start an OVMS V2 Server Connection
│   │   ├── stop - Stop an OVMS V2 Server Connection
│   │   ├── status - Show OVMS V2 Server connection status
│   │   └── update - Request OVMS V2 Server data update
│   │       ├── all - Transmit all metrics covered by v2 protocol
│   │       └── modified - Transmit modified metrics only
│   └── v3 - OVMS Server V3 Protocol
│       ├── start - Start an OVMS V3 Server Connection
│       ├── stop - Stop an OVMS V3 Server Connection
│       ├── status - Show OVMS V3 Server connection status
│       └── update - Request OVMS V3 Server data update
│           ├── all - Transmit all metrics
│           └── modified - Transmit modified metrics only
│
├── wifi - WIFI framework
│   └── [Various WiFi management commands]
│
├── cellular - CELLULAR MODEM framework
│   └── [Various cellular management commands]
│
├── bt - BLUETOOTH framework
│   └── [Various Bluetooth management commands]
│
└── tls - SSL/TLS Framework
    └── [Various TLS management commands]
```

## Vehicle-Specific Commands

```plain
├── xsq - SmartEQ 453 Gen.4
│   ├── start - Show OBD trip start
│   ├── reset - Show OBD trip total
│   ├── counter - Show vehicle trip counter
│   ├── total - Show vehicle trip total
│   ├── mtdata - Show Maintenance data
│   ├── climate - Show Climate timer data
│   ├── tpmsset - set TPMS dummy value
│   ├── ddt4all - DDT4all Command
│   └── ddt4list - DDT4all Command List
│
├── xrz2 - Renault Zoe Ph2
│   ├── poller - Start, stop, inhibit or resume poller
│   │   ├── start - Start poller in idle mode
│   │   ├── stop - Stop poller
│   │   ├── inhibit - Disable poller for vehicle maintenance
│   │   └── resume - Resume poller for normal operation
│   ├── unlock - Unlock trunk or open chargeport
│   │   ├── trunk - Unlock trunk
│   │   └── chargeport - Open chargeport
│   ├── debug - Debug output of custom functions
│   └── ddt - Modify configuration of ECUs on V-CAN
│       ├── hvac - Modify configuration of HVAC ECU
│       │   └── compressor - Enable or disable compressor
│       │       ├── enable - Enable compressor for normal operation
│       │       └── disable - Disable compressor if there are problems with it
│       └── cluster - Service functions of Instrument cluster
│           └── reset - Reset functions
│               └── service - Reset service reminder
│
└── [Additional vehicle-specific command trees for other vehicles like xvu (VW e-Up), xkn (Kia Niro), xmg (MG EV), etc.]
```

## Additional Component Commands

```plain
├── location - LOCATION framework
│   ├── status - Show location status
│   ├── set - Set the position of a location
│   ├── radius - Set the radius of a location
│   ├── rm - Remove a defined location
│   └── action - Set an action for a location
│       ├── enter - Set an action upon entering a location
│       └── leave - Set an action upon leaving a location
│
├── plugin - PLUGIN framework
│   ├── status - Show status of plugins
│   ├── list - Show list of plugins
│   ├── show - Show plugin details
│   ├── install - Install a plugin
│   ├── remove - Remove a plugin
│   ├── enable - Enable a plugin
│   ├── disable - Disable a plugin
│   ├── update - Update all or a specific plugin
│   └── repo - PLUGIN Repositories
│       ├── list - List repositories
│       ├── install - Install a repository
│       ├── remove - Remove a repository
│       └── refresh - Refresh repository metadata
│
├── poller - OBD polling framework
│   ├── pause - Pause OBD Polling
│   ├── resume - Resume OBD Polling
│   ├── trace - OBD Poller Verbose Logging
│   │   ├── on - Turn verbose logging ON for poller loop
│   │   ├── txrx - Turn verbose logging ON for txrx queuing
│   │   ├── all - Turn verbose logging ON
│   │   ├── off - Turn verbose logging OFF
│   │   └── status - Show status for poller loop logging
│   └── times - OBD Poll-Time Tracing
│       ├── on - Turn on Poll-Time Tracing
│       ├── off - Turn off Poll-Time Tracing
│       ├── status - Show timing status
│       └── reset - Reset Poll-Time Tracing
│
├── power - Power control
├── pushover - pushover notification framework
├── re - RE framework (Reverse Engineering)
├── sd - SD CARD framework
└── tpms - TPMS framework
```
