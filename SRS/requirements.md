# Mars Rover Mission Control - SRS Requirements

## Mission 1: Engineering Notes Analysis

### Functional Requirements (FRs)
* **FR-01 (Command Execution):** The rover shall receive commands from Mission Control and execute valid commands.
* **FR-02 (Telemetry Reporting):** The rover shall report its current position, battery level, temperature, and communication status.
* **FR-03 (Authentication & Authorization):** The system shall verify operator identity and reject invalid or unauthorized commands.
* **FR-04 (Emergency Safety Mode):** The rover shall enter Safe Mode when a critical battery or thermal condition is detected.
* **FR-05 (Execution Status Feedback):** Mission Control shall receive command execution status updates from the rover.
* **FR-06 (Event & Command Logging):** All commands and critical rover events shall be recorded with a timestamp and operator ID.
### Non-Functional Requirements (NFRs)
* **NFR-01 (Fault Tolerance / Reliability):** The system shall continue operating despite temporary communication interruptions.
* **NFR-02 (Performance / Response Time):** Command processing shall complete within 5 seconds after a command is received by the rover.
* **NFR-03 (Scalability):** The system shall support communication with multiple rovers simultaneously.
* **NFR-04 (Security):** Only authenticated Mission Control operators shall be allowed to issue commands.
  
## Mission 2: Change Requests (CRs) Analysis

### Change Request CR-01 Analysis
* **Impact:** Tightens the original safety requirement by making it precise and measurable. It specifies explicit triggers (battery temperature threshold and emergency capacity level) and adds a strict maximum reaction time window (**within 3 seconds**).
* **System Effect:** Requires continuous monitoring of sensors and an automated interrupt mechanism to guarantee execution within the 3-second constraint.

### Change Request CR-02 Analysis
* **Impact:** Replaces a vague scalability goal ("multiple rovers") with a concrete metric (**at least 20 simultaneously connected rovers**).
* **System Effect:** Requires Mission Control infrastructure to manage multi-threading, concurrency, and adequate bandwidth allocation for up to 20 concurrent telemetry and command links.

### Change Request CR-03 Analysis
* **Impact:** Upgrades the security model from basic **Authentication** (verifying *who* the operator is) to **Role-Based Access Control / Authorization** (verifying *what* permissions that specific operator role has).
* **System Effect:** The system must now maintain operator roles (e.g., Driver, Engineer, Administrator) and evaluate access control lists (ACLs) before executing any command.
