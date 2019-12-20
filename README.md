# Home Assistant Custom Component for Pioneer VSX 920 
Older Pioneer VSX amplifier/receivers require extra carriage returns to be sent to the receiver before they are ready to accept commands.

This custom component fixes that issue.  

## Configuration.yaml
```yaml
  - platform: pioneervsx
    name: "VSX920"
    host: 192.168.1.2
    port: 8102
    enabled_sources_only: true
```

## Extra Features
* enabled_sources_only: 
  Limits the list of sources to only those enabled on the Receiver. (true by default, set to false to see all sources)
