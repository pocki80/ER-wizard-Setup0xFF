# ER-wizard-Setup0xFF
Wizard for initial 0xFF configuration

A few options and only one click: this EdgeRouter-Wizard transforms a factory-setting EdgeOS to a ready-to-use Router-Konfiguration for 0xFF-Funkfeuer.at!

Fill in your settings (description and explanation within the Wizard UI) and click "Apply". After 45-120 seconds, your router is ready to go without reboot and the wizard will show the logfile from configuration procedure.

## Options
### obligatory
* Public IP for olsr(1) and IPv4
* NodeID

### optional
* hostname
* ssh-port (default: 10)
* username (default: ubnt)

### advanced
* LAN interface/vlan (default: eth0) with dhcp-server off/on (default:on)
* Web interface/vlan (dhcp-client on)
* Portforwardings for Antennas
* additional vlan-tagged OLSR interfaces

## Included Software Components
* olsrd_v1 wizard 0.9.0.3: https://github.com/vchrizz/ER-wizard-OLSRd_V1
* olsrd_v2 wizard 0.14.1-16: https://github.com/pocki80/ER-wizard-OLSRd_V2
* ebtables wizard: https://github.com/pocki80/ER-wizard-ebtables
* WSLE webstatus wizard: https://github.com/pocki80/ER-wizard-0xFF-WSLE

## Prerequisites
* factory settings:
  * username ubnt (password may have been changed already)
  * no bridge created
  * no olsrd_v1 or olsrd_v2 installed
  * no NAT/masquerade rules applied already
  * no name-servers configured already
  * no other address 192.168.1.1/24 assigned to an interface
* Firmware EdgeOS 1.9.0+
