# Mars Rover Mission Control

## **1. Mission: Analyze the Engineering Note**

### **Mission Brief**

Mars Rover Mission Control is a software system that remotely controls exploration rovers on Mars.

The rover communicates with Mission Control through a communication link. Engineers must be able to:

- **Send movement commands** to the rover.
- **Receive rover location and health data.**
- **Detect communication failures.**
- **Prevent unauthorized commands.**
- **Automatically place the rover into a safe state** when a critical fault is detected.
- **Store mission events** for later investigation.

The system has **limited communication bandwidth** and a communication delay of several minutes. Therefore, commands cannot simply be sent repeatedly without confirmation.

---

## **2. Functional Requirements (FRs)**

Functional requirements describe **what the system must do**.

### **FR-01 — Receive and Execute Commands**

The rover shall receive commands from Mission Control and execute valid commands.

### **FR-02 — Report Rover Position**

The rover shall report its current position to Mission Control.

### **FR-03 — Report Rover Health Data**

The rover shall report its **battery level, temperature, and communication status**.

### **FR-04 — Reject Invalid or Unauthorized Commands**

The system shall reject invalid or unauthorized commands.

### **FR-05 — Enter Safe Mode**

The rover shall enter **Safe Mode, within 3 seconds when battery temperature exceeds the critical threshold or battery capacity falls below the defined emergency level

### **FR-06 — Report Command Execution Status**

Mission Control shall receive command execution status.

### **FR-07 — Record Commands**

All commands shall be recorded with a **timestamp and operator ID**.

### **FR-08 — Record Critical Events**

The system shall record critical rover events for later investigation.

---

## **3. Non-Functional Requirements (NFRs)**

Non-functional requirements describe **how well the system should operate or the constraints under which it operates**.

### **NFR-01 — Communication Interruption Handling**

The system shall continue operating despite temporary communication interruptions.

### **NFR-02 — Command Processing Time**

Command processing should normally complete within **5 seconds** after a command is received by the rover.

### **NFR-03 — Multiple Rover Support**

The system shall support at least **20 simultaneously connected rovers.

### **NFR-04 — Communication Constraints**

The system shall operate with **limited communication bandwidth** and communication delays of several minutes.

---

# **4. Mission Control Sends Change Requests**

The rover engineering team has changed the mission requirements.

---

## **CR-01 — Emergency Safety**

### **Original FR-04**

The rover shall enter Safe Mode when a critical battery or thermal condition is detected.

### **Updated FR-04**

The rover shall enter **Safe Mode within 3 seconds** when battery temperature exceeds the critical threshold or battery capacity falls below the defined emergency level.

### **Explanation**

The updated requirement is more specific and measurable because it defines:

- **Maximum response time:** 3 seconds
- **Battery temperature condition**
- **Battery capacity condition**
- **Required action:** Safe Mode

---

## **CR-02 — Mission Expansion**

### **Original NFR-04**

The system shall support communication with multiple rovers simultaneously.

### **Updated NFR-04**

The system shall support **at least 20 simultaneously connected rovers**.

### **Explanation**

The original requirement was vague because the word **"multiple"** did not specify a particular number.

The updated requirement is **measurable and testable** because it specifies **at least 20 rovers**.

---

## **CR-03 — Security Upgrade**

### **Original NFR-02**

The system shall require authenticated and role-authorized operators before accepting rover commands..

### **Updated NFR-02**

The system shall require **authenticated and role-authorized operators** before accepting rover commands.

### **Explanation**

The updated requirement improves security by requiring both:

1. **Authentication**
2. **Role authorization**

before a rover command can be accepted.

---

# **5. Final Requirements Summary**

## **Functional Requirements**

| **ID** | **Requirement** |
|---|---|
| **FR-01** | Receive and execute valid rover commands |
| **FR-02** | Report current rover position |
| **FR-03** | Report battery level, temperature, and communication status |
| **FR-04** | Reject invalid or unauthorized commands |
| **FR-05** | Enter Safe Mode during critical battery or thermal conditions |
| **FR-06** | Send command execution status to Mission Control |
| **FR-07** | Record commands with timestamp and operator ID |
| **FR-08** | Record critical rover events |

## **Non-Functional Requirements**

| **ID** | **Requirement** |
|---|---|
| **NFR-01** | Continue operating despite temporary communication interruptions |
| **NFR-02** | Normally process commands within 5 seconds |
| **NFR-03** | Support communication with multiple rovers |
| **NFR-04** | Operate with limited bandwidth and communication delays |

---

# **6. Updated Requirements Summary**

| **Change Request** | **Updated Requirement** |
|---|---|
| **CR-01 — Emergency Safety** | Rover enters Safe Mode within **3 seconds** during critical battery/temperature conditions |
| **CR-02 — Mission Expansion** | System supports **at least 20 simultaneously connected rovers** |
| **CR-03 — Security Upgrade** | Commands require **authentication and role authorization** |

---

