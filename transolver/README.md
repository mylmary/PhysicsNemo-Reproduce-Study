



<img width="2494" height="696" alt="image" src="https://github.com/user-attachments/assets/1a4f2c85-d301-4bb0-b1aa-5b95451c3447" />



Transolver was integrated into NVIDIA physicsnemo on 10.2024.

Transolver is a Transformer-based neural operator designed to solve partial differential equations (PDEs) on complex, unstructured 3D meshes and general geometries with linear computational complexity.

The main idea is; instead of making the transformer perform attention between every mesh point, Transolver first learns a smaller number of physics-informed states from the mesh. Attention is then performed between these states and the information is mapped back to the original mesh.

The model tries to group points that have similar physical behaviour into the same learned state. 

Simply, it does the following;

 1) Replaces standard quadratic attention (O(N²)) with a linear-complexity mechanism (\(O(N \cdot G + G^2)\)) by clustering mesh points with similar physical behaviors into learnable "slices". 
 2)  Dynamically projects point cloud or mesh data into compact, physics-aware tokens (G slices), performs self-attention across these tokens, and broadcasts the results back to the original massive mesh domain (N points)

The original paper describes this as learning the intrinsic physical states hidden inside the discretized geometry.

Read the original paper: https://arxiv.org/abs/2402.02366

[Link to the dataset: ](https://github.com/thuml/Transolver#:~:text=List%20of%20experiments,Airfoil%2DDesign%2DAirfRANS)



