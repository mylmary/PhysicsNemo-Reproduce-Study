
### DoMINO

DoMINO takes 3D geometries (like STL files) as input instead of relying on heavy mesh downsampling, preserving high accuracy and generalization.

It uses stencil-like query operations combined with learnable layers to capture short- and long-range dependencies for partial differential equations (PDEs).

It can simultaneously predict surface fields (such as pressure and wall shear stress) and volumetric fields (such as velocity) around complex geometries like cars.

DOMINO has been validated on the DrivAerML and Ahmed body datasets, and it delivers massive speedups (over 30x) compared to traditional numerical solvers.


Read the paper: https://arxiv.org/abs/2501.13350
