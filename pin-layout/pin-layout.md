
| Arduino Port | DB-25 Pin | SC function of Pin | standard grbl function | new grbl function |
| --- | --- | --- | --- | --- |
| D1 | x | x | x | x |
| D2 | 2 | Dir X | Step X | Dir X |
| D3 | 4 | Dir Y | Step Y| Dir Y |
| D4 | 6 | Dir Z | Step Z | Dir Z |
| D5 | 3 | Step X | Dir X | Step X |
| D6 | 5 | Step Y | Dir Y  | Step Y |
| D7 | 7 | Step Z | Dir Z | Step Z |
| D8 | x | x | stepper enable | x |
| D9 | 11 | emergency stop | Limit X | Reset/Abort |
| D10 | 12 | reference switch x/y/z | Limit Y | Limit for all? |
| D11 | 13 | reference switch 4th axis | Spindle PWM | x |
| D12 | 17 | n.a. (out) | Limit z | x |
| D13 | 1 | relay 1 | spindle direction | Enable (Spindle PWM) |
| A0 | 10 | tool length sensor (=probe) | Reset/ Abort | Probe |
| A1 | x | x | Feed Hold | x |
| A2 | x | x | Cycle Start | x |
| A3 | x | x | Coolant Enable | x |
| A4 | x | x | x | x |
| A5 | 15 | n.a.(in) | Probe | x |

***

pins to move:

Dir X: D5 -> D2 x  
Dir Y: D6 -> D3 x  
Dir Z: D7 -> D4 x  

Step X: D2 -> D5 x  
Step Y: D3 -> D6 x  
Step Z: D4 -> D7 x  

Reset / Abort: A0 -> D9 x  
Enable (Spindle PWM): D11 -> D13 x  
Probe: A5 -> A0 x  

Limit: set only one limit (Y) on D10 as is x --> (D9, D11/D12 not configured here anymore)  
D12 not set anymore as Limit Z Pin x  
D11 not set as Spindle_direction_bit x  
A5 not defined anymore,  --> set as input x (really needed?)
D11/D12 not defined, --> set as input x
