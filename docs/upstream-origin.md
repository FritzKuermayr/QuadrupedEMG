# Upstream Origin

This repository consolidates material from the public upstream project below with additional local hardware design files.

- Upstream repository: <https://github.com/lawraa/WristControlledQuadruped>

## Imported From Upstream

- `dynamixel_tools/` -> [`software/dynamixel_tools/`](/Users/Besitzer/Allgemein/Berkeley/Semester 1/Embedded Systems/Quadruped/software/dynamixel_tools)
- `raspi_controller/` -> [`software/raspi_controller/`](/Users/Besitzer/Allgemein/Berkeley/Semester 1/Embedded Systems/Quadruped/software/raspi_controller)
- `wristband_control/` -> [`software/wristband_control/`](/Users/Besitzer/Allgemein/Berkeley/Semester 1/Embedded Systems/Quadruped/software/wristband_control)
- `legacy/` -> [`software/legacy/`](/Users/Besitzer/Allgemein/Berkeley/Semester 1/Embedded Systems/Quadruped/software/legacy)
- `setup_pi.sh` -> [`software/setup_pi.sh`](/Users/Besitzer/Allgemein/Berkeley/Semester 1/Embedded Systems/Quadruped/software/setup_pi.sh)
- `149_final_quadruped.pdf` -> [`docs/project-report/149_final_quadruped.pdf`](/Users/Besitzer/Allgemein/Berkeley/Semester 1/Embedded Systems/Quadruped/docs/project-report/149_final_quadruped.pdf)
- `wristband/model.py` -> [`research/wristband/model.py`](/Users/Besitzer/Allgemein/Berkeley/Semester 1/Embedded Systems/Quadruped/research/wristband/model.py)

## Local Additions

- [`hardware/cad/step/`](/Users/Besitzer/Allgemein/Berkeley/Semester 1/Embedded Systems/Quadruped/hardware/cad/step) contains locally maintained STEP exports for the robot design.

## Excluded During Import

The following categories were intentionally excluded from the upstream import:

- trained model binaries in `gesture_recognition/models/`
- locally collected datasets in `gesture_recognition/training_data/`
- generated PNG analysis outputs
- notebook files and local environment artifacts
- compiled binaries from `dynamixel_tools/`

## Attribution

The upstream Git history includes contributions from:

- Lawrance Chen
- Shou-Jen Chen
- Jayanth Sadhasivan
- Daniel John Ratcliffe Grant Van Camp

This repository preserves and reorganizes that work for a cleaner combined project layout.
