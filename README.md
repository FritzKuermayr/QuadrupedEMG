# QuadrupedEMG

QuadrupedEMG is an EECS 149 project focused on EMG- and wrist-controlled locomotion for a quadruped robot platform.

## Team

- Lawrance Chen
- Shou-Jen Chen
- Jayanth Sadhasivan
- Daniel John Ratcliffe Grant Van Camp

## Project Overview

The project combines quadruped locomotion control, Raspberry Pi orchestration, Dynamixel motor tooling, and wristband / EMG-based input experiments.

This repository includes:

- robot control software
- Dynamixel utilities
- wristband and EMG tooling
- CAD assets for the robot hardware
- project documentation and report material

## Repository Layout

```text
QuadrupedEMG/
├── docs/
│   ├── project-report/
│   └── upstream-origin.md
├── hardware/
│   └── cad/
│       ├── README.md
│       └── step/
├── research/
│   └── wristband/
└── software/
    ├── dynamixel_tools/
    ├── legacy/
    ├── raspi_controller/
    ├── wristband_control/
    └── setup_pi.sh
```

## Getting Started

### Raspberry Pi and Dynamixel tools

```bash
cd software
./setup_pi.sh
cd dynamixel_tools
make
```

### Python tooling

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r software/wristband_control/requirements.txt
pip install -r software/wristband_control/gesture_recognition/requirements.txt
```

## Notes

- The active project code is under `software/`.
- `software/legacy/` is kept for historical reference and earlier experiments.
- Hardware CAD files are organized under `hardware/`.
