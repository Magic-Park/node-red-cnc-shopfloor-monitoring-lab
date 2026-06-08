# Node-RED CNC Shopfloor Monitoring Lab
Node-RED lab project for CNC machine status monitoring, alarm detection, dashboard visualization, and JSONL log generation.




## Project Overview

This project is a Node-RED based lab for simulating CNC machine status monitoring, alarm detection, dashboard visualization, and JSONL log generation.

The project demonstrates basic OT/ICS monitoring logic using Node-RED flows, dashboard widgets, Function nodes, Switch nodes, and file-based logging.

## Features

- CNC machine status simulation: RUNNING, STOPPED, ALARM
- Dashboard buttons for status control
- Current machine status visualization
- Alarm details panel
- Alarm history table
- JSONL status logging
- JSONL alarm logging
- Duplicate ALARM detection
- Basic event enrichment using Function nodes

## Architecture

```text
Inject / Dashboard Button
→ Build Machine Message
   ├── Prepare Status JSONL Log → write status log
   └── Switch
       ├── RUNNING
       ├── STOPPED
       └── ALARM → Build Alarm Event
           ├── Prepare Alarm JSONL Log
           ├── Alarm Details
           └── Alarm History Table






