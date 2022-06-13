* Adjusting Engine Feature Levels | Unreal Engine Documentation
<https://docs.unrealengine.com/4.26/en-US/TestingAndOptimization/PerformanceAndProfiling/Options/>

* https://youtube.com/watch?v=EbXakIuZPFo&feature=share <https://youtube.com/watch?v=EbXakIuZPFo&feature=share>

* Screen Percentage with Temporal Upsample | Unreal Engine Documentation 
 <https://docs.unrealengine.com/4.26/en-US/RenderingAndGraphics/ScreenPercentage/


* Chaos Physics Scene does not use the World PhysicsCollisionHandler

https://udn.unrealengine.com/s/question/0D54z00007gr2KcCAI/chaos-physics-scene-does-not-use- the-world-physicscollisionhandler

* Implementing Fshader Cache to smooth out hitches.

https://udn.unrealengine.com/s/question/0D54z00007RHJRYCA5/implementing-fshader-cache-to- smooth-out-hitches

* GeometryCache performance and future plans

https://udn.unrealengine.com/s/question/0D54z00007gqoCICAY/geometrycache-performance-and- future-plans

* Setting p.BroadphaseType to 4 hits check in AABBTree PrepareCopyTimeSliced

https://udn.unrealengine.com/s/question/0D54z00007iKhPhCAK/setting-pbroadphasetype-to-4-hits- check-in-aabbtree-preparecopytimesliced

* Streaming Virtual Texturing in Unreal Engine | Unreal Engine 5.0 Documentation https://docs.unrealengine.com/5.0/en-US/streaming-virtual-texturing-in-unreal-engine/

# to test:
* try returning in set scalar parameter if the parameter does not exist.this is used widely and although not in tick everywhere its still a lot to update.
* add LOD to the vechile mesh.
* reduce shadow map size and quality, especilly check what on the vehicles casts shadows and if it can be LODed properly.
* remove forcing dbuffer. decals are a bit expensive.
* find a way to not update niagara! sparks and shit need to fly but not if its not visible and NOT if its on a fucking checkpoint thats not visible. focus on vehicles for now though.
* profile render thread properly WITH RHITread enabled. is this the bottleneck?

* https://youtube.com/watch?v=VTjALz6dhvw&feature=share https://youtube.com/watch?v=VTjALz6dhvw&feature=share

* Using the RebuildHLOD Automation Tool - Unreal Engine / Pipeline & Plugins - Unreal Engine Forums

https://forums.unrealengine.com/t/using-the-rebuildhlod-automation-tool/265073

* Dynamic Resolution | Unreal Engine Documentation https://docs.unrealengine.com/4.27/en-US/RenderingAndGraphics/DynamicResolution/
