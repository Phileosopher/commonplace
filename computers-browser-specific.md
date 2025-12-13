
# Specific browser-based information

## DNS configs

### Quick copy-paste

v4:

94.140.14.14
1.1.1.1
9.9.9.9

v6:

2a10:50c0::ad1:ff
2606:4700:4700::1111
2620:fe::fe

### AdGuard

*Very* effective at blocking ads

Default servers:

94.140.14.14
94.140.15.15
2a10:50c0::ad1:ff
2a10:50c0::ad2:ff

Family servers (blocks more filth):

94.140.14.15
94.140.15.16
2a10:50c0::bad1:ff
2a10:50c0::bad2:ff

### Cloudflare

Highly reliable, since Cloudflare is associated with running most of the internet

1.1.1.1
2606:4700:4700::1111

### Quad9

A great, lesser-known fallback

9.9.9.9
2620:fe::fe

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
