# Exploration with task losses for generative modeling

We uniformely sampled a set of points belonging to the surface of a 3D model and used it as a training set. We trained the same generator *(a simple MLP with two hidden layers, of input size 2 and output of size 3)* on the task of generating points belonging to this 2D surface manifold embedded in 3D 
using different task losses:

* A **parametric adversarial divergence** approximating the Jensen Shannon Divergence (JSD) at convergence *(Vanilla GAN)*
* The **Hausdorff distance**
* The **Chamfer distance**
* The **Nearest Neighbor Distance**
* The **L_2 loss** with target corresponding to the Nearest Neighbor in latent space
* The **Sinkhorn divergence**

We compared the results both visually and quantitatively by sampling a point cloud from each of these trained generators and by comparing them to the true 3D models we tried to learn.

For more information about our approach and results, see the [report](https://github.com/AdelNabli/Courses-Udem/blob/master/IFT%206132%20-%20StrucPred%26Opt/Project/IFT_6132___Project_Report.pdf).

## Data

We used the Stanford Bunny and Dragon as the surface manifolds we tried to learn to parametrize with our generator. The data can be downloaded [here](https://www.cc.gatech.edu/projects/large_models/)

## Dependencies

In order to fully run our [notebook](https://nbviewer.jupyter.org/github/AdelNabli/Courses-Udem/blob/master/IFT%206132%20-%20StrucPred%26Opt/Project/IFT%206132%20-%20Project.ipynb), you will need, in addition to **numpy, matplotlib, scikit-learn** and **PyTorch**:

* [Open3D](http://www.open3d.org/docs/release/index.html)
* [Trimesh](https://trimsh.org/index.html)
* [blender](https://www.blender.org/)
* [node js](https://nodejs.org/en/download/package-manager/)
* [Umap](https://umap-learn.readthedocs.io/en/latest/)
* [GeomLoss](http://www.kernel-operations.io/geomloss/)
