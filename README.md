# UniFi UDM Pro by HTTP and SNMP - v1.4

## Dashboard naming

Dashboard widget titles are intentionally static because Zabbix 8.0 does not expand user macros in widget names:

- `WAN1`
- `WAN2`
- `WAN1 traffic`
- `WAN2 traffic`

Host-level macros `{$WAN1.ISP}` and `{$WAN2.ISP}` remain in item and trigger names. Zabbix expands them in graph legends, Latest data and problem names. Users who want ISP names in widget titles can rename the four widgets manually.

## Required host-level macros

The template defines no macro values. Configure all environment-specific values on the host, including `{$WAN1.ISP}` and `{$WAN2.ISP}`.

## Raw JSON retention

`UniFi Clients JSON`, `UniFi Devices JSON`, `UniFi Sites JSON` and `UDM Pro Statistics JSON` retain history for one day.
