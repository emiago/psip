# psip
Tools for SIP powered by sipgo lib. 
For now not opensource but more to serve as demo for library.

[Download (Linux only for now) psip](https://github.com/emiago/psip/releases/latest/download/psip)

CLI inbound proxy and registrar.
Features:
- [x] Inbound proxy
- [x] Dialog routing
- [ ] Multiple inbound targets and loadbalancing within proxy
- [ ] Inbound/Outbound proxy

```
$>psip -h
Usage: psip [FLAGS]

  -http string
    	Listen HTTP address. env 'PSIP_HTTP_METRICS' (default ":8080")
  -in string
    	Inbound proxy destination. env 'PSIP_INBOUND_TARGET'
  -ip string
    	External IP to use. env 'PSIP_EXTERNAL_ADDR'
  -pprof
    	Full profile
  -tcp string
    	Listen TCP address. env 'PSIP_LISTEN_TCP' (default "127.0.0.1:5060")
  -udp string
    	Listen UDP address. env 'PSIP_LISTEN_UDP' (default "127.0.0.1:5060")

Debuging:
  LOG_LEVEL=string                      Log level for out messaging
  SIP_DEBUG=bool                        SIP trace on debug level

Examples:
psip -in 127.0.0.200:5060 -udp 127.0.0.1:5066 -tcp 127.0.0.1:5066
```
