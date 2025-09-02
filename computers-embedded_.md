
Computers are constantly getting faster, cheaper, and more reliable. The reason behind this is because of Moore's Law.

[Moore's Law](https://en.wikipedia.org/wiki/Moore's_law) was from [Gordon Moore](https://en.wikipedia.org/wiki/Gordon_Moore) noticing a predictable trend: the number of transistors that can fit into an integrated circuit doubles about every 2 years.

The implications of this are huge. It means that for the same relative price, every part of a computer can be:

- Twice as fast as it was 2 years ago
- 4 times as fast as 4 years ago
- 8 times as fast as 6 years ago
- 32 times as fast as 10 years ago

This means, without exaggeration, that your average computer is about 1,024 times faster than 20 years ago.

What that means, then, is that the best computers money can buy today will technically be obsolete before they fail. It also means computers get cheaper.

With that in mind, the "[latest and greatest](trends.md)" is a *very* fleeting [social trend](trends.md). The only reason you *need* a new computer is for one of the following:

1. Your [purpose](purpose.md) has expanded that you need a particularly powerful one to do something (most often for playing games or professional media creation).
2. You must add a peripheral and the computer is so old it's no longer compatible, even with a converter/adapter.
3. You have money to burn on ego or image and want something faster.

## Cheap computers

Computers provide [*many* career options](jobs-2_goals-cs.md), and some organizations decided to do something different with them. Instead of selling top-dollar computers, they shaved down as many features as possible to create the cheapest possible computer.

Even though they originally designed these low-spec computers for [teaching](education.md) purposes, they created a *very* affordable general-purpose computer for anyone to use:

- The Raspberry Pi Foundation not-for-profit aims their Raspberry Pi at young people.
  - [The Raspberry Pi](https://www.raspberrypi.org) comes in a variety of forms, but are almost all designed to be as easily accessible as possible.Prices for basic Pis are $35-70, though there are much smaller ones now that run for $4.With respect to hardware, a Raspberry Pi simply needs peripherals (keyboard and screen).
  - There are now units that come with a built-in keyboard, meaning that it only needs a screen to setup.
  - Pis run on [Linux](computers-os-unix.md), so they work with a vast variety of [programming languages](computers-languages.md).
- Ivrea Interaction Design Institute aims their Arduino at giving non-technical students a chance to quickly and affordably prototype what they want.
  - [The Arduino](https://www.arduino.cc/en/Main/Products) is a bit weaker than the Pi, but doesn't have the overhead or complexity of an entire [operating system](computers-os.md), so it's easier to scale than the Pi.
  - Prices for Arduinos range from $10-100.
  - Unlike the Pi's standalone setup, Arduinos need another computer to program them.
  - Programming is in C/C++, or you can get sophisticated and run other languages on it, but it has limitations and not many people do it.
- [PINE64](https://www.pine64.org/) directs their efforts toward affordable, open-source, ready-to-use devices.
  - Like the others, they have single board computers, as well as a clusterboard for [distributed systems](computers-distsys.md).
  - As of right now, they have open-source consumer devices like a laptop, phone, and smart watch.
  - They also have an affordable IP camera and a soldering iron for more specific projects.
  - Pine devices are as-is devices with almost no hardware tinkering required.
- Hardkernal designs a few types of low-end, small devices.
  - ODROID is a tiny circuit board in the spirit of the Raspberry Pi.
  - ODROID-GO has a tiny screen with it and is designed as a portable [emulator console](computers-distsys-vm.md).
- Espressif has [the ESP32](https://www.espressif.com/en/products/socs/esp32), which is a small, cheap, and WiFi-enabled microchip.
- Along with all the above, many vendors sell [very cheap "microcontrollers" for as little as $1](https://jaycarlson.net/microcontrollers/) that allow plenty of opportunities for expanding and scaling a computer's purposes.

Both the Pi and Arduino have GPIO ("general purpose input-output) pins, which creates a modular way to connect peripherals.

Further, old computers and computer parts also have plenty of reusability if you're willing to engage in a little [break-fix](fix.md) and hardware diagnosis:

- Obsolete desktop computers and laptops
- [Printers](engineering-printers.md) and [scanners](computers-ocr.md)
- Old [networking](networks-computer.md) equipment like routers, modems, telephones, and fax machines
- Old [cameras](engineering-camera.md), especially webcams
- While they take more work to fiddle with, most old smartphones are a complete computer with other features like a camera, accelerometer, and GPS.
  - Generally, for reusing, you'll want to focus your efforts on the parts that can be reused the most (which is typically the phone's processor and memory).

No matter what you're poking around with, you *must* be willing to explore [Linux](computers-os-unix.md). The cost of a [Windows](computers-os-windows.md) license for that device makes it cost about as much as a low-tier Windows device, but Windows requires so much processing power and memory [compared to Linux](computers-os-winunix.md) that the computer would run very slowly, if it runs at all.

## Project examples

There are [many potential uses](https://github.com/Phileosopher/toolbox/) for tiny, cheaply-acquired devices.

Make a self-sufficient, fully-functioning [personal computer](computers-hardware.md).

- It will often have to be [Linux](computers-os-unix.md), but you can also make it a Windows thin client to remotely access a separate, more powerful [Windows](computers-os-windows.md) computer.
- While it's a bit clunky, you can even make a smartphone with the right parts (e.g., [OURS project](https://github.com/evanman83/OURS-project/)).

Hobbies:

- Practice [PenTesting](computers-cysec-pentest.md).
- Record and stream [video](engineering-screen.md).
- Use and manage your entire media library in a media server.
- Create a smart TV.
- Play [electronic games](computers-software-gamedev.md).
- Build a [robot](computers-robotics.md).
- Make an FM radio, [FM transmitter](https://github.com/markondej/fm_transmitter) or streaming internet radio station.
- Make a time-lapse camera.
- Create a music box.
- Make a wireless boombox.
- Build an oscilloscope.
- Make an automatic plant waterer.
- Maintain the irrigation system of a [farm](horticulture.md) (e.g., [GardenPi](https://projects-raspberry.com/gardenpi-powered-by-neptune/)).
- Create a soundboard.
- Build an [e-ink home weather display](https://github.com/kimmobrunfeldt/eink-weather-display).

Convenient improvements:

- Make a motion detector or laser tripwire.
- Block ads across your home network ([called a Pi-hole](https://pi-hole.net/)).
- Create a Wi-Fi bridge (e.g., make an old printer wireless).
- Create a Wi-Fi extender.
- Control your smart lights.
- Create a video doorbell.
- Manage your smart home (e.g., locks, climate control).
- Make a weather station with collected weather data (eg., temperature, humidity).
- Monitor air quality.
- Create an altimeter.
- Create a simple display indicator (e.g., meetings, opened, cleaned, etc.).
- Create a voice-activated or gesture-controlled digital assistant.

Personal [risk management](safety-riskmgmt.md):

- Create a motion-activated security video feed.
- Make a backup camera for your auto.
- [Cloud](computers-distsys-cloud.md) synchronize your files.
- Create a [VPN](computers-cysec.md) server or build a local Tor router.
- Make a [firewall](computers-cysec.md).
- Host your private [password manager](encryption.md).
- Host a [DNS server](computers-sofware-webdev.md).
- Make a [facial-recognition or voice-recognition](computers-cysec-authentication.md) lockbox.

[Enterprise](computers-distsys-enterprise.md)-grade:

- Host a [database](database.md).
- Host [virtual machines](computers-distsys-vm.md).
- Train a [machine learning algorithm](computers-ai-ml.md) to detect pretty much anything in particular.
- Host a complete [web server](computers-sofware-webdev.md).
- Keep a private phone server.
- Host your own email.
- Track things with RFID tags.

Enterprise-grade support:

- [Network monitor](https://github.com/geerlingguy/internet-pi)
- Computer resource monitoring
- Keep a redundant [NAS](computers-distsys-cloud.md)
