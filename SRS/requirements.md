# Mars Rover Mission Control - SRS Requirements

## Mission 1: Engineering Notes Analysis

### Functional Requirements (FRs)
* **FR-01 (Command Execution):** The rover shall receive commands from Mission Control and execute valid commands.
* **FR-02 (Telemetry Reporting):** The rover shall report its current position, battery level, temperature, and communication status.
* **FR-03 (Authentication & Authorization):** The system shall verify operator identity and reject invalid or unauthorized commands.
* **FR-04 (Emergency Safety Mode):** The rover shall enter Safe Mode within 3 seconds when
battery temperature exceeds the critical threshold or battery capacity falls below the defined emergency level.
* **FR-05 (Execution Status Feedback):** Mission Control shall receive command execution status updates from the rover.
* **FR-06 (Event & Command Logging):** All commands and critical rover events shall be recorded with a timestamp and operator ID.
### Non-Functional Requirements (NFRs)
* **NFR-01 (Fault Tolerance / Reliability):** The system shall continue operating despite temporary communication interruptions.
* **NFR-02 (Performance / Response Time):** The system shall require authenticated and role-authorized
operators before accepting rover commands.
* **NFR-03 (Scalability):** The system shall support communication with multiple rovers simultaneously.
* **NFR-04 (Security):** The system shall support at least 20 simultaneously
connected rovers.
  
