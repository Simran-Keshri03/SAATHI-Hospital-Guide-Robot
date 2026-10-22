# SAATHI — Hospital Guide Robot

**Raasta bhi, saath bhi.**

SAATHI is a hospital guide robot project designed for navigating a simulated hospital outpatient department (OPD). It explores how a mobile robot can help visitors locate hospital departments, navigate around people and obstacles, and interact through voice-based commands.

The project uses a Webots simulation environment and Python-based controllers to explore perception, navigation, and human–robot interaction.

> **Project status:** Simulation-based project. Features, performance measurements, and hardware deployment should be considered verified only when supported by reproducible tests or demonstrations.

## Overview

Hospitals can be difficult to navigate, especially for first-time visitors. SAATHI explores a robotic assistance system that can guide visitors through a simulated hospital environment.

The repository includes simulation worlds, robot controllers, perception and navigation modules, supporting assets, and tools for running demonstrations and experiments.

## Key Areas

- **Hospital navigation:** Explore route planning between departments in a simulated OPD.
- **Perception:** Integrate camera, depth, and LiDAR data for understanding the robot's surroundings.
- **Path planning:** Explore A* search and obstacle-aware navigation.
- **Human–robot interaction:** Investigate voice commands and gesture-based controls.
- **Multi-floor simulation:** Includes hospital worlds intended to represent different floors and lift-based navigation.
- **Experimentation:** Includes scripts for demonstrations, benchmarking, and generating supporting project media.

Feature availability and runtime requirements depend on the corresponding controller, models, dependencies, and simulation configuration.

## Technology Stack

| Technology | Purpose |
|---|---|
| Python | Robot controller and supporting tools |
| Webots | Robot and environment simulation |
| OpenCV | Image processing |
| NumPy | Numerical operations |
| YOLO-based models | Object and person detection, where configured |
| A* search | Path planning |
| Camera, depth, and LiDAR | Environmental perception |

Additional models and libraries may be required for optional perception, voice, or vision-language features.

## Repository Structure

```text
.
├── controllers/     # Robot controllers and perception/navigation modules
├── docs/            # Project documentation and demo assets
├── motions/         # Motion-related assets
├── ppt/             # Presentation materials
├── protos/          # Webots PROTO definitions
├── textures/        # Simulation textures
├── tools/           # Demo, benchmark, and utility scripts
├── worlds/          # Webots simulation worlds
├── requirements.txt
├── requirements-brain.txt
└── README.md
```

## Prerequisites

Before running the simulation, check the following:

- A compatible installation of [Webots](https://cyberbotics.com/).
- Python compatible with the project's dependencies.
- The required Python packages and any model weights used by the selected controller.
- The repository's world files, controller files, and supporting assets.

Some helper scripts use shell commands intended for macOS or Linux. Windows users may need to adapt those commands to PowerShell.

## Getting Started

### 1. Clone the repository

```bash
git clone <YOUR-REPOSITORY-URL>
cd <REPOSITORY-FOLDER>
```

Replace the placeholders with the URL and directory name for your repository.

### 2. Review dependencies

Inspect the requirements files before installing packages:

```bash
python -m pip install -r requirements.txt
```

Install additional dependencies from `requirements-brain.txt` only when required by the controller or feature you intend to run. Use a virtual environment and check the project's Python and platform requirements first.

### 3. Open the simulation

Open Webots and load a world file from the `worlds/` directory, such as `worlds/opd.wbt`.

Check that the configured robot controller, required assets, and dependencies are available before starting the simulation.

### 4. Explore supporting tools

The `tools/` directory contains scripts for demonstrations, benchmarking, perception-related utilities, and presentation generation.

Review each script's usage and platform requirements before running it. In particular, benchmark output should be treated as experimental evidence only when the setup, parameters, and results can be reproduced.

## Documentation and Demo Assets

The `docs/` directory contains additional project material, including simulation screenshots, animations, and supporting documentation.

For further setup details and experimental methodology, see [docs/DETAILS.md](docs/DETAILS.md), if available in the current checkout.

## Limitations

- The project is primarily organized around a simulated hospital environment; real-world deployment is not implied.
- Results depend on the selected world, controller configuration, model availability, and execution environment.
- Simulation results do not by themselves establish clinical safety or real-hospital effectiveness.
- Voice recognition, visual search, fall detection, and multi-robot coordination should be evaluated independently before relying on them.
- Privacy and safety claims require validation of the actual data-handling and control mechanisms.

## Team

The existing project documentation lists the following team members:

- **Ayush Kumar** — Robot and simulation, vision/AI, shared memory, and Hindi voice.
- **Soumya Raghuwanshi** — Research and hospital-related sources.
- **Simran Kumari Keshri** — Testing and presentation support.

These roles reflect the project's existing documentation and should be updated if responsibilities differ.

## Acknowledgements and Attribution

This repository is based on an existing SAATHI project. Original implementation and third-party assets should be credited in accordance with the upstream repository's license and notices.

**Original source:** [Upstream SAATHI repository](<ADD-ORIGINAL-REPOSITORY-URL>)

Before redistributing or modifying upstream code, review its license and preserve any required copyright notices. Any future modifications should be distinguished clearly from the original implementation.

## License

Check the upstream repository's license and the license files included in this checkout before stating or changing the license for this project.

---

*SAATHI — Raasta bhi, saath bhi.*