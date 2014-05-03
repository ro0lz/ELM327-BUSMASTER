# ELM327-BUSMASTER

## Objective

This project aims to develop a driver for ELM327-compatible devices for using with BUSMASTER software. BUSMASTER is a PC software for monitoring and analyzing communication within data networks in vehicles, such as Controller Area Network (CAN), Local Interconnected Network (LIN), and FlexRay. The software can be downloaded from the following URL.

http://rbei-etas.github.io/busmaster/

Even the BUSMASTER is a commercial grade software which has been released with an open source license by Robert Bosch Engineering and Business Solutions (RBEI) division and maintained by ETAS GmbH, the usage in academic and hobby areas are still limited by the cost of professional hardware. Therefore we would like to overcome such limitation by extending hardware support for ELM327-compatible devices which is the de-facto standard for hobbyists who work with OBD-II interface in their cars. ELM327-compatible interface can be purchased with the price to be less than $100 with various PC interfaces.

https://www.sparkfun.com/products/9555

## Main Use Case
1. When user plugs ELM327 device to OBD-II interface, user can select ELM327 from [Driver Selection] menu. 
  * Driver will initiate communication with ELM327 device and wait for corresponding response.
  * Driver will use mode 1 (current data) to collect data.
2. User associates with obd-ii.dbf for pre-configured database of OBD-II PIDs.
3. For CAN [Transmit] menu, user can select from list of OBD-II PIDs to acquire information from vehicle ECU.
4. When user activates any CAN message display (message window, signal watch, sigal graph), BUSMASTER will show each OBD-II PID response as CAN messages.

## Scope
1. Test with ELM327-compatible devices: Vgate scan 1.5 and 2.1 with Bluetooth interface, ELM327 1.5 USB interface.
2. List of supported ELM327 commands:
  * Engine RPM
  * Calculated Load Value
  * Coolant Temperature
  * Fuel System Status
  * Vehicle Speed
  * Short Term Fuel Trim
  * Long Term Fuel Trim
  * Intake Manifold Pressure
  * Timing Advance
  * Intake Air Temperature
  * Air Flow Rate
  * Absolute Throttle Position
  * Oxygen sensor voltages / associated short term fuel trims
  * Fuel System status
  * Fuel Pressure,
