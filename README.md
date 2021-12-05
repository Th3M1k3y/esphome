# ESPHome
Here I am posting my different ESPHome configs.

Use them at your own risk!

### [energy-and-gas-meter.yaml](https://github.com/Th3M1k3y/esphome/blob/main/energy-and-gas-meter.yaml)
This is made for monitoring a power meter with a short pulsing output and a gas meter with a pulse in varying length.
Inside the gas meter there is a magnet attached to the rightmost barrel. This means it can stop both right on the edge of the reed switch, or stay on top of it for an extended amount of time. To handle this a binary sensor is used instead of pulse_counter. The filter in pulse_counter is not suited for filtering out noise when the pulse vary in length.
To limit the amount of rows in the database outputs are throttled, otherwise it would make one for each pulse received from the energy meters.

### [sonoff-4ch-pro.yaml](https://github.com/Th3M1k3y/esphome/blob/main/sonoff-4ch-pro.yaml)
This is made for the Sonoff 4CH Pro, but will probably also work on the non pro version.
Each button will toggle the output with the corresponding number on and off.

### [sonoff-pow-r1.yaml](https://github.com/Th3M1k3y/esphome/blob/main/sonoff-pow-r1.yaml)
This is made for the Sonoff POW R1. The energy measurment from this can spike up and down, to limit this a sliding moving average is used on the power output.

[Buy me a coffee! ☕](https://www.buymeacoffee.com/mikeydk)
