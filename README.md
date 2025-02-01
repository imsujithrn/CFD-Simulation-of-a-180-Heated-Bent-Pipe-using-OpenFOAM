# CFD Simulation of a 180° Heated Bent Pipe using OpenFOAM

## Overview
This project presents a Computational Fluid Dynamics (CFD) simulation of fluid flow and heat transfer in a 180-degree bent pipe using OpenFOAM. The study focuses on analyzing velocity, pressure, and temperature distributions under specified boundary conditions.

## Features
- 3D simulation of a heated 180° bent pipe
- Meshing using blockMesh
- Reynolds number-based velocity calculations
- Implementation of boundary conditions (U, P, T)
- Post-processing with ParaView

## Repository Structure
```
|-- projectFiles/
|   |-- bentPipe/
|   |   |-- Re100/
|   |   |   |-- q-500/
|   |   |   |   |-- 0/
|   |   |   |   |-- constant/
|   |   |   |   |-- allrun
|   |   |   |   |-- allclean
|   |   |   |   |-- system/
|   |   |   |   |-- results/
|   |   |   |   |-- 100
|   |   |   |   |-- 200
|   |   |   |   |-- 300
|   |   |   |   |-- 400
|   |   |   |   |-- 500
|   |   |   |   |-- 600
|   |   |   |   |-- 700
|   |   |   |   |-- 800
|   |   |   |   |-- 900
|   |   |   |   |-- 1000
|   |   |   |-- q-1000/
|   |   |   |-- q-1500/
|   |   |-- Re5000/
|   |   |-- Re20000/
|   |-- straightPipe/
|   |   |-- (Same structure as bentPipe)
|-- README.md             # Project documentation
```

## Setup Instructions
### Prerequisites
Ensure you have OpenFOAM installed. You can install it using:
```bash
sudo apt update && sudo apt install openfoam
```

### Running the Simulation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/repository-name.git
   cd repository-name
   ```
2. Go to the specific Reynold's Number and go to the specific Heat Flux and Generate the mesh:
   ```bash
   blockMesh
   ```
3. Delete the already simulated values(100-1000) and Set initial conditions and run the solver:
   ```bash
   buoyantSimpleFoam
   ```
4. View results in ParaView:
   ```bash
   paraFoam
   ```

## Results & Analysis
- **Velocity Distribution**: Shows how fluid moves through the bend.
- **Pressure Drop**: Evaluates pressure changes due to curvature.
- **Heat Transfer**: Examines temperature variations along the pipe.

## Future Improvements
- Implement turbulence modeling (RANS, LES)
- Explore different Reynolds numbers and heat flux values
- Compare results with experimental data

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments
- OpenFOAM Community & Documentation
- ParaView for visualization

## Contact
For any inquiries, feel free to reach out at [your email] or open an issue in this repository.

