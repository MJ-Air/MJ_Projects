# MJ_Projects
class-d audio amplifier – vicharak task

this repo shows the full work of designing a simple class-d amplifier. i used 555 timer for triangle wave, op-amp as comparator (LT1013), mosfet half bridge(IRFZ44N), and lc low pass filter for speaker output.

how it works:

1. triangle wave:
- 555 timer ic in astable mode creates a triangle wave around 300khz.
- r = 1k and 300 ohms (in series for timing)
- c = 0.0015µf and 0.0015µf (for triangle integrator)

2. audio input:
- audio signal is simulated using a 10khz sine wave Frequency with the amplitude of 1V.
- 0.1µf capacitor is connected in series with audio input.

3. comparator (pwm):
- op-amp lt1013 is used as comparator.
- triangle wave goes to op-amp negative input.
- audio signal goes to non inverting input.
- output of op-amp is pwm pulses around 300khz.

4. mosfet stage:
- 2 n-channel mosfets are used (half-bridge).
- high side mosfet drain → 12v
- low side mosfet source → gnd
- output node is between both mosfets.
- gate resistors = 33 ohm for both mosfet gates.

5. speaker filter (lc low pass):
- l = 10µh in series
- c = 0.47µf to gnd after inductor
- speaker + terminal after inductor
- speaker − terminal to gnd

files in this repo:
- ltspice schematic 
- easyeda pcb
- simulation plots
- connection diagram
- screen recording link (added as per task)

note:
i am beginner in using GITHUB, so if there are small mistakes please forgive. this is a simple prototype design to learn and test pwm audio modulation.

