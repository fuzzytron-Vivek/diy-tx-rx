# Debugging 
1. since I am writing this after completion of the project , I'll just be giving an over view of the problems I faced .
    - Wiring Problems 
    - Cold Solder joints 
    - Improper grounding 
    - Improper Connection of 5v through regulator 
    - Insights Gained and Solutions applied
    1. ## Wiring Problems 
       1. Bad wires used , changed to solid core cables 
       2. No dedicated 5V and GND line 
    2. ## Cold Solder joints 
       1. was using 60:40 lead soldering tin 
       2. cold joints + rust 
       3. loose connection
       4. Insufficient amount of soldering flux 
    3. ## Improper grounding 
       1. Grounding of the entire circuit on the receiver was **not** done properly which lead to loose grounding and gravity changing how the circuit behaves .
       2. Grounding had shorted on the transmitter end with the voltage regulator VCC line 
    4. ## Improper Connection of 5v
       1. 5v line passed from the DC power straight to the AMS1117 Voltage Regulator and hence it was lowered to  3.3v which was fine for the nrf modules but it was being double regulated into 2.7v by the arduino (which itself needs 5v to function robustly!).
    5. ## Insights Gained and Solutions applied 
       1. Switch to solid core wire 
       2. used Rosin based soldering tin 
       3. Created a dedicated GND channel 
       4. Connected 5v directly to a seperate , dedicated 5v channel.
       5. Resoldered all the signal , data connections 
       6. Wound up MOSI and MISO cables to reduce noise 
       7. Added coupling capacitors to smoothen the supply 
   