* Lumen Performance Guide for Unreal Engine | Unreal Engine 5.5 Documentation | Epic

Developer Community

<https://dev.epicgames.com/documentation/en-us/unreal-engine/lumen-performance-guide-for-

unreal-engine>

* Lumen Performance Guide for Unreal Engine | Unreal Engine 5.5 Documentation | Epic

Developer Community

<https://dev.epicgames.com/documentation/en-us/unreal-engine/lumen-performance-guide-for-

unreal-engine>

* Using The Low Level Memory Tracker In Unreal Engine | Unreal Engine 5.4 Documentation | Epic Developer Community

<https://dev.epicgames.com/documentation/en-us/unreal-engine/using-the-low-level-memory- tracker-in-unreal-engine>

* Tasm Windows 7|Windows 8|8.1 Full Screen 32bit-64bit Version Single Installer Updated Fullscreen – TechApple

<https://techapple.net/2013/01/tasm-windows-7-windows-8-full-screen-64bit-version-single-installer/ >

* Jenkins, CI and Test-Driven Development | Unreal Engine Community Wiki <https://unrealcommunity.wiki/jenkins-ci-amp-test-driven-development-6912tx0c>

* Posts | Easyperf <https://easyperf.net/notes/>

* Adding Stat Traces (Stat Commands) in Unreal Engine - Tom Looman <https://www.tomlooman.com/unreal-engine-profiling-stat-commands/>

* Unreal Engine Game Optimization on a Budget - Tom Looman <https://www.tomlooman.com/unrealengine-optimization-talk/>

* PSO Precaching for Unreal Engine | Unreal Engine 5.3 Documentation <https://docs.unrealengine.com/5.3/en-US/pso-precaching-for-unreal-engine/>

[ ![Header image](rtr-header.png) ](http://www.realtimerendering.com/blog/)

  * [Blog](http://www.realtimerendering.com/blog/)
  * [Graphics books](books.html)
  * [Intersections](intersections.html)
  * [Portal](portal.html)
  * [Ray tracing](raytracing.html)
  * [Resources](index.html)
  * [USD & glTF](usd_gltf.html)
  * [WebGL](webgl.html)

Ray Tracing Resources Page

![](spacer.gif)  


Last changed: June 6, 2021 

This page gives a grid of intersection routines for various popular objects, pointing to resources in books and on the web. The most comprehensive books on the subject are _[Geometric Tools for Computer Graphics_](https://www.geometrictools.com/Books/Books.html) (GTCG) and _[Real-Time Collision Detection_](http://realtimecollisiondetection.net/) (RTCD); the former is all-encompassing, the latter more approachable and focused. A book focused in large part on object/object intersection tests is the _[Game Physics Cookbook](https://www.packtpub.com/product/game-physics-cookbook/9781787123663)_ (GPC), with [code](https://github.com/gszauer/GamePhysicsCookbook) \- see its [giant grid](https://github.com/gszauer/GamePhysicsCookbook#collision-detection) for what intersections it covers. [Quilez](https://www.iquilezles.org/www/articles/intersectors/intersectors.htm) has a bunch of shader-based ray/object intersectors, including ones (beyond those listed in the table) for the torus, disk, and capsule. 

Guide to source abbreviations: 

  * **3DG** \- _[3D Games: Real-time Rendering and Software Technology_](https://smile.amazon.com/exec/obidos/ASIN/0201619210?tag=realtimerenderin), Alan Watt and Fabio Policarpo, Addison-Wesley, 2001. 
  * **GPC** \- _[Game Physics Cookbook](https://www.packtpub.com/product/game-physics-cookbook/9781787123663)_, by Gabor Szauer, Packt Publishing, March 2017, with [code](https://github.com/gszauer/GamePhysicsCookbook)
  * **GPG** \- _[Game Programming Gems_](https://smile.amazon.com/exec/obidos/ASIN/1584500492?tag=realtimerenderin), ed. Mark DeLoura, Charles River Media, 2000. 
  * **GTCG** \- _[Geometric Tools for Computer Graphics_](https://www.geometrictools.com/Books/Books.html), Philip J. Schneider and David H. Eberly, Morgan Kaufmann Publishers, 2002. Good, comprehensive book on this topic. 
  * **Gems** \- [The _Graphics Gems_ series](http://www.graphicsgems.org). See the book's [website](http://www.graphicsgems.org) for individual book links and code. 
  * **GTweb** \- [Geometric Tools](https://www.geometrictools.com/), Dave Eberly's online computer graphics related software repository. His book _[3D Game Engine Design_](https://www.geometrictools.com/Books/Books.html) also covers these, in a readable format, as well as many other [object/object intersection tests](https://www.geometrictools.com/Samples/Geometrics.html). 
  * **IRT** \- _[An Introduction to Ray Tracing_](https://smile.amazon.com/exec/obidos/ASIN/0122861604?tag=realtimerenderin), ed. Andrew Glassner, Academic Press, 1989. [Free to download](http://www.realtimerendering.com/blog/an-introduction-to-ray-tracing-is-now-free-for-download/). 
  * **JCGT** \- _[The Journal of Computer Graphics Techniques_](http://jcgt.org/). 
  * **jgt** \- _[journal of graphics tools_](https://www.tandfonline.com/toc/ujgt21/current). A partial [code repository](https://github.com/erich666/jgt-code) is available. 
  * **RTCD** \- _[Real-Time Collision Detection_](http://realtimecollisiondetection.net/), by Christer Ericson, Morgan Kaufmann Publishers, 2004. 
  * **RTR4** \- _[Real-Time Rendering, Fourth Edition_](http://www.realtimerendering.com/), by [Tomas Moller](https://cs.lth.se/tomas-akenine-moller/), [Eric Haines](http://erichaines.com), Naty Hoffman, Angelo Pesce, Michał Iwanicki, and Sébastien Hillaire [A.K. Peters/CRC Press](https://www.routledge.com/), 2018. 
  * **SG** \- [Simple Geometry library](http://plib.sourceforge.net/sg/index.html), Steve Baker's vector, matrix, and quaternion manipulation library. 
  * **Shadertoy** \- [Quilez](https://www.iquilezles.org/www/articles/intersectors/intersectors.htm) gives code snippets and shader-based demos, runnable in your browser (best on Chrome). 
  * **TgS** \- [Teikitu gaming System COLLISION](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION), Andrew Aye's object/object intersection/distance and sweep/penetration software (non-commercial use only). 
  * **TVCG** \- [IEEE Transactions on Visualization and Computer Graphics](https://www.computer.org/csdl/journal/tg). 

Individual article references follow after the table. 

## Static Object Intersections

Entries are listed from oldest to newest, so often the _last_ entry is the best. This table covers objects not moving; see the next section for dynamic objects. 

 
**ray**
**plane**
**sphere**
**cylinder**
**cone**
**triangle**
**AABB**
**OBB**
**frustum**
**polyhedron**
 

**ray**
Gems p.304;  
[SG](http://plib.sourceforge.net/sg/index.html);  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
RTCD p.198;  
[SoftSurfer](https://web.archive.org/web/20110716101931/http://www.softsurfer.com/Archive/algorithm_0104/algorithm_0104B.htm): [code](http://geomalgorithms.com/code.html);  
RTR4 p.989
[IRT p.50](http://www.siggraph.org/education/materials/HyperGraph/raytrace/rayplane_intersection.htm),88;  
[SG](http://plib.sourceforge.net/sg/index.html);  
GTCG p.482;  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
RTCD p.175;  
[SoftSurfer](https://web.archive.org/web/20110716101931/http://www.softsurfer.com/Archive/algorithm_0104/algorithm_0104B.htm) ([more](https://web.archive.org/web/20110716101940/http://www.softsurfer.com/Archive/algorithm_0105/algorithm_0105.htm)): [code](http://geomalgorithms.com/code.html);  
[GPC](https://github.com/gszauer/GamePhysicsCookbook);  
[Graphics Codex](http://graphicscodex.com)
[IRT p.39](http://www.siggraph.org/education/materials/HyperGraph/raytrace/rtinter1.htm),91;  
Gems p.388;  
[Held jgt 2(4)](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.49.9172&rep=rep1&type=pdf);  
[GTweb](https://www.geometrictools.com/Samples/Geometrics.html);  
3DG p.16;  
GTCG p.501;  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
RTCD p.127,177;  
[Graphics Codex](http://graphicscodex.com);  
RTR4 p.955;  
[GPC](https://github.com/gszauer/GamePhysicsCookbook);  
[Shadertoy](http://www.iquilezles.org/www/articles/intersectors/intersectors.htm) [(demo)](https://www.shadertoy.com/view/4d2XWV)
IRT p.91;  
Gems IV p.356;  
[Held jgt 2(4)](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.49.9172&rep=rep1&type=pdf);  
[GTweb](https://www.geometrictools.com/Samples/Geometrics.html);  
GTCG p.507;  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
RTCD p.194;  
[Shadertoy](http://www.iquilezles.org/www/articles/intersectors/intersectors.htm) [(demo)](https://www.shadertoy.com/view/4lcSRn)
IRT p.91;  
Gems V p.227;  
[Held jgt 2(4)](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.49.9172&rep=rep1&type=pdf);  
[GTweb doc](https://www.geometrictools.com/Documentation/IntersectionLineCone.pdf);  
GTCG p.512
[Moller-Trumbore jgt 2(1)](https://www.tandfonline.com/doi/abs/10.1080/10867651.1997.10487468): [code](https://fileadmin.cs.lth.se/cs/Personal/Tomas_Akenine-Moller/code/) ([mirror](https://github.com/erich666/jgt-code/tree/master/Volume_02/Number_1/Moller1997a)), [paper draft](http://www.graphics.cornell.edu/pubs/1997/MT97.html);  
[IRT p.53](http://www.siggraph.org/education/materials/HyperGraph/raytrace/raypolygon_intersection.htm),102;  
Gems IV p.24;  
[Held jgt 2(4)](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.49.9172&rep=rep1&type=pdf);  
[GTweb](https://www.geometrictools.com/Samples/Geometrics.html);  
3DG p.17;  
[Moller](https://fileadmin.cs.lth.se/cs/Personal/Tomas_Akenine-Moller/code/) ([mirror](https://github.com/erich666/jgt-code/tree/master/Volume_02/Number_1/Moller1997a));  
GTCG p.485;  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
RTCD p.153,184;  
[Lofstedt jgt 10(2)](https://www.tandfonline.com/doi/abs/10.1080/2151237X.2005.10129195): [code](https://github.com/erich666/jgt-code/tree/master/Volume_10/Number_2/Lofstedt2005), [paper draft](https://fileadmin.cs.lth.se/cs/Personal/Tomas_Akenine-Moller/pubs/ray_tri_survey.pdf)  
[Chirkov jgt 10(3)](https://www.tandfonline.com/doi/abs/10.1080/2151237X.2005.10129201): [code](https://github.com/erich666/jgt-code/tree/master/Volume_10/Number_3/Chirkov2005);  
[Lagae jgt 10(4)](https://www.tandfonline.com/doi/abs/10.1080/2151237X.2005.10129208): [code](https://github.com/erich666/jgt-code/tree/master/Volume_10/Number_4/Lagae2005), [paper draft](https://web.archive.org/web/20120905133158/http://people.cs.kuleuven.be/~ares.lagae/publications/LD05ERQIT/LD05ERQIT.pdf);  
[SoftSurfer](https://web.archive.org/web/20110716101940/http://www.softsurfer.com/Archive/algorithm_0105/algorithm_0105.htm): [code](http://geomalgorithms.com/code.html);  
[Havel TVCG June 2009](https://www.computer.org/csdl/journal/tg/2010/03/ttg2010030434/13rRUyp7tWT );  
[Woop JCGT 2(1)](http://jcgt.org/published/0002/01/05/);  
[Baldwin JCGT 5(3)](http://jcgt.org/published/0005/03/03/);  
[GPC](https://github.com/gszauer/GamePhysicsCookbook);  
[Graphics Codex](http://graphicscodex.com/Sample2-RayTriangleIntersection.pdf);  
RTR4 p.962;  
[Shadertoy](http://www.iquilezles.org/www/articles/intersectors/intersectors.htm) [(demo)](https://www.shadertoy.com/view/MlGcDz)
[IRT p.65](http://www.siggraph.org/education/materials/HyperGraph/raytrace/rtinter3.htm),104;  
Gems p.395;  
[Smits](https://dl.acm.org/doi/abs/10.1145/1198555.1198745);  
3DG p.20;  
[Terdiman (optimized Woo)](http://www.codercorner.com/RayAABB.cpp);  
Schroeder;  
GTCG p.626;  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
RTCD p.179;  
[Mahovsky jgt 9(1)](https://github.com/erich666/jgt-code/tree/master/Volume_09/Number_1/Mahovsky2004);  
[Williams jgt 10(1)](https://github.com/erich666/jgt-code/tree/master/Volume_10/Number_1/Williams2005) ([code](https://dl.acm.org/doi/abs/10.1145/1198555.1198748));  
[Eisemann jgt 12(4)](https://www.cg.cs.tu-bs.de/people/eisemann) ([code](https://web.archive.org/web/20150910070400/https://www.cg.cs.tu-bs.de/media/publications/fast-rayaxis-aligned-bounding-box-overlap-tests-using-ray-slopes.pdf));  
[Shirley 2016](http://psgraphics.blogspot.com/2016/02/new-simple-ray-box-test-from-andrew.html);  
[GPC](https://github.com/gszauer/GamePhysicsCookbook);  
[Chatzianastasiou](https://github.com/constantinides/RAABB);  
[Majercik JCGT 7(3)](http://jcgt.org/published/0007/03/04/);  
RTR4 p.959;  
[Wiche](https://medium.com/@bromanz/another-view-on-the-classic-ray-aabb-intersection-algorithm-for-bvh-traversal-41125138b525);  
[Shadertoy](http://www.iquilezles.org/www/articles/intersectors/intersectors.htm) [(demo)](https://www.shadertoy.com/view/ld23DV)
(IRT p.104;  
Gems II p.247);  
[GTweb](https://www.geometrictools.com/Samples/Geometrics.html);  
[Gomez](https://web.archive.org/web/19991129050752/http://www.gamasutra.com/features/19991018/Gomez_6.htm);  
GTCG p.630;  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
RTCD p.179;  
[Shadertoy](http://www.iquilezles.org/www/articles/intersectors/intersectors.htm) [GPC](https://github.com/gszauer/GamePhysicsCookbook);  
RTR4 p.960;  
[(demo)](https://www.shadertoy.com/view/ld23DV)
(IRT p.104;  
Gems II p.247)
IRT p.104;  
Gems II p.247;  
GTCG p.493;  
[Platis jgt 8(4)](https://github.com/erich666/jgt-code/tree/master/Volume_08/Number_4/Platis2003);  
RTCD p.198;  
[SoftSurfer](https://web.archive.org/web/20110725233122/http://www.softsurfer.com/Archive/algorithm_0111/algorithm_0111.htm): [code](http://geomalgorithms.com/code.html)
**ray**

**plane**
[IRT p.50](http://www.siggraph.org/education/materials/HyperGraph/raytrace/rayplane_intersection.htm),88;  
[SG](http://plib.sourceforge.net/sg/index.html);  
GTCG p.482;  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
RTCD p.175;  
[SoftSurfer](https://web.archive.org/web/20110716101931/http://www.softsurfer.com/Archive/algorithm_0104/algorithm_0104B.htm) ([more](https://web.archive.org/web/20110716101940/http://www.softsurfer.com/Archive/algorithm_0105/algorithm_0105.htm)): [code](http://geomalgorithms.com/code.html);  
[GPC](https://github.com/gszauer/GamePhysicsCookbook);  
[Graphics Codex](http://graphicscodex.com)
[GTweb](https://www.geometrictools.com/Samples/Geometrics.html);  
[SG](http://plib.sourceforge.net/sg/index.html);  
GTCG p.529;  
RTCD p.207;  
[GPC](https://github.com/gszauer/GamePhysicsCookbook)
distance of  
center to plane  
<= radius;  
[GTweb](https://www.geometrictools.com/Samples/Geometrics.html);  
[Gomez](https://web.archive.org/web/19991128214140/http://www.gamasutra.com/features/19991018/Gomez_1.htm);  
GTCG p.548;  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
RTCD p.160,219;  
[GPC](https://github.com/gszauer/GamePhysicsCookbook)
[GTweb](https://www.geometrictools.com/Samples/Geometrics.html);  
GTCG p.551;  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
[GTweb doc](https://www.geometrictools.com/Documentation/IntersectionCylinderPlane.pdf)
GTCG p.563;  
RTCD p.164
Check if all  
vertices are  
on one side;([Moller jgt 2(2)](https://fileadmin.cs.lth.se/cs/Personal/Tomas_Akenine-Moller/code/tritri_tam.pdf));  
GTCG p.534;  
[SoftSurfer](https://web.archive.org/web/20110716101940/http://www.softsurfer.com/Archive/algorithm_0105/algorithm_0105.htm): [code](http://geomalgorithms.com/code.html);  
[GPC](https://github.com/gszauer/GamePhysicsCookbook)
Gems IV p.74;  
GTCG p.634;  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
RTCD p.161,222;  
[GPC](https://github.com/gszauer/GamePhysicsCookbook);  
RTR4 p.970
[GTweb](https://www.geometrictools.com/Samples/Geometrics.html);  
[Gomez](https://web.archive.org/web/19991127082151/http://www.gamasutra.com/features/19991018/Gomez_7.htm);  
GTCG p.635;  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
RTCD p.161;  
[GPC](https://github.com/gszauer/GamePhysicsCookbook);  
RTR4 p.972
 
 
**plane**

**sphere**
[IRT p.39](http://www.siggraph.org/education/materials/HyperGraph/raytrace/rtinter1.htm),91;  
Gems p.388;  
[Held jgt 2(4)](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.49.9172&rep=rep1&type=pdf);  
[GTweb](https://www.geometrictools.com/Samples/Geometrics.html);  
3DG p.16;  
GTCG p.501;  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
RTCD p.127,177;  
[Graphics Codex](http://graphicscodex.com);  
RTR4 p.955;  
[GPC](https://github.com/gszauer/GamePhysicsCookbook);  
[Shadertoy](http://www.iquilezles.org/www/articles/intersectors/intersectors.htm) [(demo)](https://www.shadertoy.com/view/4d2XWV)
distance of  
center to plane  
<= radius;  
[GTweb](https://www.geometrictools.com/Samples/Geometrics.html);  
[Gomez](https://web.archive.org/web/19991128214140/http://www.gamasutra.com/features/19991018/Gomez_1.htm);  
GTCG p.548;  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
RTCD p.160,219;  
[GPC](https://github.com/gszauer/GamePhysicsCookbook)
If radii A+B >=  
center/center distance;  
[Held jgt 2(4)](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.49.9172&rep=rep1&type=pdf);  
[GTweb](https://www.geometrictools.com/Samples/Geometrics.html);  
[Gomez](https://web.archive.org/web/19991128214140/http://www.gamasutra.com/features/19991018/Gomez_1.htm);  
GPG p.390;  
GTCG p.602;  
TgS;  
RTCD p.88,215,223;  
Ellipsoids: [GTweb doc](https://www.geometrictools.com/Documentation/IntersectionOfEllipsoids.pdf);  
[GPC](https://github.com/gszauer/GamePhysicsCookbook);  
RTR4 p.976
If radii A+B >=  
center/axis distance;  
[Held jgt 2(4)](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.49.9172&rep=rep1&type=pdf);  
(GTCG p.602);  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
RTCD p.114
[GTweb](https://www.geometrictools.com/Samples/Geometrics.html);  
[GTweb doc](https://www.geometrictools.com/Documentation/IntersectionSphereCone.pdf);  
(GTCG p.602);  
[Hale](https://blog.squareys.de/sphere-cone-intersection/)
[Held jgt 2(4)](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.49.9172&rep=rep1&type=pdf);  
[GTweb](https://www.geometrictools.com/Samples/Geometrics.html);  
[Karabassi jgt 4(1)](https://www.tandfonline.com/doi/abs/10.1080/10867651.1999.10487499);  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
RTCD p.135,167,226;  
[GPC](https://github.com/gszauer/GamePhysicsCookbook)
Gems p.335;  
[Gomez](https://web.archive.org/web/19991129023147/http://www.gamasutra.com/features/19991018/Gomez_4.htm);  
GTCG p.644;  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
RTCD p.130,165,228;  
Ellipsoid: [GTweb doc](https://www.geometrictools.com/Documentation/IntersectionBoxEllipsoid.pdf);  
[GPC](https://github.com/gszauer/GamePhysicsCookbook);  
RTR4 p.977
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
RTCD p.132,166  
[Larsson](https://www.semanticscholar.org/paper/An-Efficient-Ellipsoid-OBB-Intersection-Test-Larsson/0af6971bb3fc403cdd27e32d81d78497fc57b574?p2df);  
[GPC](https://github.com/gszauer/GamePhysicsCookbook)
[GTweb](https://www.geometrictools.com/Samples/Geometrics.html);  
[Assarsson](http://www.cse.chalmers.se/~uffe/);  
GPG p.433;  
3DG p.302;  
[GPC](https://github.com/gszauer/GamePhysicsCookbook);  
RTR4 p.984
3DG p.462;  
RTCD p.142
**sphere**

**(capped) cylinder**
IRT p.91;  
Gems IV p.356;  
[Held jgt 2(4)](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.49.9172&rep=rep1&type=pdf);  
[GTweb](https://www.geometrictools.com/Samples/Geometrics.html);  
GTCG p.507;  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
RTCD p.194;  
[Shadertoy](http://www.iquilezles.org/www/articles/intersectors/intersectors.htm) [(demo)](https://www.shadertoy.com/view/4lcSRn)
[GTweb](https://www.geometrictools.com/Samples/Geometrics.html);  
GTCG p.551;  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
[GTweb doc](https://www.geometrictools.com/Documentation/IntersectionCylinderPlane.pdf)
If radii A+B >=  
center/axis distance;  
[Held jgt 2(4)](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.49.9172&rep=rep1&type=pdf);  
(GTCG p.602);  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
RTCD p.114
If radii A+B >=  
axis/axis distance;  
[GTweb doc](https://www.geometrictools.com/Documentation/IntersectionOfCylinders.pdf);  
[GTweb doc](https://www.geometrictools.com/Documentation/IntersectionInfiniteCylinders.pdf);  
GTCG p.602,646;  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
RTCD p.114
(GTCG p.602)
[Held jgt 2(4)](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.49.9172&rep=rep1&type=pdf);  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
[GTweb doc](https://www.geometrictools.com/Documentation/IntersectionTriangleCylinder.pdf)
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION)
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION)
GPG p.380
 
**(capped) cylinder**

**(capped) cone**
IRT p.91;  
Gems V p.227;  
[Held jgt 2(4)](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.49.9172&rep=rep1&type=pdf);  
[GTweb doc](https://www.geometrictools.com/Documentation/IntersectionLineCone.pdf);  
GTCG p.512
GTCG p.563;  
RTCD p.164
[GTweb](https://www.geometrictools.com/Samples/Geometrics.html);  
[GTweb doc](https://www.geometrictools.com/Documentation/IntersectionSphereCone.pdf);  
(GTCG p.602);  
[Hale](https://blog.squareys.de/sphere-cone-intersection/)
(GTCG p.602)
(GTCG p.602)
[Held jgt 2(4)](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.49.9172&rep=rep1&type=pdf);  
[GTweb doc](https://www.geometrictools.com/Documentation/IntersectionTriangleCone.pdf);  
GTCG p.583
[GTWeb doc](https://www.geometrictools.com/Documentation/IntersectionBoxCone.pdf)
[GTweb doc](https://www.geometrictools.com/Documentation/IntersectionBoxCone.pdf)
 
 
**(capped) cone**

**triangle (polygon)**
[Moller-Trumbore jgt 2(1)](https://www.tandfonline.com/doi/abs/10.1080/10867651.1997.10487468): [code](https://fileadmin.cs.lth.se/cs/Personal/Tomas_Akenine-Moller/code/) ([mirror](https://github.com/erich666/jgt-code/tree/master/Volume_02/Number_1/Moller1997a)), [paper draft](http://www.graphics.cornell.edu/pubs/1997/MT97.html);  
[IRT p.53](http://www.siggraph.org/education/materials/HyperGraph/raytrace/raypolygon_intersection.htm),102;  
Gems IV p.24;  
[Held jgt 2(4)](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.49.9172&rep=rep1&type=pdf);  
[GTweb](https://www.geometrictools.com/Samples/Geometrics.html);  
3DG p.17;  
[Moller](https://fileadmin.cs.lth.se/cs/Personal/Tomas_Akenine-Moller/code/) ([mirror](https://github.com/erich666/jgt-code/tree/master/Volume_02/Number_1/Moller1997a));  
GTCG p.485;  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
RTCD p.153,184;  
[Lofstedt jgt 10(2)](https://www.tandfonline.com/doi/abs/10.1080/2151237X.2005.10129195): [code](https://github.com/erich666/jgt-code/tree/master/Volume_10/Number_2/Lofstedt2005), [paper draft](https://fileadmin.cs.lth.se/cs/Personal/Tomas_Akenine-Moller/pubs/ray_tri_survey.pdf)  
[Chirkov jgt 10(3)](https://www.tandfonline.com/doi/abs/10.1080/2151237X.2005.10129201): [code](https://github.com/erich666/jgt-code/tree/master/Volume_10/Number_3/Chirkov2005);  
[Lagae jgt 10(4)](https://www.tandfonline.com/doi/abs/10.1080/2151237X.2005.10129208): [code](https://github.com/erich666/jgt-code/tree/master/Volume_10/Number_4/Lagae2005), [paper draft](https://web.archive.org/web/20120905133158/http://people.cs.kuleuven.be/~ares.lagae/publications/LD05ERQIT/LD05ERQIT.pdf);  
[SoftSurfer](https://web.archive.org/web/20110716101940/http://www.softsurfer.com/Archive/algorithm_0105/algorithm_0105.htm): [code](http://geomalgorithms.com/code.html);  
[Havel TVCG June 2009](https://www.computer.org/csdl/journal/tg/2010/03/ttg2010030434/13rRUyp7tWT );  
[Woop JCGT 2(1)](http://jcgt.org/published/0002/01/05/);  
[Baldwin JCGT 5(3)](http://jcgt.org/published/0005/03/03/);  
[GPC](https://github.com/gszauer/GamePhysicsCookbook);  
[Graphics Codex](http://graphicscodex.com/Sample2-RayTriangleIntersection.pdf);  
RTR4 p.962;  
[Shadertoy](http://www.iquilezles.org/www/articles/intersectors/intersectors.htm) [(demo)](https://www.shadertoy.com/view/MlGcDz)
Check if all  
vertices are  
on one side;([Moller jgt 2(2)](https://fileadmin.cs.lth.se/cs/Personal/Tomas_Akenine-Moller/code/tritri_tam.pdf));  
GTCG p.534;  
[SoftSurfer](https://web.archive.org/web/20110716101940/http://www.softsurfer.com/Archive/algorithm_0105/algorithm_0105.htm): [code](http://geomalgorithms.com/code.html);  
[GPC](https://github.com/gszauer/GamePhysicsCookbook)
[Held jgt 2(4)](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.49.9172&rep=rep1&type=pdf);  
[GTweb](https://www.geometrictools.com/Samples/Geometrics.html);  
[Karabassi jgt 4(1)](https://www.tandfonline.com/doi/abs/10.1080/10867651.1999.10487499);  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
RTCD p.135,167,226;  
[GPC](https://github.com/gszauer/GamePhysicsCookbook)
[Held jgt 2(4)](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.49.9172&rep=rep1&type=pdf);  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
[GTweb doc](https://www.geometrictools.com/Documentation/IntersectionTriangleCylinder.pdf)
[Held jgt 2(4)](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.49.9172&rep=rep1&type=pdf);  
[GTweb doc](https://www.geometrictools.com/Documentation/IntersectionTriangleCone.pdf);  
GTCG p.583
[Moller jgt 2(2)](https://fileadmin.cs.lth.se/cs/Personal/Tomas_Akenine-Moller/code/tritri_tam.pdf);  
[Held jgt 2(4)](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.49.9172&rep=rep1&type=pdf);  
[GTweb](https://www.geometrictools.com/Samples/Geometrics.html);  
[Moller](https://fileadmin.cs.lth.se/cs/Personal/Tomas_Akenine-Moller/code/) ([mirror](https://github.com/erich666/jgt-code/tree/master/Volume_02/Number_2/Moller1997b));  
GPG p.393;  
GTCG p.539;  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
RTCD p.155,172;  
[Shen jgt 8(1)](https://www.tandfonline.com/doi/abs/10.1080/10867651.2003.10487579);  
[Guigue jgt 8(1)](https://www.tandfonline.com/doi/abs/10.1080/10867651.2003.10487580): [code](https://github.com/erich666/jgt-code/tree/master/Volume_08/Number_1/Guigue2003);  
[SoftSurfer](https://web.archive.org/web/20110716101940/http://www.softsurfer.com/Archive/algorithm_0105/algorithm_0105.htm): [code](http://geomalgorithms.com/code.html);  
[GTweb doc](https://www.geometrictools.com/Documentation/DynamicCollisionDetection.pdf);  
[GPC](https://github.com/gszauer/GamePhysicsCookbook);  
RTR4 p.972
Gems III p.236;  
Gems V p.375;  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
RTCD p.169;  
[Moller](https://fileadmin.cs.lth.se/cs/Personal/Tomas_Akenine-Moller/code/);  
[GPC](https://github.com/gszauer/GamePhysicsCookbook);  
RTR4 p.974
[GTweb](https://www.geometrictools.com/Samples/Geometrics.html);  
[GTweb doc](https://www.geometrictools.com/Documentation/DynamicCollisionDetection.pdf)  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
[GPC](https://github.com/gszauer/GamePhysicsCookbook)
homogeneous clipping:  
Gems p.84
generalized clipping
**triangle (polygon)**

**axis-aligned bounding box**
[IRT p.65](http://www.siggraph.org/education/materials/HyperGraph/raytrace/rtinter3.htm),104;  
Gems p.395;  
[Smits](https://dl.acm.org/doi/abs/10.1145/1198555.1198745);  
3DG p.20;  
[Terdiman (optimized Woo)](http://www.codercorner.com/RayAABB.cpp);  
Schroeder;  
GTCG p.626;  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
RTCD p.179;  
[Mahovsky jgt 9(1)](https://github.com/erich666/jgt-code/tree/master/Volume_09/Number_1/Mahovsky2004);  
[Williams jgt 10(1)](https://github.com/erich666/jgt-code/tree/master/Volume_10/Number_1/Williams2005) ([code](https://dl.acm.org/doi/abs/10.1145/1198555.1198748));  
[Eisemann jgt 12(4)](https://www.cg.cs.tu-bs.de/people/eisemann) ([code](https://web.archive.org/web/20150910070400/https://www.cg.cs.tu-bs.de/media/publications/fast-rayaxis-aligned-bounding-box-overlap-tests-using-ray-slopes.pdf));  
[Shirley 2016](http://psgraphics.blogspot.com/2016/02/new-simple-ray-box-test-from-andrew.html);  
[GPC](https://github.com/gszauer/GamePhysicsCookbook);  
[Chatzianastasiou](https://github.com/constantinides/RAABB);  
[Majercik JCGT 7(3)](http://jcgt.org/published/0007/03/04/);  
RTR4 p.959;  
[Wiche](https://medium.com/@bromanz/another-view-on-the-classic-ray-aabb-intersection-algorithm-for-bvh-traversal-41125138b525);  
[Shadertoy](http://www.iquilezles.org/www/articles/intersectors/intersectors.htm) [(demo)](https://www.shadertoy.com/view/ld23DV)
Gems IV p.74;  
GTCG p.634;  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
RTCD p.161,222;  
[GPC](https://github.com/gszauer/GamePhysicsCookbook);  
RTR4 p.970
Gems p.335;  
[Gomez](https://web.archive.org/web/19991129023147/http://www.gamasutra.com/features/19991018/Gomez_4.htm);  
GTCG p.644;  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
RTCD p.130,165,228;  
Ellipsoid: [GTweb doc](https://www.geometrictools.com/Documentation/IntersectionBoxEllipsoid.pdf);  
[GPC](https://github.com/gszauer/GamePhysicsCookbook);  
RTR4 p.977
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION)
[GTWeb doc](https://www.geometrictools.com/Documentation/IntersectionBoxCone.pdf)
Gems III p.236;  
Gems V p.375;  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
RTCD p.169;  
[Moller](https://fileadmin.cs.lth.se/cs/Personal/Tomas_Akenine-Moller/code/);  
[GPC](https://github.com/gszauer/GamePhysicsCookbook);  
RTR4 p.974
A.LO<=B.HI &&  
A.HI>=B.LO;  
[Gomez](https://web.archive.org/web/19991129002900/http://www.gamasutra.com/features/19991018/Gomez_3.htm);  
3DG p.445;  
GTCG p.637;  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
RTCD p.79,230;  
[GPC](https://github.com/gszauer/GamePhysicsCookbook);  
RTR4 p.978
(Gems V p.378;  
[GTweb](https://www.geometrictools.com/Samples/Geometrics.html);  
[Gomez](https://web.archive.org/web/19991129035017/http://www.gamasutra.com/features/19991018/Gomez_5.htm);  
GTCG p.639);  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
[GPC](https://github.com/gszauer/GamePhysicsCookbook)
(Gems IV p.83);  
(Gems V p.378);  
([GTweb](https://www.geometrictools.com/Samples/Geometrics.html));  
[Assarsson](http://www.cse.chalmers.se/~uffe/);  
3DG p. 302;(  
GTCG p.624);  
[GPC](https://github.com/gszauer/GamePhysicsCookbook);  
RTR4 p.986
Gems IV p.74;  
Gems V p.378
**axis-aligned bounding box**

**oriented bounding box**
(IRT p.104;  
Gems II p.247);  
[GTweb](https://www.geometrictools.com/Samples/Geometrics.html);  
[Gomez](https://web.archive.org/web/19991129050752/http://www.gamasutra.com/features/19991018/Gomez_6.htm);  
GTCG p.630;  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
RTCD p.179;  
[Shadertoy](http://www.iquilezles.org/www/articles/intersectors/intersectors.htm) [GPC](https://github.com/gszauer/GamePhysicsCookbook);  
RTR4 p.960;  
[(demo)](https://www.shadertoy.com/view/ld23DV)
[GTweb](https://www.geometrictools.com/Samples/Geometrics.html);  
[Gomez](https://web.archive.org/web/19991127082151/http://www.gamasutra.com/features/19991018/Gomez_7.htm);  
GTCG p.635;  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
RTCD p.161;  
[GPC](https://github.com/gszauer/GamePhysicsCookbook);  
RTR4 p.972
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
RTCD p.132,166  
[Larsson](https://www.semanticscholar.org/paper/An-Efficient-Ellipsoid-OBB-Intersection-Test-Larsson/0af6971bb3fc403cdd27e32d81d78497fc57b574?p2df);  
[GPC](https://github.com/gszauer/GamePhysicsCookbook)
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION)
[GTweb doc](https://www.geometrictools.com/Documentation/IntersectionBoxCone.pdf)
[GTweb](https://www.geometrictools.com/Samples/Geometrics.html);  
[GTweb doc](https://www.geometrictools.com/Documentation/DynamicCollisionDetection.pdf)  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
[GPC](https://github.com/gszauer/GamePhysicsCookbook)
(Gems V p.378;  
[GTweb](https://www.geometrictools.com/Samples/Geometrics.html);  
[Gomez](https://web.archive.org/web/19991129035017/http://www.gamasutra.com/features/19991018/Gomez_5.htm);  
GTCG p.639);  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
[GPC](https://github.com/gszauer/GamePhysicsCookbook)
[GTweb](https://www.geometrictools.com/Samples/Geometrics.html);  
[Gomez](https://web.archive.org/web/19991129035017/http://www.gamasutra.com/features/19991018/Gomez_5.htm);  
3DG p.449;  
GTCG p.639;  
[TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION);  
RTCD p.101;  
[GTweb doc](https://www.geometrictools.com/Documentation/DynamicCollisionDetection.pdf);  
[GPC](https://github.com/gszauer/GamePhysicsCookbook);  
RTR4 p.980
[GTweb](https://www.geometrictools.com/Samples/Geometrics.html);  
[GTweb doc](https://www.geometrictools.com/Documentation/IntersectionBox3Frustum3.pdf);  
[Assarsson](http://www.cse.chalmers.se/~uffe/);  
GTCG p.624;  
[GPC](https://github.com/gszauer/GamePhysicsCookbook)
(Gems IV p.83)
**oriented bounding box**

**viewing frustum**
(IRT p.104;  
Gems II p.247)
 
[GTweb](https://www.geometrictools.com/Samples/Geometrics.html);  
[Assarsson](http://www.cse.chalmers.se/~uffe/);  
GPG p.433;  
3DG p.302;  
[GPC](https://github.com/gszauer/GamePhysicsCookbook);  
RTR4 p.984
GPG p.380
 
homogeneous clipping:  
Gems p.84
(Gems IV p.83);  
(Gems V p.378);  
([GTweb](https://www.geometrictools.com/Samples/Geometrics.html));  
[Assarsson](http://www.cse.chalmers.se/~uffe/);  
3DG p. 302;(  
GTCG p.624);  
[GPC](https://github.com/gszauer/GamePhysicsCookbook);  
RTR4 p.986
[GTweb](https://www.geometrictools.com/Samples/Geometrics.html);  
[GTweb doc](https://www.geometrictools.com/Documentation/IntersectionBox3Frustum3.pdf);  
[Assarsson](http://www.cse.chalmers.se/~uffe/);  
GTCG p.624;  
[GPC](https://github.com/gszauer/GamePhysicsCookbook)
(Gems IV p.83)
(Gems IV p.83)
**viewing frustum**

**convex polyhedron**
IRT p.104;  
Gems II p.247;  
GTCG p.493;  
[Platis jgt 8(4)](https://github.com/erich666/jgt-code/tree/master/Volume_08/Number_4/Platis2003);  
RTCD p.198;  
[SoftSurfer](https://web.archive.org/web/20110725233122/http://www.softsurfer.com/Archive/algorithm_0111/algorithm_0111.htm): [code](http://geomalgorithms.com/code.html)
 
3DG p.462;  
RTCD p.142
 
 
generalized clipping
Gems IV p.74;  
Gems V p.378
(Gems IV p.83)
(Gems IV p.83)
Gems IV p.83;  
3DG p.453;(  
[GTweb doc](https://www.geometrictools.com/Documentation/MethodOfSeparatingAxes.pdf);  
GTCG p.726;  
[Ganovelli jgt 7(2)](http://vcg.isti.cnr.it/Publications/2003/GPR03/fast_tetrahedron_tetrahedron_overlap_algorithm.pdf);  
RTCD p.383,399,410;  
[Gregorius 2013](http://twvideo01.ubm-us.net/o1/vault/gdc2013/slides/822403Gregorius_Dirk_TheSeparatingAxisTest.pdf)
**convex polyhedron**

 
**ray**
**plane**
**sphere**
**cylinder**
**cone**
**triangle**
**AABB**
**OBB**
**frustum**
**polyhedron**
 

References are listed in historical order, so it's usually best to look at the last reference first. References in parentheses indicate algorithms that will work, but are not optimized for the particular primitives. Note that all AABB algorithms can also be used for OBB intersections (simply transform the other primitive to the OBB's space), so we do not list these in the table. 

## Dynamic Object Intersections

These are intersections in which the objects are moving relative to one another. Linear motion (only) is assumed; there is research on rotational motion collision detection, not covered here. The [TgS](https://github.com/teikitu/teikitu_release/tree/master/teikitu/src/TgS%20COLLISION) collision system (non-commercial use only) has many methods in this area, and the book _Real-Time Collision Detection_ covers the subject in some depth. Other relevant presentations can be found on the [Essential Math for Games Programmers](https://www.essentialmath.com/tutorial.htm) site. One principle is that even if both objects are moving, only one has to be considered moving. That is, one object's movement vector can be subtracted from both objects, leaving one object at rest. Another principle is to perform a [Minkowski sum](https://algorist.com/problems/Minkowski_Sum.html) (or [Minkowski difference](http://twvideo01.ubm-us.net/o1/vault/gdc2013/slides/822403Gregorius_Dirk_TheSeparatingAxisTest.pdf)) of the moving sphere with the other object, essentially shrinking the moving sphere to a ray. A set of static intersection tests are used in many of these tests, so look in the table above for these. The tests below are categorized as _boolean_, i.e., whether the objects intersect at all, or _location_, where the actual intersection location where the two moving objects first hit is formed. _(Please let me know if you have simple ways of making a given boolean test into a location test.)_

**Ray/Moving Sphere:** _(location)_ Form a cylinder between the two spheres, intersect the two spheres and cylinder with the ray. See [Gregorius 2015](http://media.steampowered.com/apps/valve/2015/DirkGregorius_Contacts.pdf).  
**Ray/Moving Triangle:** _(boolean)_ If each triangle is entirely on one side of the plane formed by the other triangle, form the polyhedron between the two triangles. The connecting faces are formed by all the combinations of an edge on one triangle and a vertex on the other. Discard any separating planes formed (i.e., use only planes in which both triangles are on the same side of the plane). Shoot the ray against it using [ray/polyhedron testing](http://www.realtimerendering.com/intersections.html#II247). _(Short of splitting the triangles into two parts each and forming volumes amongst these, is there an elegant way to perform this operation when one triangle's plane splits the other triangle?)_  
**Ray/Moving AABB:** _(boolean)_ Form a [shaft](http://www.realtimerendering.com/downloads/shaft.zip) ([paper](http://www.erichaines.com/ShaftCulling.pdf)) between the beginning and ending position of the AABB and shoot the ray against it using [ray/polyhedron testing](http://www.realtimerendering.com/intersections.html#II247). See [RTR4, free Collision Detection chapter](http://www.realtimerendering.com/Real-Time_Rendering_4th-Collision_Detection.pdf).  
**Ray/Moving OBB:** _(boolean)_ An inelegant way is to form all combinations of edge/vertex pairs and form planes to bound the OBBs (see Ray/Moving triangle, above). **Ray/Moving Polyhedron:** Take the convex hull of each polyhedron and then the convex hull of both of these. [Glassner](http://ieeexplore.ieee.org/xpl/articleDetails.jsp?arnumber=504) is the earliest reference I know. See [Gregorius 2015](http://media.steampowered.com/apps/valve/2015/DirkGregorius_Contacts.pdf) for a modern treatment. 

**Plane/Moving Sphere:** _(location)_ Transform the problem into changing the plane into a thick slab, of thickness equal to the radius of the sphere. Change the sphere's path into a line segment. Perform slab/line segment intersection, i.e., ray/plane intersection for the two sides of the slab. See [Gomez](https://web.archive.org/web/19991128214140/http://www.gamasutra.com/features/19991018/Gomez_1.htm); and [RTR4, free Collision Detection chapter](http://www.realtimerendering.com/Real-Time_Rendering_4th-Collision_Detection.pdf)..  
**Plane/Moving AABB:** _(location)_ If the plane's normal is along one of the primary axes, e.g., it is [0 1 0], [0 0 -1], etc., then turn the problem into slab/line segment intersection, similar to plane/moving sphere above. That is, take the thickness of the AABB and make the plane this thick.  


The general principal of intersecting a moving sphere against an object is to simplify thinking about the problem by making the sphere into a line segment between its center's start and end locations, while "adding" this sphere (a [Minkowski sum](https://algorist.com/problems/Minkowski_Sum.html)) to the other object.  
**Moving Sphere/Sphere:** _(location)_ Add the radius of the moving sphere to the static sphere, and treat the moving sphere as a ray. Use this ray to perform ray/sphere intersection. See [Gomez](https://web.archive.org/web/19991128214140/http://www.gamasutra.com/features/19991018/Gomez_1.htm) and [RTR4, free Collision Detection chapter](http://www.realtimerendering.com/Real-Time_Rendering_4th-Collision_Detection.pdf)..  
**Moving Sphere/Triangle:** _(location)_ Similar to above, turn the sphere into a ray. The triangle turns into a solid defined by a set of spheres at the vertices, cylinders along the edges, and a slab for the interior of the triangle. See [Rouwe's article and code](https://github.com/jrouwe/SweptEllipsoid); [GTWeb doc](https://www.geometrictools.com/Documentation/IntersectionMovingSphereTriangle.pdf); [RTR4, free Collision Detection chapter](http://www.realtimerendering.com/Real-Time_Rendering_4th-Collision_Detection.pdf).; [Gregorius 2012](http://twvideo01.ubm-us.net/o1/vault/gdc2013/slides/822403Gregorius_Dirk_TheSeparatingAxisTest.pdf).  
**Moving Sphere/AABB:** GTWeb has [a more detailed document on this topic. _(boolean)_ A conservative test (i.e., no false misses, but can give false hits when there actually is no overlap) is to make the AABB move, so forming a [shaft](http://www.realtimerendering.com/downloads/shaft.zip) ([paper](http://www.erichaines.com/ShaftCulling.pdf)) between the beginning and ending position of the AABB. Test the static sphere with shaft testing. ](https://www.geometrictools.com/Documentation/IntersectionMovingSphereBox.pdf)  


**Moving Triangle/Triangle:** See [GTweb doc](https://www.geometrictools.com/Documentation/MethodOfSeparatingAxes.pdf) and [Catto 2013](https://code.google.com/archive/p/box2d/downloads). 

**Moving AABB/AABB:** _(location)_ See [Gomez](https://web.archive.org/web/19991129002900/http://www.gamasutra.com/features/19991018/Gomez_3.htm) for a use of the Separating Axis Theorem to solve this problem. _(boolean)_ Form a [shaft](http://www.realtimerendering.com/downloads/shaft.zip) ([paper](http://www.erichaines.com/ShaftCulling.pdf)) between the beginning and ending position of the AABB and compare the static AABB against it with shaft testing.  


**Moving OBB/OBB:** _(location)_ See [GTweb doc](https://www.geometrictools.com/Documentation/IntersectionRotatingBoxes.pdf).  


**Moving Convex Polyhedra/Convex Polyhedra:** _(boolean)_ The GTCG book, p. 615 on, gives pseudocode for using the method of separating axes to solve this problem. See [GTweb doc](https://www.geometrictools.com/Documentation/MethodOfSeparatingAxes.pdf).  


[Gregorius 2015](http://media.steampowered.com/apps/valve/2015/DirkGregorius_Contacts.pdf) covers computing contact points among spheres, capsules, convex hulls, and meshes. 

Many of the non-curved objects which are moving can be treated as forming [shafts](http://www.erichaines.com/ShaftCulling.pdf) between the starting and ending locations, and then the shaft can be tested against a ray simply enough, or against another non-curved object by using the polyhedron/polyhedron test in Gems IV p.83. Another approach is to use the [Separating Axis Theorem](https://www.geometrictools.com/Documentation/MethodOfSeparatingAxes.pdf) (also see [Bobic](https://web.archive.org/web/20000510080633/http://www.gamasutra.com/features/20000330/bobic_01.htm)) to tell if the two objects overlap. However, all of these approaches are just _boolean_ tests. 

## Article references

**Bobic** \- Bobic, Nick, ["Advanced Collision Detection Techniques,"](https://web.archive.org/web/20000510080633/http://www.gamasutra.com/features/20000330/bobic_01.htm) _Gamasutra_, March 2000.   
**Gomez** \- Gomez, Miguel, ["Simple Intersection Tests for Games,"](https://web.archive.org/web/19991128214140/http://www.gamasutra.com/features/19991018/Gomez_1.htm) _Gamasutra_, October 1999.   
**Schroeder** \- Schroeder, Tim, "Collision Detection Using Ray Casting," _Game Developer Magazine_, pp. 50-57, August 2001. 

## Graphics Gems references

**Ray/ray:** Ronald Goldman, _Intersection of Two Lines in Three-Space_, Graphics Gems, p. 304.  
**Ray/sphere:** Jeff Hultquist, _Intersection of a Ray with a Sphere_, Graphics Gems, pp. 388-389.  
**Ray/cylinder:** Joseph M. Cychosz and Warren N. Waggenspack, Jr., _Intersecting a Ray with a Cylinder_, Graphics Gems IV, pp. 356-365, [includes code](https://github.com/erich666/GraphicsGems/blob/master/gemsiv/ray_cyl.c).  
**Ray/polygon:** Eric Haines, _[Point in Polygon Strategies_](http://www.erichaines.com/ptinpoly), Graphics Gems IV, pp. 24-46, [includes code](https://github.com/erich666/GraphicsGems/tree/master/gemsiv/ptpoly_haines).  
**Ray/cone:** Ching-Kuang Shene, _Computing the Intersection of a Line and a Cone_, Graphics Gems V, pp. 227-231.  
**Ray/AABB:** Andrew Woo, _Fast Ray-Box Intersection_, Graphics Gems, pp. 395-396, [includes code](https://github.com/erich666/GraphicsGems/blob/master/gems/RayBox.c).  
**Ray/polyhedron:** Eric Haines, _Fast Ray-Convex Polyhedron Intersection_, Graphics Gems II, pp. 247-250, [includes code](https://github.com/erich666/GraphicsGems/blob/master/gemsii/RayCPhdron.c).  


**Plane/AABB and AABB/polyhedron:** Ned Greene, _Detecting Intersection of a Rectangular Solid and a Convex Polyhedron_, Graphics Gems IV, pp. 74-82.  


**Sphere/AABB:** Jim Arvo, _A Simple Method for Box-Sphere Intersection Testing_, Graphics Gems, pp. 247-250, [includes code](https://github.com/erich666/GraphicsGems/blob/master/gems/BoxSphere.c).  


**Triangle/AABB:** Doug Voorhies, _Triangle-Cube Intersection_, Graphics Gems III, pp. 236-239, [includes code](https://github.com/erich666/GraphicsGems/blob/master/gemsiii/triangleCube.c).  
**Triangle/AABB and AABB/polyhedron:** Green and Hatch, _Fast Polygon-Cube Intersection Testing_, Graphics Gems V, pp. 375-379, [includes code](https://github.com/erich666/GraphicsGems/tree/master/gemsv/ch7-2/).  
**Triangle/frustum:** Paul Heckbert, _Generic Convex Polygon Scan Conversion and Clipping_, Graphics Gems, pp. 84-86, [includes code](https://github.com/erich666/GraphicsGems/tree/master/gems/PolyScan/).  


**Polyhedron/polyhedron:** Rich Rabbitz, _Fast Collision Detection of Moving Convex Polyhedra_, Graphics Gems IV, pp. 83-109, [includes code](https://github.com/erich666/GraphicsGems/blob/master/gemsiv/collide.c).  


## Algorithms

Scalar values are lowercase italic: _a, n, t_. Vectors are lowercase bold: **p, v, x**. Matrices are uppercase bold: **M, T**. "X" denotes a cross product, "^2" means "squared", "||**x**||" means the length of vector **x**. 

**Ray/ray:** _(after Goldman, Graphics Gems; see his article for the derivation)_ Define each ray by an origin **o** and a normalized (unit vector) direction **d**. The two lines are then

_L1(t1)_ = **o1** \+ **d1***_t1_  
_L2(t2)_ = **o2** \+ **d2***_t2_  


The solution is:  
_t1_ = Determinant{(**o2**-**o1**),**d2**,**d1** X **d2**} / ||**d1** X **d2**||^2

and

_t2_ = Determinant{(**o2**-**o1**),**d1**,**d1** X **d2**} / ||**d1** X **d2**||^2

If the lines are parallel, the denominator ||**d1** X **d2**||^2 is 0.

If the lines do not intersect, _t1_ and _t2_ mark the points of closest approach on each line. 

![](spacer.gif)
   


* * *

Contact: [Eric](mailto:erich@acm.org)

* Large World Coordinates in Niagara for Unreal Engine
<https://docs.unrealengine.com/5.3/en-US/large-world-coordinates-in-niagara-for-unreal-engine/>

* Relationship between Niagara DataInterface and it’s PerInstanceData?
<https://udn.unrealengine.com/s/question/0D52L00004lunvOSAQ/relationship-between-niagara- datainterface-and-its-perinstancedata>

* Niagara Spawn particles in custom positions
<https://dev.epicgames.com/community/snippets/L2B/unreal-engine-niagara-spawn-particles-in- custom-positions>

* Virtual Texture Memory Pools in Unreal Engine
 <https://docs.unrealengine.com/5.3/en-US/virtual-texture-memory-pools-in-unreal-engine/> 

* World Building Guide
 <https://udn.unrealengine.com/s/article/World-Building-Guide>

* Crash Reporter Client for Unreal Engine | Sentry Documentation <https://docs.sentry.io/platforms/unreal/configuration/setup-crashreporter/>

* medium.com/@davidzulic/unity-drawing-custom-debug-shapes-part-1-4941d3fda905
  <https://medium.com/@davidzulic/unity-drawing-custom-debug-shapes-part-1-4941d3fda905>

* Low res mips only on certain objects
  <https://udn.unrealengine.com/s/question/0D52L00005HA6W2SAL/low-res-mips-only-on-certain-objects>

* Unreal Engine Issues and Bug Tracker (UE-181294) <https://issues.unrealengine.com/issue/UE-181294>

* How to Improve Texture Streaming GPU performance in UE5 over 20% increase on GPU memory [Solved] - Development / Platform & Builds - Epic Developer Community Forums
<https://forums.unrealengine.com/t/how-to-improve-texture-streaming-gpu-performance-in-ue5- over-20-increase-on-gpu-memory-solved/267023/19>

* What is Crunch Compression? - techarthub <https://www.techarthub.com/what-is-crunch-compression/>

* Your Guide to Texture Compression in Unreal Engine - techarthub <https://www.techarthub.com/your-guide-to-texture-compression-in-unreal-engine/>

* Enhanced Input in Unreal Engine | Unreal Engine 5.3 Documentation <https://docs.unrealengine.com/5.3/en-US/enhanced-input-in-unreal-engine/>

* Debugging and Optimizing Memory <https://www.unrealengine.com/en-US/blog/debugging-and-optimizing-memory>

* <https://simon.peytonjones.org/assets/pdfs/haskell-exchange-22.pdf>

* How to Create a Custom Deformer Graph in Unreal Engine | Unreal Engine 5.1 Documentation

<https://docs.unrealengine.com/5.1/en-US/how-to-create-a-custom-deformer-graph-in-unreal- engine/>

* Exploring Unreal's physics framework - Caius' Blog <https://itscai.us/blog/post/ue-physics-framework/>

* The Grug Brained Developer <https://grugbrain.dev/>

* Crafting Interpreters <https://craftinginterpreters.com/>

* Fixed random crash ocurring in HLOD builder commandlet, where we're h... · EpicGames/ UnrealEngine@62f5660

<https://github.com/EpicGames/UnrealEngine/commit/ 62f566009a8ad315e3177f368e9dc8644ddf3e41>

* Unreal 5.1 appears to be forcing foliage to fully load no matter the distance from the camera during a render Queue Render

<https://udn.unrealengine.com/s/question/0D54z00008UMi1dCAD/unreal-51-appears-to-be-forcing- foliage-to-fully-load-no-matter-the-distance-from-the-camera-during-a-render-queue-render>

* Primer: Loading Pak Files and Content at Runtime <https://udn.unrealengine.com/s/article/Primer-Loading-Pak-Files-and-Content-at-Runtime>

* Experimental: Getting Started With Iris <https://udn.unrealengine.com/s/article/Experimental-Getting-Started-With-Iris>

* Tech Note: WinGDK PSO cache fix <https://udn.unrealengine.com/s/article/Tech-Note-WinGDK-PSO-cache-fix>

* Using the RebuildHLOD Automation Tool <https://udn.unrealengine.com/s/article/Using-the-RebuildHLOD-Automation-Tool>

* Summary of How HLODs Are Generated in Fortnite <https://udn.unrealengine.com/s/article/Summary-of-How-HLODs-Are-Generated-in-Fortnite>

* PacktPublishing/Mastering-Graphics-Programming-with-Vulkan <https://github.com/PacktPublishing/Mastering-Graphics-Programming-with-Vulkan>

* Game Physics Cookbook <https://gamephysicscookbook.com/>

* Stargazers · gszauer/GamePhysicsCookbook <https://github.com/gszauer/GamePhysicsCookbook>

* LearningUnrealEngine/Unit tests source notes.md at master · ibbles/LearningUnrealEngine

<https://github.com/ibbles/LearningUnrealEngine/blob/master/ Unit%20tests%20source%20notes.md>

* World Partition: Soft object pointers for actors that are in Data Layers or Spatially Loaded fail to resolve.
  <https://udn.unrealengine.com/s/question/0D54z00008PRvloCAD/world-partition-soft-object-pointers-for-actors-that-are-in-data-layers-or-spatially-loaded-fail-to-resolve>

* Optimize Unreal Engine builds with BuildGraph and CircleCI | CircleCI <https://circleci.com/blog/optimize-unreal-engine-builds/>

* Steam Deck Quick Start in Unreal Engine | Unreal Engine 5.0 Documentation <https://docs.unrealengine.com/5.0/en-US/steam-deck-quick-start-in-unreal-engine/>

* Image generation - OpenAI API <https://beta.openai.com/docs/guides/images/usage>

* https://youtube.com/watch?v=4NkNBImONJU&feature=share <https://youtube.com/watch?v=4NkNBImONJU&feature=share>

* EmberGen: Real-Time Fluid Simulations For Fire, Smoke, And Explosions! <https://jangafx.com/software/embergen/?section=games>

* AyoubKhammassi/CustomMeshComponent: The minimal source code for creating a custom mesh component and using it in Unreal Engine 4. This is an example project published with a series of articles that cover the topic.

<https://github.com/AyoubKhammassi/CustomMeshComponent>

* https://youtube.com/watch?v=zcDv5WfCTSU&feature=share <https://youtube.com/watch?v=zcDv5WfCTSU&feature=share>

* Using DDC for QA Builds vs Full Cooks

<https://udn.unrealengine.com/s/question/0D54z0000879GnYCAU/using-ddc-for-qa-builds-vs-full- cooks>

* Skeletal mesh vertex editing - Unreal Engine / Programming & Scripting - Unreal Engine Forums <https://forums.unrealengine.com/t/skeletal-mesh-vertex-editing/339834>

* Running Gauntlet Tests | Unreal Engine 4.27 Documentation

<https://docs.unrealengine.com/4.27/en-US/TestingAndOptimization/Automation/Gauntlet/ RunningTests/>

## performance links

* Adjusting Engine Feature Levels | Unreal Engine Documentation
<https://docs.unrealengine.com/4.26/en-US/TestingAndOptimization/PerformanceAndProfiling/Options/>

* youtube clip
 <https://youtube.com/watch?v=EbXakIuZPFo&feature=share>

* Screen Percentage with Temporal Upsample | Unreal Engine Documentation
 <<https://docs.unrealengine.com/4.26/en-US/RenderingAndGraphics/ScreenPercentage/>

* Chaos Physics Scene does not use the World PhysicsCollisionHandler
<https://udn.unrealengine.com/s/question/0D54z00007gr2KcCAI/chaos-physics-scene-does-not-use-the-world-physicscollisionhandler>

* Implementing Fshader Cache to smooth out hitches.
<https://udn.unrealengine.com/s/question/0D54z00007RHJRYCA5/implementing-fshader-cache-to-smooth-out-hitches>

* GeometryCache performance and future plans
<https://udn.unrealengine.com/s/question/0D54z00007gqoCICAY/geometrycache-performance-and-future-plans

* Setting p.BroadphaseType to 4 hits check in AABBTree PrepareCopyTimeSliced
<https://udn.unrealengine.com/s/question/0D54z00007iKhPhCAK/setting-pbroadphasetype-to-4-hits-check-in-aabbtree-preparecopytimesliced>

* Streaming Virtual Texturing in Unreal Engine | Unreal Engine 5.0 Documentation
<https://docs.unrealengine.com/5.0/en-US/streaming-virtual-texturing-in-unreal-engine/>

* UEEngine tools for performance on Open World games
<https://youtube.com/watch?v=VTjALz6dhvw&feature=share>

* Using the RebuildHLOD Automation Tool - Unreal Engine / Pipeline & Plugins - Unreal Engine Forums
<https://forums.unrealengine.com/t/using-the-rebuildhlod-automation-tool/265073>

* Dynamic Resolution | Unreal Engine Documentation
* <https://docs.unrealengine.com/4.27/en-US/RenderingAndGraphics/DynamicResolution/>

* UnrealEngine/Patches/Improve AO Shader memory access pattern at EngineOpt-4.25 * GPUOpenSoftware/UnrealEngine
<https://github.com/GPUOpenSoftware/UnrealEngine/tree/EngineOpt-4.25/Patches/Improve%20AO%20Shader%20memory%20access%20pattern>

* Significance Manager short tutorial
<https://youtube.com/watch?v=u7K4qFTW608&feature=share>

* Improving UE4 Perf for Battle Royale
 <https://youtube.com/watch?v=KHWquMYtji0&feature=share>

* FRHICommandListImmediate get - Programming & Scripting / C++ - Unreal Engine Forums
<https://forums.unrealengine.com/t/frhicommandlistimmediate-get/481455>

* https://cs.uwaterloo.ca/~m32rober/rsqrt.pdf

* https://link.medium.com/B6jXT6XMUqb 
<https://link.medium.com/B6jXT6XMUqb>

* UE4 Automation Testing | Squareys’ Blog
<https://blog.squareys.de/ue4-automation-testing/>

* DaedalicEntertainment/ue4-test-automation: Facilitates setting up integration test suits with Unreal Engine 4 Gauntlet.
<https://github.com/DaedalicEntertainment/ue4-test-automation#setup>

* BugReport: D3D12 Crash when command lists per payload exceeds 128 (due to wrong constant used)
<https://udn.unrealengine.com/s/question/0D54z00007Y5AYzCAN/bugreport-d3d12-crash-when-command-lists-per-payload-exceeds-128-due-to-wrong-constant-used>

* UE4 Rendering FAQ - Performance https://udn.unrealengine.com/s/article/UE4-Rendering-FAQ-Performance

* Bringing Fortnite to Mobile https://udn.unrealengine.com/s/article/Bringing-Fortnite-to-Mobile

* Dealing with GPU crashes https://udn.unrealengine.com/s/article/dealing-with-GPU-crashes

* How to eliminate Moire effect on materials?

https://udn.unrealengine.com/s/question/0D54z00007gtCmOCAU/how-to-eliminate-moire-effect-on- materials

* RDG 101_ A Crash Course.pptx - Box

https://m.box.com/shared_item/ https%3A%2F%2Fepicgames.box.com%2Fs%2Ful1h44ozs0t2850ug0hrohlzm53kxwrz

* Draw Call Bottleneck? - Help me understand Frontend - Unreal Engine / Rendering - Unreal Engine Forums

https://forums.unrealengine.com/t/draw-call-bottleneck-help-me-understand-frontend/94765

* Animation Insights Overview | Unreal Engine Documentation

https://docs.unrealengine.com/4.27/en-US/TestingAndOptimization/PerformanceAndProfiling/ UnrealInsights/AnimationInsights/

* How to Implement Trace Source Filtering | Unreal Engine Documentation

https://docs.unrealengine.com/4.27/en-US/TestingAndOptimization/PerformanceAndProfiling/ UnrealInsights/AnimationInsights/HowTo/TraceSourceFiltering/

* GPU Profiling | Unreal Engine Documentation https://docs.unrealengine.com/4.27/en-US/TestingAndOptimization/PerformanceAndProfiling/GPU/

* Optimization Tools in Code Plugins - UE Marketplace https://www.unrealengine.com/marketplace/en-US/product/optimization-tools

* Additional Commands to Improve Performance - Optimizing Projects for Real Time

https://dev.epicgames.com/community/learning/courses/d1r/optimizing-projects-for-real-time/kOx/ additional-commands-to-improve-performance

* Search | Epic Developer Community

https://dev.epicgames.com/community/search? query=Optimization&types=learning&application=unreal_engine

* Fantastic Bottlenecks and Where to Find Them | Unreal Fest Europe 2019 | Unreal Engine | Epic Developer Community

https://dev.epicgames.com/community/learning/talks-and-demos/O6a/fantastic-bottlenecks-and- where-to-find-them-unreal-fest-europe-2019-unreal-engine

* Hierarchical LOD Outliner Reference in Unreal Engine | Unreal Engine 5.0 Documentation https://docs.unrealengine.com/5.0/en-US/hierarchical-lod-outliner-reference-in-unreal-engine/

* https://youtube.com/watch?v=VjPLegMhm8I&feature=share https://youtube.com/watch?v=VjPLegMhm8I&feature=share

* Niagara Data Interfaces https://udn.unrealengine.com/s/article/Niagara-Data-Interfaces

* AMD FidelityFX - Super Resolution 2 - GPUOpen https://gpuopen.com/fidelityfx-superresolution-2/

* Post Process Materials | Unreal Engine Documentation

https://docs.unrealengine.com/4.27/en-US/RenderingAndGraphics/PostProcessEffects/ PostProcessMaterials/

* https://docs.unrealengine.com/5.0/en-US/API/Runtime/Core/Math/FMath/ ComputeProjectedSphereScissorRec

https://docs.unrealengine.com/5.0/en-US/API/Runtime/Core/Math/FMath/ ComputeProjectedSphereScissorRec-

* FMath::GetDistanceWithinConeSegment | Unreal Engine Documentation

https://docs.unrealengine.com/5.0/en-US/API/Runtime/Core/Math/FMath/ GetDistanceWithinConeSegment/

* Imposters in UE4 https://www.unrealgamedev.org/post/imposters-in-ue4

* PSO Caching in UE4 https://www.unrealgamedev.org/post/pso-caching-in-ue4

* Programming PROP Tips in Unreal: Optimize Blueprints | Reference viewer, Size map and Wrappers — UNF Games

https://www.unfgames.com/blog-full/blueprints-tutorial-unreal-engine-5-reference-viewer

* https://github.com/EpicGames/UnrealEngine/pull/9392 https://github.com/EpicGames/UnrealEngine/pull/9392

* https://github.com/EpicGames/UnrealEngine/commit/ c1ea79bca537b843006f9e728fcd127a851701c0

https://github.com/EpicGames/UnrealEngine/commit/ c1ea79bca537b843006f9e728fcd127a851701c0

* What would be the guideline to deal with floating numbers in UE5?

https://udn.unrealengine.com/s/question/0D54z00007iLattCAC/what-would-be-the-guideline-to- deal-with-floating-numbers-in-ue5

* Variable Rate Shading: a scalpel in a world of sledgehammers - DirectX Developer Blog

https://devblogs.microsoft.com/directx/variable-rate-shading-a-scalpel-in-a-world-of- sledgehammers/

* https://github.com/GPUOpen-Effects/FidelityFX-FSR2/blob/master/src/ffx-fsr2-api/shaders/ ffx_fsr2_rec

https://github.com/GPUOpen-Effects/FidelityFX-FSR2/blob/master/src/ffx-fsr2-api/shaders/ ffx_fsr2_reconstruct_dilated_velocity_and_previous_depth.h

* AMD ¼Prof - AMD https://developer.amd.com/amd-uprof/#download

* Finding and Removing Fully Occluded Meshes | Unreal Engine Documentation https://docs.unrealengine.com/4.27/en-US/WorkingWithContent/Jacketing/

* Multiplayer Programming Quick Start for Unreal Engine | Unreal Engine 5.0 Documentation https://docs.unrealengine.com/5.0/en-US/multiplayer-programming-quick-start-for-unreal-engine/

* Chaos Destruction Overview | Unreal Engine 4.27 Documentation

https://docs.unrealengine.com/4.27/en-US/InteractiveExperiences/Physics/ChaosPhysics/ ChaosDestruction/ChaosDestructionOverview/

* Geometry collection setup questions

https://udn.unrealengine.com/s/question/0D54z00007JUQfjCAH/geometry-collection-setup- questions

* https://youtu.be/iFKzXnIiH50 https://youtu.be/iFKzXnIiH50

* https://youtu.be/_TZ2lUJefvY https://youtu.be/_TZ2lUJefvY
* UE5 Light Instances https://dev.epicgames.com/community/learning/tutorials/zweW/light-weight-instances-ue5

* Feed Detail https://udn.unrealengine.com/s/feed/0D54z000080EMuRCAW
* HLOD generation Automation - https://forums.unrealengine.com/t/using-the-rebuildhlod-automation-tool/265073

* Feed Detail https://udn.unrealengine.com/s/feed/0D54z00007jjIbkCAE

* how to optimize the runtime gpuskincache (recompute tangents) cost?
https://udn.unrealengine.com/s/question/0D54z00007iIwnqCAC/how-to-optimize-the-runtime- gpuskincache-recompute-tangents-cost

* Landscape physical material render fixes: * EpicGames/UnrealEngine@9eeba5a
https://github.com/EpicGames/UnrealEngine/commit/9eeba5aaa3e7ad72ae16cf044351cf8fae1132a0

* Feed Detail https://udn.unrealengine.com/s/feed/0D54z00007SBJV4CAP

* Chaos: Joint Constraint Per-Frame Leak
https://udn.unrealengine.com/s/question/0D54z00007WgfXcCAJ/chaos-joint-constraint-perframe-leak

* How do you get substepping to work in Chaos - UDN?
https://udn.unrealengine.com/s/question/0D54z00007c1s8rCAA/how-do-you-get-substepping-to-work-in-chaos

* Skeletal mesh component ticks before SetWorldLocationAndRotation. Is this a known issue?
https://udn.unrealengine.com/s/question/0D54z00007Y4aWoCAJ/skeletal-mesh-component-ticks-before-setworldlocationandrotation-is-this-a-known-issue

* UDN Feed https://udn.unrealengine.com/s/feed/0D54z00006u24i1CAA

* Causing Chaos: The Future of Physics and Destruction https://udn.unrealengine.com/s/article/Causing-Chaos-The-Future-of-Physics-and-Destruction

* Some ISPC functions aren’t set up to vectorize
https://udn.unrealengine.com/s/question/0D54z00007Y4aTBCAZ/some-ispc-functions-arent-set-up-to-vectorize

* GDC Vault - Scalability for All: Unreal Engine 4 on Intel (Presented by Epic Games and Intel) https://gdcvault.com/browse/gdc-19/

* Physically Based - The PBR values database
 https://physicallybased.info/
 
* GDC ISPC in Unreal Engine Presentation
https://s3-us-west-2.amazonaws.com/near-me-oregon/instances/132/uploads/attachments/custom_attachment/file/16837/GDC_2020_ISPC_in_Unreal_Engine_4.pdf?X-Amz-Expires=600&X-Amz-Date=20220912T211329Z&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIA4IMKIWYVKZ6JE7X7/20220912/us-west-2/s3/aws4_request&X-Amz-SignedHeaders=host&X-Amz-Signature=bbd5a5b1d6919b7e841d44d02c6c6f2625ed157db1d55f422d9cce39a8c48a6d

* Unreal Engine 5 Chaos Vehicle Not Moving Bug - YouTube https://m.youtube.com/watch?v=TNPTyQUS63A

* Is it possible to modify collision contacts?

https://udn.unrealengine.com/s/question/0D54z00007Y4acYCAR/is-it-possible-to-modify-collision- contacts

* [UE5, Chaos] How to create constraints between arbitrary FBodyInstances in code

https://udn.unrealengine.com/s/question/0D54z000084woFlCAI/ue5-chaos-how-to-create- constraints-between-arbitrary-fbodyinstances-in-code

* Chaos puts bodies to sleep if a low enough force is applied, despite current velocity

https://udn.unrealengine.com/s/question/0D54z00007ZEoYHCA1/chaos-puts-bodies-to-sleep-if-a- low-enough-force-is-applied-despite-current-velocity

* Chaos Scene Queries and Rigid Body Engine in UE5 - Unreal Engine https://www.unrealengine.com/en-US/tech-blog/chaos-scene-queries-and-rigid-body-engine-in-ue5

* https://github.com/EpicGames/UnrealEngine/pull/9566 https://github.com/EpicGames/UnrealEngine/pull/9566

* GPU Skin Cache https://udn.unrealengine.com/s/question/0D54z00007RItj5CAD/gpu-skin-cache

* GPU skin cache tanking FPS https://udn.unrealengine.com/s/question/0D54z00007iN9nhCAC/gpu-skin-cache-tanking-fps

* Skeletal Mesh Deferred Kinematic Update question <https://udn.unrealengine.com/s/question/0D54z000082To1CCAS/skeletal-mesh-deferred-kinematic- update-question>

* In case anyone runs into this; 
The issue is that between 4.27 and 5.0 Epic introduced a regression issue with fast loading clients during seamless travel. Since we rely heavily on that it failed. 
The fix is CL 19907190 & CL 18005285 which we were missing.