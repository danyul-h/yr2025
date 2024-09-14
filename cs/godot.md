> this will cover notes regarding godot

# collisions
* collision layer refers to where the node is *located*
* collision mask refers to where the node *observes*

> [!example]
> Node A -> layer 1 & 2, mask 2
> Node B -> layer 2, no masks
> 
> Node A will detect Node B, as it has a mask matching B's layer
> Node B will not detect anything, as it has no masks
