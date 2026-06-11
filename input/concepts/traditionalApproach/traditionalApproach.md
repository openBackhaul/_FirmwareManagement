# Traditional Approach

The firmware upgrade capability in a network management system provides centralized orchestration of firmware and operating system updates across distributed network elements. The controller integrates with scheduling mechanisms to execute upgrades during defined maintenance windows, supporting batch execution. Vendor specific requirements are abstracted into a unified workflow, ensuring a vendor agnostic experience for operators. Real time monitoring, progress reporting, and audit logging are embedded into the process, enabling administrators to track completion status, compliance, and performance impact across the network.  

The current Firmware Management is to be replaced by an open source Tool on top of a service based interface (to be provided by the MW SDN domain).  

The following scope is currently discussed between the ToolStream (consumers) and the InterfaceStream (MW SDN domain) of the ComarchOSS Replacement project:  

- Upgrade Path NE software must be upgraded via the mobile backhaul. Software packages will be stored in an external file repository, typically a network file system, organized hierarchically for easy access by the OpenBackhaul system. Repository details and links must be provided during the integration phase.
- Upgrade Process Steps
    1. Download – Software package download to the device can occur during regular operational hours.
    2. Activation – Software package activation must be initiated during a defined maintenance window.
- Pre Download Validation For quick access, NE software must first be downloaded from the centralized repository to the _FirmwareManagement Microservice of the SDN ApplicationLayer, with checksum validation performed before distribution.
- Workflow Characteristics
    1. The upgrade process must appear as a single unified workflow from the end user perspective.
    2. The feature must operate in a vendor agnostic manner.
    3. Software package download can be initiated as either a single request or a bulk request.
    4. Activation, being service affecting, must be executed on a single device at a time.
- Topology Awareness
    1. Activation sequencing must respect microwave device topology.
    2. Ideally, activation should begin from the last/far end device in the topology.
    3. In GNE–RNE setups, RNEs must be upgraded first, followed by the GNE.
- Execution and Monitoring
    1. Completion status and percentage progress for both download and activation must be tracked by the Software Download microservice.
    2. Devices requiring reboot after software download must be explicitly handled.
    3. Notifications, execution details, and trace logs must be captured in a Notification and Log Management module/screen.
    4. Transaction details for both download and activation must be recorded in a Transaction Management module/screen.

**Out of Scope:**  

- Rollback functionality (not supported, as most NEs contain only a single bank for software loading with no standby bank).
- Support for non SDN devices.
- Any enhancements outside the microwave SDN domain integration.
