
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

## Chrome browser optimization

1. Go to chrome://settings, navigate to Advanced > System
2. Disable the following, then click the relaunch button:
   - Continue running background apps when Google Chrome is closed.
   - Use hardware acceleration when available.
3. Go to chrome://flags and relaunch every time you apply a setting:
   - Disable WebRTC remote-bound event logging
   - Disable WinRT Geolocation Implementation
   - Disable hardware-accelerated video decode
   - Disable hardware-accelerated video encode
   - Enable Override Software Rendering List
   - Enable GPU Rasterization
   - Enable Parallel Downloading
4. Close the browser, then (on Windows) navigate to C:/Program Files/Google/Application/[the first folder with only numbers]
5. Delete the following:
   - Installer (folder)
   - elevation_service.exe
   - Locales/[every .pak file besides your language]
6. (On Windows) navigate to C:/Program Files (x86)/Google and delete the Updates folder.
7. Empty the recycle bin.
