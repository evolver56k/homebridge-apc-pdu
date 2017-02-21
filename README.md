# homebridge-apc-pdu
APC MasterSwitch PDU Plugin for [HomeBridge](https://github.com/nfarina/homebridge) 

# Installation
1. Install homebridge using `npm install -g homebridge`.
2. Install this plugin using `npm install -g git+https://github.com/evolver56k/homebridge-apc-pdu.git`.
3. Update your configuration file. See configuration sample below.


# Removal
1. Stop homebridge.
2. Remove configuration in `config.json`.
3. Start homebridge (the plugin will remove cached accessories automatically).
4. Remove this plugin using `npm remove -g homebridge-apc-pdu`.
5. Restart homebridge.

# Configuration
Edit your `config.json` accordingly. Configuration sample:
```
	"accessories": [{
		"accessory": "APC PDU", 
		"ip": "192.168.0.100", 
		"name": "APC PDU Switches",
		"snmp_community": "private"
	 }]
```

### Advanced Configuration
Design based on AP7900 8-Outlet PDU. If you have a PDU with more than 8 outlets, you will need to modify the two
```for (var i = 1; i < 9; i++) {``` 
loops to account for the number of outlets your unit has.


# Room for improvement
- Poll unit for number of outlets
- Show the amperage reading somewhere
