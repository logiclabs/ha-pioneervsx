# Home Assistant Custom Component for Pioneer VSX
Older Pioneer VSX amplifier/receivers require extra carriage returns to be sent to the receiver to wake up the CPU before they are ready to accept commands. This custom component fixes that issue.  

## Known models that require wakeup:
* Pioneer VSX-920
* Pioneer VSX-2021


## Installation
1. Copy manifest.json and media_player.py to <config>/custom_components/pioneervsx/ directory
2. Add configuration below to configuration.yaml
3. Restart Home Assistant
4. If required, add a media_player control to the UI

## Configuration.yaml
```yaml
media_player:
  - platform: pioneervsx
    name: "VSX920"
    host: 192.168.1.2
    port: 8102
    enabled_sources_only: true
```

## Extra Features
* enabled_sources_only: 
  Limits the list of sources to only those enabled on the Receiver. (true by default, set to false to see all sources)
  
