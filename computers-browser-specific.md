
# Specific browser-based information

## Firefox configs

about:config

- Disable WebRTC
  - media.peerconnection.enabled=false
- Toggle browser geolocation
  - Geo.enabled=false
  - Geo.wifi.uri=data:application/json,{"location": {"lat": [latitude I want], "lng": [longitude I want]}, "accuracy": 27000.0}
- Toggle Hardware Acceleration
  - layers.acceleration.force-enabled=true
  - layers.force-active=true

about:support brings up troubleshooting information.
