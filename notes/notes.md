
#Ue4 chaos cvars
p.Chaos.AccelerationStructureCacheOverlappingLeaves : This caches overlaps (Dynamic tree) that increases time in SwapAccelerationStructures

p.Chaos.AccelerationStructureUseDynamicTree : If you disable the dynamic tree, the Gridhash backup in the static tree will be used. This could potentially be faster for you if you tune the next set of parameters just right:

 

For the backup Gridhash I was talking about (Static objects)

p.aabbtree.DirtyElementGridCellSize

p.aabbtree.DirtyElementMaxGridCellQueryCount

p.aabbtree.DirtyElementMaxPhysicalSizeInCells

p.aabbtree.DirtyElementMaxCellCapacity

## to test

* try returning in set scalar parameter if the parameter does not exist.this is used widely and although not in tick everywhere its still a lot to update.
* add LOD to the vechile mesh.
* reduce shadow map size and quality, especilly check what on the vehicles casts shadows and if it can be LODed properly.
* remove forcing dbuffer. decals are a bit expensive.
* find a way to not update niagara! sparks and shit need to fly but not if its not visible and NOT if its on a fucking checkpoint thats not visible. focus on vehicles for now though.
* profile render thread properly WITH RHITread enabled. is this the bottleneck?