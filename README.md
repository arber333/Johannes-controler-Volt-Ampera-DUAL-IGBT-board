# Johannes-controler-Volt-Ampera-DUAL-IGBT-board
This is my attempt to parallel both sides of Volt inverter IGBTs into one output for running ACIM or PMSM motors. 

I also designed a control for third power stage that would be driving aux oil pump inside Ampera transmission. Now it will drive AC compressor for my car. I use Lebowski drive since it can run PM mpotors sensorless. I have one Prius gen2 ACcompressor incoming and will open new thread about this.

3.1 version uses inverter chip SN74LS06 that inverts positive signals from Olimex STM32 chip and makes them active low as this inverters driver stage requires. Also i added CAN bus chips for later control options.

3.2 version corrects my assumption that dsPic30f4011 uses serial protocol for communication. This was incorrect. Protocol is TTL and i built transistors to invert signal required to communicate wia serial module.
Also i added simple autothrottle to Lebowski AC compressor controler. Now it is enough to provide 12V signal and compressor will spool up and hold RPM by torque mode.

I added Solidworks 3D printer design for 18mm spacer. If you have access to mill you can make a new lid from the design.

In the actual built I used Microchip MCP6001RT opamp variant which is inverted sensing. I think OPA344 is not a correct opamp. I think you may have a problem in voltage polarity if you use another positive sensing opamp. Also to clarify for isolated op amp i use Si8920 which is marked on board but model is ATTINY. It is just a mistake in using a wrong model for a chip. To supply isolated voltage i use Murata NME0505SC which can withstand short on opamp indefinitely. I am sorry if i caused confusion. I have just used the drawing for so long i forgot about some points.
