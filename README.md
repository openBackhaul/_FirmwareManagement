# _FirmwareManagement

UserDemand for automation of the Firmware Management  

## Driver

Replacement of ComarchOSS  

## Scope

The _FirmwareManagement UserDemand is still in its design phase.  
Several [concepts](./input/concepts/concepts.md) have been documented.  
A list of [detailed requirements](../../issues?q=is%3Aissue%20label%3AHighLevelRequirement) can be found in the issues section.  

## Components

The following components are required for implementing the _FirmwareManagement UserDemand.  

### New Applications

- [FirmWareManager](https://github.com/openBackhaul/FirmWareManager)  
  Autonomously manages the firmware on the microwave devices in the network.  
  Documents planned activities and their status in the ticketing system.  

### To be updated Tools

- MDOI, APT, x:akta, netsite or NetExplorer  
  Creates and deletes group definitions for devices  
  Associates target firmware release with group definition  

- MDOI, APT, x:akta, netsite or NetExplorer  
  Categorizes individual devices into group definitions  

- AutomationEngine  
  Provides REST API for creating, updating and deleting tickets in the ticket management system TSM  

### Dependencies on on-going Implementations

- FTP Server  
  Hosts the firmware releases  

- TSM  
  Stores and represents tickets that document deviations from the target firmware  

- API Gateway  
  Demarcation between SDN domain and tool layer  
