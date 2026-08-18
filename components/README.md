# FirmwareManagement Components

<p align="center">
  <img src="./diagrams/260623 Integration.png" alt="Integration of the FirmWareManager" width="600"/>
</p>

## Roles

- Engineering  
  - documents firmware approvals  
  
- Operation  
  - manages device group definitions and associates firmware versions  
  - analyzes unexpected situations via ticketing system  

- Planning  
  - categorizes individual devices into device groups  

## Components

### New Applications

- [FirmWareManager](https://github.com/openBackhaul/FirmWareManager)  
  Autonomously manages the firmware on the microwave devices in the network  

### To be updated Applications

- [MicroWaveDeviceInventory](https://github.com/openBackhaul/MicroWaveDeviceInventory)  
  Retrieves inventory data from the microwave devices  
- [MicroWaveDeviceGatekeeper](https://github.com/openBackhaul/MicroWaveDeviceGatekeeper)  
  Manages the access to the microwave devices in the network  
  _[if decided to be used]_  

### New Tools

- [_name to be defined_]  
  Graphical user interface for managing the firmware approvals  
- [_name to be defined_]  
  Graphical user interface for managing the device group definitions  

### To be updated Tools

- [_to be chosen from MDOI, APT, x:akta, netsite or NetExplorer_]  
  Categorizes individual devices into group definitions  
- AutomationEngine  
  Mediates between FirmWareManager and TSM  
- TSM  
  Represents on-going activities in the network  
  Represents unexpected situations in the FirmWareManager  

### To be configured Platforms

- FTP Server  
  Hosts the firmware releases  
- API Gateway  
  REST demarcation between SDN domain and tool layer  
- EMP  
  Kafka demarcation between SDN domain and tool layer  
  _[if Kafka is used for error reporting]_  
