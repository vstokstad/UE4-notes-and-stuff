
#Ue4 chaos cvars
p.Chaos.AccelerationStructureCacheOverlappingLeaves : This caches overlaps (Dynamic tree) that increases time in SwapAccelerationStructures

p.Chaos.AccelerationStructureUseDynamicTree : If you disable the dynamic tree, the Gridhash backup in the static tree will be used. This could potentially be faster for you if you tune the next set of parameters just right:

 

For the backup Gridhash I was talking about (Static objects)

p.aabbtree.DirtyElementGridCellSize

p.aabbtree.DirtyElementMaxGridCellQueryCount

p.aabbtree.DirtyElementMaxPhysicalSizeInCells

p.aabbtree.DirtyElementMaxCellCapacity