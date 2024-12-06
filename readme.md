# Behringer WING USB Latency Tests

## Background
The following latency tests were conducted after hearing a significant increase in round trip latency compared to what was reported in Live Professor. After taking latency measurements I discovered that real world round trip latency changed depending the USB Audio in/out selection on the WING.  The interesting part through all of this is that the reported round trip latency in Live Professor remained constant. ***As shown in the table below 32x32 was the best performing.***

## Latency Tests

| Test Name               | Latency (ms) | Notes                                                                                                                                                        |
|-------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Local in to out         | .54          | Measurement ref #1                                                                                                                                           |
| Ch. (no processing)     | 1.29         | Measurement ref #2                                                                                                                                           |
| Ch. (processing)        | 1.29         | Measurement ref #3 - HPF, DESSER, EQ, COMP                                                                                                                   |
| USB 2x2 EXT Insert      | 26.73        | WING channel with processing and external USB insert. USB 2x2 -> Intel Macbook Pro -> Live Professor (direct in to out patch) @64 samples buffer -> USB      |
| USB 8x8 EXT Insert      | 13.40        | Same as previous with USB 8x8                                                                                                                                |
| USB 16x16 EXT Insert    | 11.54        | Same as previous with USB 16x16                                                                                                                              |
| USB 32x32 EXT Insert    | ***9.79***   | Same as previous with USB 32x32                                                                                                                              |
| USB 48x48 EXT Insert    | 9.85         | Same as previous with USB 48x48                                                                                                                              |
| WDante 2x2 EXT Insert | 14.58 | Same as previous but using Dante Card on the wing with DVS set to 2x2 @ 4ms
| M1 Mac Full Chain       | 9.67         | WING channel with processing and external USB insert. USB 48x48 -> M1 Macbook Pro -> Live Professor @64 samples buffer -> Waves Sibilence -> Waves F6 -> USB |
| M1 Mac Direct in to out | 9.64         | Same as previous but direct input to out to bypass plugin chain                                                                                              |

## Notes
- All testing was done in Open Sound Meter
- Measurements can be found in OSM folder
- Measurement rig - MOTU M2 with looped output 2 into input 2 for signal ref