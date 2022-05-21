# ROME
RatOS Multi Extruder

A multi extruder to direct extruder solution for RatOS
(Currently limited to 2 Extruders)

## Table of Content
- [Installation](#installation)
    - [Raspberry](#raspberry)
    - [Moonraker](#moonraker)
    - [Klipper](#klipper)
- [Slicer](#slicer)
    - [Native](#native)
    - [Classic](#classic)
 
# Installation

## Raspberry
```
cd ~/
git clone https://github.com/HelgeKeck/rome.git
bash ~/rome/install.sh
```

## Moonraker
```ini
[update_manager rome]
type: git_repo
primary_branch: main
path: ~/rome
origin: https://github.com/HelgeKeck/rome.git
```

## Klipper 
```ini
# ROME
[include rome/config.cfg]
```

# Slicer 

Rome can operate in two different modes.

## Native 

The Rome Native Mode handles the filament loading and unloading on the Wipe tower. Less Slicer configuration needed and more control over the process.

<img src="https://cdn.discordapp.com/attachments/842792223769624605/888344547501940736/20210917_103629.jpg" alt="Carrot Feeder" width="600"/><img src="https://cdn.discordapp.com/attachments/842792223769624605/888344548298874880/20210917_103640.jpg" alt="Carrot Feeder 2" width="600"/>

## Classic

The Rome Classic Mode works exactly like the MMU or ERCF. You are responsible to configure the Slicer proeprly.

```ini
# ROME
[include rome/config.cfg]
```
