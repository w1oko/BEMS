# BEMS (Backwoods Energy Management System)
System to monitor and control various aspects of an off-grid electrical system, including charge controllers and inverters.

The vision of this project is to create an extensible platform that be used to remotely monitor and control off-grid electrical systems in a hardware agnostic manner, principally written in Python and designed to run on a Raspberry Pi (to keep the system lightweight in terms of cost and energy consumption).  At a high level, the architecture of this system can be broken down into the following components:

1. Hardware Interface Modules: to interface the system with different types of hardware devices (e.g. charge controllers, inverters, temperature sensors, etc.) from different manufacturers using a common abstraction layer.
2. REST API:  expose hardware devices via a REST API using a common set of methods and properties.
3. MQTT Client: publish status messages to an MQTT server and listen for messages on subscribed MQTT server channels
4. Monitoring & Control Module: provides services to monitor the state of attached hardware devices, send system status updates via MQTT client, listen for and respond to API calls and MQTT messages, send alarm messages when configured threshold conditions are met, and control attached hardware devices based on prefconfigured conditions.
5. UI Module: provides user interface to display system status and accept user commands

The creator of this project has an off-grid photovoltaic (PV) system with a Magnum 4448 inverter, Lithium Ion batteries, and a Midnite Solar Classic charge controller, so until other contributors come forward, the focus of the initial development will be around those devices, even though the vision is for a system that supports multiple hardware devices.  Wherever possible, this project will leverage existing open source material.  The project creator has some Python experience, but is not a professional developer, so contributions to this project are both welcomed and encouraged.

This project interfaces with high voltage (AC and DC) devices manufactured by third-parties, so by using any information or material from this project, you are accepting the risks that go along with that.  If you don't have the appropriate qualifications, experience, and skill necissary to interface with these devices, do not use anything from this project.  Needless to say, there is NO WARRANTY associated with this project or anything derived from this project.   USE AT YOUR OWN RISK!
