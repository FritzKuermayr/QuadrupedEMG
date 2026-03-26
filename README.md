# QuadrupedEMG

QuadrupedEMG combines the original software from the public `WristControlledQuadruped` project with locally maintained CAD assets for the robot hardware.

This repository is intended to be the clean, consolidated project home for the full system:

- robot control software
- EMG / wristband tooling
- Dynamixel motor utilities
- CAD exports for the robot hardware
- project documentation and report material

## Project Background

This project was developed collaboratively. The software foundation in this repository is based on the public upstream repository:

- Upstream source: <https://github.com/lawraa/WristControlledQuadruped>

The original project history shows contributions from:

- Lawrance Chen
- Shou-Jen Chen
- Jayanth Sadhasivan
- Daniel John Ratcliffe Grant Van Camp

This repository reorganizes that work and combines it with additional local hardware assets maintained in the Berkeley Embedded Systems project folder.

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

## What Was Imported

- `software/dynamixel_tools/`: low-level Dynamixel utilities and motor control helpers
- `software/raspi_controller/`: Raspberry Pi control stack for gait execution and high-level command handling
- `software/wristband_control/`: OpenBCI wristband / EMG utilities and gesture-recognition scripts
- `software/legacy/`: earlier controller implementations kept for reference
- `docs/project-report/149_final_quadruped.pdf`: original project report
- `research/wristband/model.py`: experimental wristband modeling notebook export
- `hardware/cad/step/`: local STEP exports for the robot hardware assembly and related parts

## What Was Intentionally Left Out

To keep the repository maintainable, this import does not include generated or environment-specific artifacts from the source project, such as:

- trained model binaries
- local training datasets
- generated plots
- notebook checkpoints
- local macOS metadata files
- compiled Dynamixel helper binaries

## Getting Started

### Raspberry Pi and Dynamixel tools

```bash
cd software
./setup_pi.sh
cd dynamixel_tools
make
```

### Python tooling

Create a virtual environment and install dependencies for the relevant workflow:

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r software/wristband_control/requirements.txt
pip install -r software/wristband_control/gesture_recognition/requirements.txt
```

## Notes

- The active project code is under `software/`.
- The `software/legacy/` folder is preserved for historical reference and earlier experiments.
- Hardware CAD files are separated from software to keep the repository easier to navigate.
- Additional manufacturing or cut files can be added under `hardware/` later without mixing them into the software tree.
