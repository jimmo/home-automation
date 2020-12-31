## Home Automation

This is a guide for people interested in adding some form of smart lighting and other home automation functionality to their house.

by [Jim Mussared](https://twitter.com/jim_mussared)

Last updated: Dec 2020

Please send PRs or [raise issues](https://github.com/jimmo/home-automation/issues) if you have questions, suggestions, or improvements.

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License][cc-by-sa].

[![CC BY-SA 4.0][cc-by-sa-image]][cc-by-sa]

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-image]: https://licensebuttons.net/l/by-sa/4.0/88x31.png

### Why did you write this

Understanding the trade-offs, limitations, and prerequisites for a given approach requires a fair bit of background knowledge.

### Why do I want Home Automation?

Here are some examples of simple functionality:

* Automatic time-of day dimming

* Add more switches for a room (i.e. a room with multiple entries/exits)

* Group control (e.g. "all off" or "downstairs off")

* Smartphone control

* Voice control

* Integrate lamps with fixed lighting


Some more sophisticated functionality:

* Proximity based control (i.e. turn off when nobody is home)

* Sensor control (i.e. humidity, motion, temperature)

### Just tell me what to do!

It's really hard to give a specific recommendation, but Philips Hue is probably the best all-round option.
* Easy retro-fit to many common light sockets and lamps.
* Good range of first-party accessories (e.g. switch panels, sensors).
* Good app.
* Good third-party ecosystem and developer access.

## Smart Automation

Many "home automation" and "smart lighting" solutions are neither "automatic" or "smart", and don't achieve much more than adding a way to control a light with a smartphone app. With third-party integration (e.g. Google Home) this can be improved, for example to add voice control.

What's missing from many of these systems is a way to define logic in the form of simple conditionals and state management.

## House wiring

Note: This section is here to explain the concepts such that you can understand which systems will work in your house, not so that you can DIY cabling or switches. Modification of any fixed wiring in your house is illegal in Australia. Don't do it! Also, while you're here, make sure you have RCDs fitted on all circuits.

### Two-wire

This is typical for most homes in Australia.

TODO: Diagram

### Three-wire

### Double-switching

### Types of light sockets

#### GU10
These are 240V fittings.

#### MR16
These are 16V fittings, originally intended for halogen bulbs.

#### E27
Also known as "Edison screw".

#### B22
Also known as "bayonet".

## Dimming (and flickering)

### Why do my lights flicker?

## Connectivity

Home automation systems require a way for the various devices to communicate. Due to the difficulty involved in adding more cabling to an existing house, most systems are based on some sort of radio protocol. Some systems will involve a combination of wired and wireless components.

### Wired

For obvious reasons, wired systems have a huge reliability advantage, however unless you're building a new home they are generally not an option.

### WiFi

### Bluetooth Low Energy (BLE)

#### BLE Mesh

### Zigbee

ZigBee is the "other" 2.4GHz wireless standard (alongside WiFi and BLE) and is targeted at low-power, longer-range applications.

A ZigBee "PAN" is comprised of a single "coordinator" which talks to "routers" and "end devices". A vendor will typically sell the coordinator as a "hub", bulbs can be routers or end devices, and switches and sensors are end devices.

### Z-Wave

Z-Wave is similar to ZigBee, but in the 900MHz ISM band instead.

One big drawback with Z-Wave is that different countries use different frequencies, and Z-Wave gear purchased overseas not only won't work with Australian gear, but is technically illegal to use (and may interfere with critical services like distress/medical alarms).

### Other

## Systems

This is an (extremely incomplete) list of systems that are commercially available in Australia.

### Philips Hue

Connectivity: ZigBee

Advantages:
* Very well established, large ecosystem

Drawbacks:
* There's no Hue component that acts as a dimmer for an existing lighting circuit.

### Ikea TRÅDFRI

Connectivity: ZigBee

Advantages:
* [Hackable](https://trmm.net/Ikea/)

Drawbacks:
* 

### SAL Pixie

Connectivity: BLE Mesh

Advantages:
* Works with two-wire home wiring.

Drawbacks:
* 

### Clipsal Iconify

Connectivity: BLE, Wired

Advantages:
* 

Drawbacks:
* Expensive
* Requires three-wire home wiring.

### CBUS

Connectivity: Wired

Advantages:
* 

Drawbacks:
* 

### DIY

I have a lot to say about this :)

## Third-party integration

### Google Home

### Apple HomeKit

### Amazon Alexa

### Home Assistant

### Node-RED

## Security

### Network partitioning
