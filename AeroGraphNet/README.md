


AeroGraphNet is a graph neural network (GNN) model designed to predict external aerodynamic flow features around car bodies.

Architecture: Built on the MeshGraphNet framework within NVIDIA's physics machine learning ecosystem (such as the PhysicsNeMo Framework and NVIDIA Modulus).

It acts as an AI surrogate model to bypass long, traditional computational fluid dynamics (CFD) compute cycles for external vehicle aerodynamics.


Inputs: Surface mesh files (such as .vtp formats), Reynolds numbers, surface normals, and geometry design parameters.

Outputs: Surface pressure, wall shear stresses, and overall drag coefficients.


Use Cases Ahmed Body: Uses standard simplified geometries parameterized by length, width, height, ground clearance, slant angle, and fillet radius.

Realistic Car Models: Trains on complex configurations (such as DrivAer geometries) to support real-time data-driven design optimization and generative car design.


https://docs.nvidia.com/physicsnemo/latest/physicsnemo/examples/cfd/external_aerodynamics/aero_graph_net/README.html#:~:text=AeroGraphNet%20currently%20supports%20two%20datasets%3A%20Ahmed%20Body%20and%20DrivAerNet.
