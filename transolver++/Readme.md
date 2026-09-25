

Transolver++ was developed specifically because the original Transolver starts running into problems when the geometry reaches the million-point scale.

The basic Transolver idea is retained, but Transolver++ changes how the physical states are obtained and how the computation is distributed.

The two major additions are:

Eidetic physical states

Instead of relying on the original global slicing mechanism, Transolver++ introduces a local adaptive mechanism that can extract more distinguishable physical states from massive numbers of mesh points.

Highly parallel computation

The implementation is designed to distribute the workload efficiently across GPUs, allowing the input size to scale with additional GPUs. The authors report million-scale inputs on a single GPU and approximately linear scaling as GPUs are added.

Read the original paper : https://arxiv.org/abs/2502.02414


Download the data from (https://drive.google.com/file/d/1UDGgtOM8UYBFbDe_t2FP7Ij9N5SA3w-g/view).

This reproduction actually gives me a way to look at both models side by side and understand what is actually gained by moving from Transolver to Transolver++.
