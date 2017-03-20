# Fast semantic segmentation of 3D point clouds using a dense CRF with learned parameters
[paper](http://hobbit.acin.tuwien.ac.at/publications/2015wolfpranklvincze_icra.pdf)
### Implementation

### What

- Proposal for semantic segmentation framework for indoor 3D point clouds scenes
-

### How
- The input point cloud is over-segmented and discriminative features are extracted from each segment
- A Random Forest classifier assigns label probabilities to the segments us.
- Output of their Random Forest Classifier is used as unary potentials for a densely interconnected Conditional Random Field
- The pairwise potentials for the CRF are learned from training data.
    - They incorporate the likelihood of different class labels appearing close to each other, depending on the properties of the underlying 3D points such as color and surface orientation.


### Experiments

-
