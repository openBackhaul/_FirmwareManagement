# _FirmwareManagement

UserDemand for automation of the Firmware Management  

## Driver

Replacement of ComarchOSS  

## Scope

_[to be defined]_

See former [concepts](./input/concepts/concepts.md)  

**Detailed Requirements:**  
See [detailed list of requirements](../../issues?q=is%3Aissue%20label%3AHighLevelRequirement) in the issues section.  

## Components

The following components are required for implementing the _FirmwareManagement UserDemand.  

### New Applications and Tools

**p1FirmwareManager (Interface Stream):**  A
Autonomous roll-out of firmware releases.  
Documenting planned activities and their status in TSM.  

**FirmwareManagementGui (Tools Stream):**  
Definition of groups of devices.  
Definition of ticket templates.  
Association of firmware releases with groups of devices and ticket templates.  

### To be updated Applications/Tools

**Gloria (? Stream):**  
Interface to p1FirmwareManager for informing about new firmware approvals.  

### Dependencies on on-going Implementations

**TSM (? Tools):**  
Interface for creating, updating and closing of tickets.  
