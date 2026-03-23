**Bicycle Gamelan Automaton**
Solenoids whack bicycle parts to play Reich-style phasing patterns. Tempo knob on A7. Patterns randomly build up and fade every 4 bars.

**Hardware**
Arduino Uno/Nano
9 solenoids → pins 12,11,10,9,8,7,6,5,4 
Potentiometer → A7 (tempo control)
A1 → floating analog input to provide a random seed
Bicycle tubes from framses as sound source. Use round ones only, the overtones are more manageable
External 12V solenoid power supply

**Quick Start**
Wire solenoids (LOW=strike)

Upload gamelan.ino

Board: Arduino Uno | Port: /dev/ttyUSB0

Open Serial Monitor (9600 baud)

Twist A7 pot - slow left (100ms), fast right (300ms)

How It Works
4 parallel 12-step patterns slowly drift in/out of phase

Every 4 bars: Randomly add/remove one note (0-8 total)

Chance system: Mimics Steve Reich's process music

Serial debug: 88=add note, 00=remove note, beat # being modified

Plays like: |x---|--x-|---x-| across 4 staggered tracks

**Tuning**

onTime=25    // Hammer strike length (ms)  
minAim=0     // Min notes (line 13)
maxAim=8     // Max notes (line 14) 
tempo range  // A7 pot: 100ms (slow) → 300ms (fast)



sol9 always HIGH (safety?)

Needs beefy external power for 9 solenoids
