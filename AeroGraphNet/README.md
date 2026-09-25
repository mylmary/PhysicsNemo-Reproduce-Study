
### AeroGraphNet

AeroGraphNet is a graph neural network (GNN) model designed to predict external aerodynamic flow features around car bodies.

Architecture: Built on the MeshGraphNet framework within NVIDIA's physics machine learning ecosystem (such as the PhysicsNeMo Framework and NVIDIA Modulus).

It acts as an AI surrogate model to bypass long, traditional computational fluid dynamics (CFD) compute cycles for external vehicle aerodynamics.


Inputs: Surface mesh files (such as .vtp formats), Reynolds numbers, surface normals, and geometry design parameters.

Outputs: Surface pressure, wall shear stresses, and overall drag coefficients.


Use Cases 

### Ahmed Body: 

Uses standard simplified geometries parameterized by length, width, height, ground clearance, slant angle, and fillet radius. 

NOTE: The dataset for the Ahmed Body case is not publicly available, you have to reach out to the NVIDIA PhysicsNeMo team to gain individual access.

To train the model, run

python train.py +experiment=ahmed/mgn data.data_dir=/data/ahmed_body/
Make sure to set data.data_dir to a proper location.
Read the paper: https://arxiv.org/abs/2001.11074


### Realistic Car Models: 

Trains on complex configurations (such as DrivAer geometries) to support real-time data-driven design optimization and generative car design.

Read the paper: https://arxiv.org/abs/2403.08055

