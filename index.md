* Testing for Game Development <https://www.gamedeveloper.com/programming/testing-for-game-development>

Skip To Main Content

[ ![Intel logo - Return to the home page](/content/dam/logos/intel-header-logo.svg) ](/content/www/us/en/homepage.html)

Toggle Navigation

Sign In

### Sign In

Username

Your username is missing

Password

Your password is missing

By signing in, you agree to our Terms of Service.

Remember me

Forgot your Intel[username](https://www.intel.com/content/www/us/en/my-intel/forgot-userid.html) or[password](https://www.intel.com/content/www/us/en/my-intel/forgot-password.html)? 

[Frequently Asked Questions](/content/www/us/en/support/topics/sign-in-faq.html)

Do you work for Intel? Sign in here. 

Don’t have an Intel account? Sign up here for a basic account.

My Intel

My Tools 

  * ?

Sign Out

USA (English)

##  Select Your Region 

### Asia Pacific

  * [ Asia Pacific (English) ](https://www.intel.sg/content/www/xa/en/homepage.html)
  * [ Australia (English) ](https://www.intel.com.au/content/www/au/en/homepage.html)
  * [ India (English) ](https://www.intel.in/content/www/in/en/homepage.html)
  * [ Indonesia (Bahasa Indonesia) ](https://www.intel.co.id/content/www/id/id/homepage.html)
  * [ Japan (日本語) ](https://www.intel.co.jp/content/www/jp/ja/homepage.html)
  * [ Korea (한국어) ](https://www.intel.co.kr/content/www/kr/ko/homepage.html)
  * [ Mainland China (简体中文) ](https://www.intel.cn/content/www/cn/zh/developer/articles/technical/parallel-techniques-in-modeling-particle-systems-using-vulkan-api.html)
  * [ Taiwan (繁體中文) ](https://www.intel.com.tw/content/www/tw/zh/homepage.html)
  * [ Thailand (ไทย) ](https://www.thailand.intel.com/content/www/th/th/homepage.html)
  * [ Vietnam (Tiếng Việt) ](https://www.intel.vn/content/www/vn/vi/homepage.html)

### Europe

  * [ France (Français) ](https://www.intel.fr/content/www/fr/fr/homepage.html)
  * [ Germany (Deutsch) ](https://www.intel.de/content/www/de/de/homepage.html)
  * [ Ireland (English) ](https://www.intel.ie/content/www/ie/en/homepage.html)
  * [ Italy (Italiano) ](https://www.intel.it/content/www/it/it/homepage.html)
  * [ Poland (Polski) ](https://www.intel.pl/content/www/pl/pl/homepage.html)
  * [ Spain (Español) ](https://www.intel.es/content/www/es/es/homepage.html)
  * [ Turkey (Türkçe) ](https://www.intel.com.tr/content/www/tr/tr/homepage.html)
  * [ United Kingdom (English) ](https://www.intel.co.uk/content/www/uk/en/homepage.html)

### Latin America

  * [ Argentina (Español) ](https://www.intel.la/content/www/xl/es/homepage.html)
  * [ Brazil (Português) ](https://www.intel.com.br/content/www/br/pt/homepage.html)
  * [ Chile (Español) ](https://www.intel.la/content/www/xl/es/homepage.html)
  * [ Colombia (Español) ](https://www.intel.la/content/www/xl/es/homepage.html)
  * [ Latin America (Español) ](https://www.intel.la/content/www/xl/es/homepage.html)
  * [ Mexico (Español) ](https://www.intel.la/content/www/xl/es/homepage.html)
  * [ Peru (Español) ](https://www.intel.la/content/www/xl/es/homepage.html)

### Middle East/Africa

  * [ Israel (עברית) ](https://www.intel.co.il/content/www/il/he/homepage.html)

### North America

  * [ United States (English) ](https://www.intel.com/content/www/us/en/homepage.html)
  * [ Canada (English) ](https://www.intel.ca/content/www/ca/en/homepage.html)
  * [ Canada (Français) ](https://www.intel.ca/content/www/ca/fr/homepage.html)

Toggle Search

Search < Close Search Panel Advanced Search

close 

[ Sign In](javascript:void\(\);) to access restricted content 

### Using Intel.com Search

You can easily search the entire Intel.com site in several ways.

  * Brand Name: ** Core i9 **
  * Document Number: ** 123456 **
  * Code Name: ** Alder Lake **
  * Special Operators: ** “Ice Lake”, Ice AND Lake, Ice OR Lake, Ice* **

### Quick Links

You can also try the quick links below to see results for most popular searches.

  * [ Product Information ](https://www.intel.com/content/www/us/en/products/overview.html?wapkw=quicklink:products)
  * [ Support ](https://www.intel.com/content/www/us/en/support.html?wapkw=quicklink:support)
  * [ Drivers & Software ](https://downloadcenter.intel.com?wapkw=quicklink:download-center)

### Recent Searches

[ Sign In](javascript:void\(\);) to access restricted content 

### Advanced Search

All of these terms Any of these terms Exact term only Find results with

All Results  Product Information  Support  Drivers & Software  Documentation & Resources  Partners  Communities  Corporate  Show results from

### Only search in

Title Description Content ID

Search 

[Sign in](javascript:void\(\);) to access restricted content. 

The browser version you are using is not recommended for this site.  
Please consider upgrading to the latest version of your browser by clicking one of the following links.

  * [Safari](https://support.apple.com/downloads/safari)
  * [Chrome](https://support.google.com/chrome/answer/95346?hl=en)
  * [Edge](https://www.microsoft.com/en-us/edge)
  * [Firefox](https://www.mozilla.org/en-US/firefox/new/)

#  Parallel Techniques in Modeling Particle Systems Using Vulkan* API 

Published: 02/06/2018    
  
Last Updated: 02/06/2018 

[View PDF](/content/dam/develop/external/us/en/documents/paralleltechniquesinmodelingparticlesystemsusingvulkanapi-754322.pdf)

Example of using GPU- and CPU-based solutions utilizing Vulkan graphics and compute API

Tomasz Chadzynski  
Integrated Computer Solutions Inc.

## 1 Introduction

Parallel processing has become one of the most important aspects of today's programming techniques. The shift in paradigm forced by the CPUs hitting the power wall enforced programming techniques that emphasized the spreading of computations over multiple cores/processors. As it turns out, many of the computation tasks that software developers face are parallelizable. One example is the case of modeling particle systems. Such systems are widely used in many fields from physical simulation to computer games.

The Vulkan* API is a collaborative effort by the industry to meet current demands of computer graphics. It is a new approach that emphasizes hiding the CPU bottleneck through parallelism, allowing much more flexibility in application structure. Aside from components related only to graphics, the Vulkan API also defines the compute pipeline for numerical computation.

This paper discusses and compares aspects of the implementation of a particle system using CPUs and GPUs supported by a Vulkan-based renderer example.

### 1.1 Assumptions and expectations

With all the performance gains that Vulkan has to offer, there is a downside in the form of a rather steep learning curve. Drawing a triangle, the simplest example available on the Internet can take around six hundred lines of code. This is because Vulkan API requires the developer to specify nearly all aspects of the rendering mechanism. Still, given some effort, Vulkan is a clear and straightforward example for using API.

This document does not intend to teach Vulkan basics. Some basic knowledge of Vulkan is required, however.  You should already know how to set up simple Vulkan applications. If you are new to Vulkan, then a good start would be to work through the [LunarG tutorial](https://vulkan.lunarg.com/doc/view/1.0.57.0/windows/tutorial/html/index.html).

The example code accompanying this paper is organized to emphasize presenting architectural concepts which lead to two important assumptions: 1) The return status from Vulkan function calls is in most cases ignored to avoid overly expanding the code base. In production, every return status should be checked and reacted on; 2) Conceptually close topics are kept within a single code flow. This reduces the need for jumping through the sources, but sometimes leads to rather long functions.

This paper is recommended to be read while looking at the accompanying code. Make sure you have the examples downloaded and use your favorite code browsing tool. To avoid long code listings, this paper references the code through a series of tags. For example, GPU_TP.15 references point fifteen in the Vulkan compute version of the code base. Each tag is unique and easily searchable within the code base.

Lastly, one of the major design goals of Vulkan is to give as much freedom to the application designer as possible. Therefore, there are many ways of implementing a given task depending on the design goals, target hardware, scalability, and so on. This paper’s goal is to introduce and spark some creative thinking, rather than provide a final approach.

### 1.2 Additional resources

Vulkan has received much attention, which has resulted in many good information sources. Here are few recommended reference materials:

  1. Vulkan specification and quick reference: <https://www.khronos.org/registry/vulkan/>
  2. OpenGL and GLSL specification. We are mostly interested in GLSL as we use it as a shader programming language: <https://www.khronos.org/registry/OpenGL/index_gl.php>
  3. Vulkan SDK and an excellent tutorial covering Vulkan basics: <https://vulkan.lunarg.com/>
  4. Another Vulkan tutorial goes beyond basics, covering more advanced memory handling and textures: <https://vulkan-tutorial.com/>
  5. Database of hardware supporting Vulkan. A great source for capabilities that are offered by the variety of hardware: <http://vulkan.gpuinfo.org/>
  6. A large set of examples in Vulkan from basic triangle to compute shader: <https://github.com/SaschaWillems/Vulkan>

### 1.3 Building examples

The project build is organized using Visual Studio* 2017. Overall, it uses three dependencies: GLM, GLFW, and Vulkan SDK. The first two are installed automatically through NuGet. The Vulkan SDK should be downloaded and installed. After opening the project, select the "Property Manager" tab. From there, unfold the "Debug|x64" and open Vulkan Dir. Then go to "User Macros" and set the VK_DIR property to point to the main Vulkan SDK directory. For example, "C:\VulkanSDK\1.0.51.0." The Debug and Release both use the same property, so one change will affect both. From there just click “Build.”

## 2 Concept of a Simulated Particle System

Our goal is to model the movement of multiple objects (particles) through space. To make things more interesting, the scene will contain entities that would alter the path through which the particle is moving.

A single particle is defined as a set of two vectors, position in space, velocity, and an additional scalar representing mass. These set of properties describe the state of each particle:

![formula](/content/dam/develop/external/us/en/images/solve-using-vulkan-graphics-formula-2-1-754322.PNG)

We can look at the way a particle moves through space with displacement given by the differential equation:

![formula](/content/dam/develop/external/us/en/images/solve-using-vulkan-graphics-formula-2-2-754322.PNG)

For now, we will treat the velocity as a constant and solve for displacement:

![formula](/content/dam/develop/external/us/en/images/solve-using-vulkan-graphics-formula-2-3-754322.PNG)

## 

We arrive at a general formula that models how a particle is moving through space. Constant velocity is assumed (but will change soon). Also, we must have constant C, a value which must be known, in order to describe our system completely. The constant C is related to the initial conditions of this differential equation. In other words, the particle at the beginning of its life has to have a predefined state. This requires using generators.

### 2.1 Generators

The concept of a generator is to be a function which fulfills the task of "placing" a new particle into the scene in some predefined manner. This demonstration defines a single sprinkler generator with functionality consisting of spawning particles at a predefined point in space with given velocity and mass.

The position of the point of origin is given directly as a parameter. The direction is defined using spherical coordinates which are then internally converted into the Euclidean coordinate system. The angles are defined as follows:

  1. (theta): Angle starts at x-axis and rotates counterclockwise.
  2. (phi): Angle starts from z-axis towards xy-plane.
  3. The value of speed is given as a separate argument.

![Euclidean coordinates](/content/dam/develop/external/us/en/images/solve-using-vulkan-graphics-euclidean-coordinates-754322.png)

To convert into Euclidean coordinates, we use the following set of equations:

![formula](/content/dam/develop/external/us/en/images/solve-using-vulkan-graphics-formula-2-4-754322.PNG)

Going back to our general equation for particle motion and factoring in the generator, we can determine that at time t=0 the position of a particle becomes x0:

![formula](/content/dam/develop/external/us/en/images/solve-using-vulkan-graphics-formula-2-5-754322.PNG)

At this point, we have a formula that we can use to describe the motion of a particle. However, our scene will not look that interesting as all of the particles would only move in a straight line and at a constant speed. To give our scene more dynamic behavior, we introduce the concept of interactors.

### 2.2 Interactors

To understand how we can consistently influence the motion of a particle, we start treating velocity as a variable instead of constant. The change of velocity is given by the following formula:

![formula](/content/dam/develop/external/us/en/images/solve-using-vulkan-graphics-formula-2-6-754322.PNG)

This equation looks similar to the previous formula for displacement. By solving this differential equation, we arrive at the formula for velocity:

![formula](/content/dam/develop/external/us/en/images/solve-using-vulkan-graphics-formula-2-7-754322.PNG)

Therefore, to consistently change particle motion we influence the velocity indirectly through changing acceleration. We define the interactor as a function that, for the given particle state and given interactor properties, returns the acceleration vector:

![formula](/content/dam/develop/external/us/en/images/solve-using-vulkan-graphics-formula-2-8-754322.PNG)

Unfortunately, defining the interactor as a function becomes problematic. When we substitute back into the velocity equation, we see that the differential equation has a potential to become unsolvable:

![formula](/content/dam/develop/external/us/en/images/solve-using-vulkan-graphics-formula-2-9-754322.PNG)

This is not what we want. Our goal is to have the ability to introduce different types of interactors without being worried about breaking our model. To do that, we need to implement the Euler method of solving differential equations to approximate the particle movement numerically.

### 2.3 Euler method in numerical simulation of particle movement

The Euler method working principle is to step through the differential equation instead of solving across the entire domain. If we assume a sufficiently small time step, we can approximate the velocity (2) and acceleration (6) to be constants within the span of a single step. This allows us to fall back to the equations (5) and (7), and discretize them so they can be programmed. Therefore, the final set of equations to be used is as follows:

![formula](/content/dam/develop/external/us/en/images/solve-using-vulkan-graphics-formula-2-10-754322.PNG)

If the math so far in this chapter has given you trouble, don't get discouraged. It is enough to understand the final equations (10) to work with the rest of material. From now on we will treat the acceleration vector as a constant within the single iteration. Next, we dive deeper into interactors that affect the motion of a particle.

### 2.4 More on interactors

We established earlier that the particle motion within the scene would be influenced by changing acceleration, using Newton's second law:

![formula](/content/dam/develop/external/us/en/images/solve-using-vulkan-graphics-formula-2-11-754322.PNG)

We see that the task of an interactor should be to generate some force and convert it into acceleration using the mass of the particle. Moreover, we can sum up the forces coming from multiple interactors together:

![formula](/content/dam/develop/external/us/en/images/solve-using-vulkan-graphics-formula-2-12-754322.PNG)

Therefore, our final approach is as follows:

![formula](/content/dam/develop/external/us/en/images/solve-using-vulkan-graphics-formula13-754322.PNG)

The main reason to not multiply out the mass is that interactors that simulate gravity don't use it. In other words, the acceleration due to gravity does not depend on the mass of an object on which gravitational pull is exerted. It is also possible that some interactors which don’t model physically accurate behavior could simply ignore mass as well. This is an optimization step which could save a significant number of cycles spent on multiplication.

#### 2.4.1 Constant force interactor

This is the simplest form of an interactor. Its function is to exert the force on a particle regardless of any other properties. It could be used to make a particle go towards some predefined direction:

![formula](/content/dam/develop/external/us/en/images/solve-using-vulkan-graphics-formula14-754322.PNG)

#### 2.4.2 Gravity point interactor

This is the second type of interactor. It represents a single point that exerts the force of gravity on particles in the scene. Such a point has mass and position, but in our example it does not have volume. It uses the standard gravity equation:

![formula](/content/dam/develop/external/us/en/images/solve-using-vulkan-graphics-formula15-754322.PNG)

Now we can see why we chose not to include the mass of a particle within each interactor. When deriving the formula for acceleration, we end up with:

![formula](/content/dam/develop/external/us/en/images/solve-using-vulkan-graphics-formula16-754322.PNG)

In this equation, G is the gravitational constant, M is the mass of the gravity point, d represents the distance, and r is the unit vector pointing toward the gravity point interactor from the location of the particle.

#### 2.4.3 Gravity planar interactor

This is the last type of interactor implemented for this example. It is modeled as an infinite plane exerting gravitational force on the particles in the scene. In this case, the r vector is always perpendicular to the plane. Therefore, for any given particle location, the distance has to be calculated, as such: Let P1={x1,y1,z1} represent a particle in space. The plane is described by its normal vector n={a,b,c}, and a point on that plane, P={x,y,z}. The distance D is given by:

![formula](/content/dam/develop/external/us/en/images/solve-using-vulkan-graphics-formula-2-17-18-0-754322.PNG)

This type of interactor can be used to model large objects compared to scene size such as the Earth.

#### 2.4.4 Additional thoughts

Simulating physically correct behavior is not the only way to build interesting particle systems. In fact, setting up a physically accurate system in equilibrium could be very hard. A similar effect could be achieved by using non-physically accurate interactors. Such functions can look into the entire state of a particle and generate acceleration that will attempt to force certain behavior.

## 3 Vulkan Renderer for CPU-Based Simulator

The design of the renderer component used in visualizing the CPU version of the particle simulator will be described first. If you are not familiar with Vulkan, it is a good idea to pause here and review one of the tutorials. The [LunarG tutorial](https://vulkan.lunarg.com/doc/view/1.0.57.0/windows/tutorial/html/index.html) covers sufficient material to understand the rest of this paper. Also, remember that Vulkan leaves the application design to the programmer and allows for a variety of ways to approach a task. Take this guide as one of the options available rather than the definitive solution.

At a high level, when programming using Vulkan, the goal is to construct a virtual device to which drawing commands will be submitted. The draw commands are submitted to constructs called “queues.” The number of queues available and their capabilities depends upon how they were selected during construction of the virtual device, and the actual capabilities of the hardware. The power of Vulkan lies in the fact that the workload submitted to queues could be assembled and sent in parallel to already executing tasks. Vulkan offers functionality to coherently maintain the resources and perform synchronization.

In our application, we took the approach of breaking up the Vulkan renderer setup into five components (see graphic below). The goal is to present an easy-to-understand codebase for the Vulkan application.

![Figure 2](/content/dam/develop/external/us/en/images/solve-using-vulkan-graphics-flow-3-1-754322.png)

### 3.1 Physical device selection

The first step in every Vulkan application is to create the Instance Object. This functionality is delivered through VkInstance. It is required that an application has a VkInstance created before starting anything else. The VkInstance is the interface used to inspect the hardware capabilities of a computer system. This functionality is encapsulated in the AppInstance object (CPU_TP1). The AppInstance object is essentially a wrapper exposing the interface for convenient hardware device enumeration.

#### 3.1.1 Validation layers: A crucial step in Vulkan application development

One of the most critical steps when developing with Vulkan is to enable the validation layers (CPU_TP2). By design, for performance reasons, Vulkan does not check the validity of the application code. When used incorrectly, Vulkan calls would simply fail or crash with virtually no traces that would allow for debugging. With validation layers enabled, the Vulkan loader injects a layer of code for verification. The enabling of validation layers is a critical step that every developer should remember. However, that layer affects performance and should be disabled in production.

### 3.2 Vulkan virtual device and swapchain

The next step is to create the actual virtual device that will expose the command queue used to render the scene. First, a surface object must be instantiated. (The topic of the surface is out of the scope of this article, but it is covered in detail in the LunarG tutorial.) However, in this case, the demo code supports Windows* only, and the surface is created and exposed by the SurfaceWindows class (CPU_TP3).

Next is creating the Device object (CPU_TP4). Note that the Device class encapsulates much more than VkDevice. Starting with the constructor, the device class exposes multiple versions, which allows more flexibility in initialization (CPU_TP5). The physical device used to create the virtual device can be "first fit" or it can be specified using a VendorID number, if the software is to use specific hardware. End-user systems can have multiple devices that support Vulkan, and the first one on the list is not always the device desired.

The default constructor (CPU_TP6) obtains the list of available physical devices and then runs the createDevice method. If the creation was successful, this physical device is then used. If the creation was not successful, the constructor tries the next physical device. The actual device creation is done in the createDevice method (CPU_TP7). The first step is to determine if the physical device can deliver queues with the required functionality (CPU_TP8). Devices can deliver many types of queues. Some queues may support all of the required operations. Some queues may be highly specialized for the specific tasks, such as compute or transfer. In this case, the application expects the queue to allow for transfer and drawing graphics. The application will iterate over available queues until an index is found that matches the expected criteria.

Once completed, the virtual device is created. Besides VkDevice, the object supplies the queue handlers and swapchain that correspond to the virtual device. (For more details, please check the Vulkan tutorials and reference.)

### 3.3 Scene setup

The ParticlesElement (CPU_TP9) task is to draw the particle fountain. For it to be drawn, it has to belong to the scene. The _Scene _object role is to aggregate all the scene elements, maintain command buffer, and the render pass (CPU_TP10). When the simulator is ready to render, it calls the render function (CPU_TP11). This function is responsible first for initiating the command buffer for recording, obtaining the current render target, and finally starting the render pass (CPU_TP12). Once that is done, the renderer begins iterating over every element in the scene (CPU_TP13), allowing it to record drawing commands into the command buffer. In this case, there is a single scene element that draws the particle fountain. After all scene elements finish recording, the render function submits the command buffer into the queue and presents the results on the screen.

### 3.4 Scene Element

The SceneElement (CPU_TP14) represents the single element or entity within the scene. The expected scope of scene element objects is to handle everything related to rendering a single entity and maintaining required resources, like the pipeline and buffers. The ParticlesElement focuses its entire operation around two methods. First is the constructor (CPU_TP15) that initializes the rendering pipeline. Second is the recordToCmdBuffer (CPU_TP16) that is invoked by the Scene class to record element-specific draw calls into the command buffer.

### 3.5 Graphics memory allocation and performance

There is one important aspect that has to be considered when the memory for the buffers is allocated. The Vulkan device can expose different memory types that it can use. The Memory tab in the hardware database shows that devices expose multiple heaps from which memory could be allocated. Looking at the list of memory types, each type represents two values: the memory type flags that describe properties and the heap that is associated with them. (See hardware database referenced in section 1.2.)

The type of heap selected could significantly affect performance. For example, some devices, mainly discrete graphics cards, expose one heap with only DEVICE_LOCAL_BIT supported, which is the fastest memory available for that device, but does not allow direct access from the CPU (more on that in a moment). Another heap with the HOST_VISIBLE_BIT allows direct access, but has potentially longer access time.

As of today, most of Intel's integrated GPUs expose heaps with both DEVICE_LOCAL_BIT and HOST_VISIBLE_BIT. The presence of the first one ensures optimal access time for the platform. The second allows the memory mapping of the allocated buffer into the CPU address space and direct access (CPU_TP17, CPU_TP18).

When selecting a memory heap there is a three-step process. The first step is to specify and create the buffer (CPU_TP19) (note that vkCreateBuffer does not allocate memory for the buffer yet!). The second step is to use the Vulkan API to obtain the list of memory types that can support the defined buffer (CPU_TP20). The third step is to use the selected memory index to allocate the buffer memory. Of particular interest is the memoryTypeBits field in the VkMemoryRequirements. This field is a bit string that has a bit set to 1 at the position of the bit that corresponds to the memory type index of the memory type that can be used to allocate buffer memory. If the bit contains a value of 0, then a memory heap index cannot be used with the particular object of interest.

The first step above will likely provide multiple options. Therefore, in the second step, the exact memory type desired must be chosen. In this case, on Intel’s GPU, all of the memory types have DEVICE_LOCAL_BIT set. HOST_VISIBLE_BIT and HOST_COHERENT_BIT also must be set. The HOST_COHERENT_BIT guarantees that memory operation is observed without the need to manually flush the buffers. If the memoryTypeBit is set and the memory type at the given index supports the requested flags, then the specific index is selected to be used (CPU_TP21). In the third step, that index is used when allocating the actual memory on the heap (CPU_TP22).

This memory allocation topic is quite important, and you are encouraged to look further into it. Topics like staging buffer or Vulkan buffer copy operations would be a good next step, especially for devices with dedicated memory.

## 4 CPU-Based Particle Simulator

Section 2 describes the model of the particle simulator that was implemented for this project. The implementation is based on a real-time infinite loop. The simulation loop contains three main operations:

      1\. Obtain the time difference between the current and previous iteration (CPU_TP23).  
      2\. Compute the next Euler iteration for the particle model (CPU_TP24).  
      3\. Upload and render a new frame using the Vulkan renderer (CPU_TP25).

The entire physical simulation happens within the progress method (CPU_TP26) within the algorithm, and it is composed of three major steps:

      4\. For every particle, the algorithm launches the interactors and adds up the acceleration vectors (CPU_TP27).  
      5\. The algorithm sorts the particle list in such a way that all of the active particles (TTL>0) occupy the left side of the list, and all of the inactive particles occupy the right side of the list (CPU_TP28).  
      6\. Launches particle generator(s) in order to add new particles to the list if the generator’s conditions have been met, and there is space left in the buffer (CPU_TP29).

With this simple model, many interesting effects may be generated. Although this implementation uses a real-time approach (i.e., the actual hardware clock is used to obtain the time difference), the code can easily be modified to use a stepwise approach. An important point to remember is that the time difference has to be sufficiently small, otherwise it will break the model. Knowing that, it can be determined whether or not this approach is a good choice for a system that is capable of spinning the main loop at a sufficient speed. If that is not the case, consider switching from a real-time approach to an arbitrarily determined time-step, which will not use the system clock.

### 4.1 Particle model

To represent the set of particles in a scene, the Buffer class (CPU_TP30) is used. It is a relatively simple class that encapsulates a memory array of particle structures (CPU_TP31). The class also delivers a few convenience functions and the array sorting algorithm.

The purpose of the sorting algorithm is to place particles into two groups within the particle array. The active particles are placed on the left side and the inactive on right side. It is implemented as follows:

  1. Initialize L index at the first element and P index at the last element.
  2. Progress L toward the end of the array until a particle with TTL<=0 is encountered.
  3. Progress P toward beginning the array until a particle with TTL>0 is encountered.
  4. Swap tab[L] with tab[P].
  5. Repeat with L+1.

If at any time L==P, the finish condition is reached.

### 4.2 Scene interactors and generators

Both interactors and particle generators influence the scene during the simulation. Within the model, both are represented by their corresponding abstract interfaces. The interactors use BaseInteractor (CPU_TP32) and generators, BaseGenerator (CPU_TP33). Both need to be defined before the Model object is instantiated (CPU_TP34).

In the case of the interactor, all that the model requires is to obtain the acceleration vector given the particle state and time difference. Internally, the interactor can perform arbitrary operations, and interactors can be fundamentally different from each other. For example, the ConstForceInteractor (CPU_TP35) uses only force magnitude, direction vector, and particle data.

The BaseGenerator, aside from a common interface, delivers functions to generate particle properties like speed with randomized deviations (CPU_TP36). However, it leaves the exact particle location, the rate of appearance, and other details to the derived classes. In this example, point generator (CPU_TP37) is used. The point generator is set in such a way that it acts as particle sprinkler (CPU_TP38). It is given direction in polar coordinates specified in degrees, and emits particles according to a defined rate.

#### 4.2.1 Performance vs. maintainability

There exists a performance bottleneck in the implementation. A specific design choice was made to prioritize maintainability over performance. The problem originates from the polymorphic call into the computeAcceleration method (CPU_TP39).

Polymorphic calls tend to be slower than regular function calls, and every interactor is executed for every particle. It is clear how this could become a significant factor for a large number of particles. However, the advantage in this case is that there is an easy way to implement new interactors into the mix with no need make changes to the Model's code.

The alternative here could be to implement some mechanism that would detect the type of interactor and execute its procedures using a conditional statement. This will improve performance, but also increase the complexity of the code.

Which approach to use is a case-by-case decision that depends on project goals. When a small number of particles is expected with a large variety of interactors present, then the virtual method approach is a good choice. However, if the number of particles is large, then switching to other solutions could be a good way to improve performance.

### 4.3 Lifetime of the particle and the importance of sorting

There is one last topic related to particle generation and particle lifetime. Once a particle is moving through the scene, it can easily fly outside of the visible area. Since it is not visible, there is virtually no purpose in modeling it. Sometimes the goal is to model effects like a flame with a specific height. To implement such cases, every particle must have a property that determines its lifespan called “Time To Live” (TTL). At each iteration, the time difference is subtracted, and if the value is equal to or below zero, the particle is considered inactive. When particles become inactive, no operations are performed on them and they are no longer drawn.

There are two issues related to the case of inactive particles. First, is that a way is needed to free the space up for new particles. Second, is that inactive particles should no longer be drawn on the screen. This project example uses a simple rendering mechanism. However, in the case of a more complicated multi-pass renderer with more computation-heavy shaders, it is a good idea to avoid processing elements that would not be visible on the screen. This is where sorting comes in. Sorting the particle array allows for submitting draw calls that specify only the number of particles that should appear on the screen. It also simplifies the work of generators as they do not have to search through the buffer for free slots to fill.

There is a possible alternative approach. Instead of the contiguous array, a linked list could be used. This would eliminate the need for sorting, but, on the other hand, it would slow down the upload of data to the GPU buffers because of the need to convert the linked list structure into a contiguous array.

## 5 Multithreaded Approach to Computing Particle System

The speed of the simulation could be improved by parallelizing the workload. There are a few cases to consider:

      1\. Parallelize the workload across the array of particles, calculating the interactors’ contribution and Euler step as a single work unit.  
      2a. Parallelize the workload across interactors, calculating the effect of each interactor at every particle as a single work unit.  
      2b. Further parallelize Option 1, above, by splitting interactor contributions into separate work units.  
      3\. Parallelize the sorting algorithm.  
      4\. Parallelize the generators’ contribution.

Option 1, above, is the recommended approach. For each particle, the algorithm computes, as a single task, the contribution from each interactor, summing the acceleration vectors and then performing the Euler step (CPU_TP40). Since each particle resides in a different memory region, and interactors usually do not modify their internal data when computing particles, this method provides the most optimal solution. The OpenMP* framework was used to provide multithreading. OpenMP is an API that is based primarily on compiler directives and used for multithreaded-oriented development. It has lower overhead regarding required code to be written. It could be easily used to parallelize loops, but has much more to offer. However, sometimes it might not deliver the level of detail as some other available libraries.

Option 2a, is probably not recommended. Some might find that this option is appealing from the perspective that the data that defines the properties of an interactor would have to be loaded once, and then used extensively while computing each particle. This is something that will be supported by the CPU cache, significantly speeding up the process. However, there are issues with this approach. For example, acceleration must be summed up, which means there will be a need to synchronize access between threads executing the interactors and then store the acceleration vector for every particle in an additional memory region. Moreover, the entire array will require an additional pass performed to calculate the Euler step. These two disadvantages would produce significant synchronization overhead, likely rendering this strategy impractical.

Option 2b is an extension of Option 1. Hypothetically, if there are computationally demanding interactors, it could be beneficial to split their operations. However, the goal is to achieve minimal context switching. If every particle computation and every interactor contribution is parallelized, it will most likely lead to an explosion of threads. Switching between those threads would further decrease performance.

Option 3 suggests improving the sorting algorithm through parallelization. This strategy might improve sorting speed; however, the type of data must be considered. In this particular case, a particle is in an active or inactive state. The order of the particles that are in the same state is not important, as long as they are all placed on the correct side of the sorted array. This allows for the array to be sorted in a single pass. If a parallel sorting algorithm is used instead, it is possible that performance could be improved. However, such improvement is not guaranteed. Possible improvements may be determined through experimentation.

In Option 4, parallelizing the generation of particles has a high potential of improving performance, but only under certain conditions. The first consideration is to determine the workload of all of the generators. If the memory buffer is almost always full, there won’t be any space for the generators to work. Therefore, spawning additional threads to execute the generators will only create unnecessary overhead. Every generator takes as much space as needed, and what is left is assigned to the next generator in the list. This could result in some threads executing generators just to find out that there is nothing for them to do.

### 5.1 Going further with parallelization

There are few more things worth mentioning that could affect performance. First is the issue of false sharing. A single particle structure size was 44 bytes. Given that the cache line size was 64 bytes, what was fetched from lower level memory was an entire particle structure, or part of a particle structure, that the current thread was working on, as well as part of a particle structure located right next to it. If two parallel threads each work on a single particle located next to each other, the modification of the acceleration vector inside one thread will invalidate the entire cache line. Essentially, this will cause cache miss on the other thread, even though the threads were assigned to different particles. This situation can be alleviated by aligning the particle structures to the 64-bytes boundary. However, this will also increase memory waste.

The second and preferred solution is to group multiple particle structures together and direct them to be processed as a single unit. This is what OpenMP does by default in the "parallel for" directive.

OpenMP is a very good framework, but it has disadvantages. OpenMP is built into a number of compilers that support it. However, not all compilers support OpenMP, or support an outdated version of OpenMP. A great alternative to OpenMP is the thread support library that was introduced with C++11 and should be supported in almost all C++ compilers currently available.

## 6 Vulkan Compute in a Modeling Particle System

This section addresses the topic of porting a CPU-based particle simulator onto the GPU using Vulkan compute. Vulkan compute is an integral part of the Vulkan API. Although most of the simulation will be moved onto the GPU, the sorting and generation of particles will still be kept on the CPU.

The goal of this section is to present how to set up the compute pipeline, instantiate more advanced shader input constructs, and show how to send frequently changing, but small, portions of data onto the GPU without using memory mapping.

This is a good moment to mention a tool that is extremely valuable when debugging Vulkan applications. The tool, RenderDoc, can be used to capture the current application state for inspection. The tool can be used to examine buffers content, shader input, textures, and much more. RenderDoc is automatically installed with VulkanSDK. Although not discussed in this document, it is highly recommended for readers to become familiar with this tool.

### 6.1 Using GPU memory buffer for computation and visualization

The first step is to repurpose the buffer structure that holds particle data. Among the buffer types available to use on a GPU is a buffer type called the shader storage buffer object (SSBO). This is a type of buffer that is similar to the uniform buffer. However, SSBOs are much larger in size than the uniform buffer and are writable from within the shader.

The internal storage, which was the standard C-style array contained by the Buffer class, is now replaced with an SSBO. Moreover, the same buffer memory region will be reused as a vertex buffer for rendering. The compute shader will modify the SSBO content, and then the renderer will use it as a vertex buffer object (VBO) to render the frame.

Up until now, the Buffer class was independent of Vulkan. Now, however, the entire application is dependent of Vulkan. This means that before the Model class can be instantiated, the Buffer class must be constructed. And before the Buffer class is constructed, the Vulkan virtual device must be created.

To make things appear in a more organized order, the buffer, the device, the AppInstance, and the rest of supporting code was moved into a new namespace called “base.” Now, instead of creating the Model first, the application starts from creating the AppInstance, device, and buffer objects (GPU_TP41). The code creating the vertex buffer has been moved out of ParticleElement into buffer (GPU_TP42). Note the change in the usage field: it now has two flags assigned, VERTEX_BUFFER_BIT and STORAGE_BUFFER_BIT. The rest of the procedure remains the same. The Buffer class now delivers the VkBuffer handle and interface to access the buffer on the CPU side (GPU_TP43). The constructed buffer is then used in instantiation of both the Model (GPU_TP44) and the ParticlesElement(GPU_TP45) objects.

### 6.2 Moving computation from the CPU to compute shader on the GPU

The Model class is where most of the changes will occur. In this version, the Model class will contain another pipeline which will execute the compute shader.

First, one of the biggest changes is in how the interactors are generally implemented. Although the interactor logic was moved into the compute shader, there is still a need for the mechanism to allow for the ability to dynamically specify the properties of each interactor in the application logic. Because of the structure of GLSL language, it is no longer possible to implement interactors using an abstract interface. This requires the interactors to be split by their type and provide specific data for all of them. To do this, we define a structure (GPU_TP46) called Setup to contain arrays for each type of interactor. Each array defines properties for an interactor and allows an arbitrary number of interactors of a given type to be present up to a specified upper boundary. The count variables specify the actual number of active interactors.

When submitting complex structures to buffer objects, it is critical to adhere to the layout rules that apply for the given type of buffer (Note the alignment statement in the structure field’s declaration (GPU_TP47)).  For uniform or shader storage buffer objects, these layouts are std140 and std430. Their full specification can be found in the Vulkan specification and GLSL language specification.

As in the CPU version, interactors were initialized before constructing the Model object (GPU_TP48). However, this time the initialization is based on populating the Setup structure. Later, the entire structure will be uploaded into the GPU during construction (GPU_TP49), making it available for the compute shader to access.

In the Vulkan API the compute stage and graphics stage cannot be bound into a single pipeline. As a result, two pipeline objects are available. Compared to the graphics pipeline, the compute pipeline (GPU_TP50) is less complicated. The primary concern is to define the proper pipeline layout. Beyond that, the process of creating the compute pipeline is nearly the same as creating the graphics pipeline.

Once the pipeline is established and the necessary data is ready to execute, the procedure starts recording commands into the command buffer for the compute pipeline (GPU_TP51). However, there are two concepts that are worth examining.

The first concept is “push constants.” Push constants are small regions of memory residing internally in the GPU designated for fast access. The advantage of using push constants is that data delivery can be scheduled right within the command buffer (GPU_TP52) without the need for memory mapping. The memory layout of push constants needs to be defined during pipeline construction, but the process is much simpler compared to the descriptor set (GPU_TP53).

The second concept is related to the division of workload. The number of elements is split into work groups that are scheduled to execute on the compute device. The size of the work group is specified within the compute shader (GPU_TP54). Then the API is given the number of work groups scheduled (GPU_TP55) for execution of the compute job. The sizes and number of workgroups are both limited by the hardware. Those limits can be checked by looking at the maxComputeWorkGroupCount and maxComputeWorkGroupSize fields, which are part of VkPhysicalDeviceLimits structure (which is a part of the VkPhysicalDeviceProperties structure that is obtained through calling vkGetPhysicalDeviceProperties). It is imperative to schedule a sufficient number work groups with appropriate size to cover the entire set of particles. The optimal choice of sizes is dictated by the specific hardware architecture and influenced by the compute shader code (e.g., the internal memory requirements).

### 6.3 Structure of the compute shader-oriented simulation

With the transition to the compute shader, the interactors take the form of two components. First are the interactor parameters which are delivered through the uniform buffer (GPU_TP56). The second is the function set wherein each function corresponds to a specific interactor and calculates the acceleration vector for the processed particle (GPU_TP57).

The function per iteration of the compute shader is to obtain a particle from SSBO using the global id index (GPU_TP58). The compute shader iterates through each interactor descriptor and invokes its function as many times as the count field indicates (GPU_TP59). Once all interactors have been executed, the acceleration vectors are summed and the compute shader invokes the Euler step function (GPU_TP60). The particle is then saved back to SSBO.

After the computing step is done, the renderer is invoked. The renderer uses the same buffer, but accesses memory through the vertex buffer interface, instead of SSBO, to render the scene.

## 7 Going Further

Building on this work, there are few options to consider that may improve performance.

### 7.1 Eliminate the CPU role in computations

Currently, the GPU compute shader only calculates the interactor’s influence on the particle. All sorting and generating of the particles were left to the CPU (see section 5). In the case of Intel's GPU, this approach is not penalized at all due to the uniform access to the memory. However, for other platforms, especially a discrete GPU, allocating buffers using the memory heap with most efficient access time is a must. This could mean that address space in such a heap might not be accessible from the CPU through memory mapping. In that case, the only way to access the data would be by copying buffers internally between heaps back and forth, or accessing it through the compute shader.

An approach in which buffers are copied between each other will almost certainly create a performance bottleneck. Therefore, the compute shader option seems more appealing. Initially, the sorting was left in its sequential form because of the unclear gains of parallel algorithms for this specific scenario. However, a GPU offers many more computing units which could make parallel sorting algorithms, like an “odd-even sort,” deliver better results.

There is still the issue of synchronization. An instance of the compute shader cannot start the next sorting pass before the previous one has completed. However, if only a single local work group is used, then the GLSL language delivers a set of Shader Invocation Control Functions (see GLSL specification) that will deliver the capability of setting up proper memory barriers.

Similarly, in the case of the generators, the biggest problem was the random number generator not being thread-safe and its dependence on the generator’s internal state. The randomize function can be ported into GLSL, and the coherence maintained using the GLSL atomic memory functions.

### 7.2 Parallelizing the performance path by double buffering

For this project, the approach was to first compute the scene and then render it sequentially. The complexity of the rendering in this case was fairly basic, and, therefore, its impact on performance was negligible. However, this will not always be the case. With more involved renderers it is necessary to attempt to perform computations and rendering in parallel. The Vulkan API was designed with this goal in mind and provides the means to synchronize program flow, but does not enforce it. For example, looking at where the program loop is waiting for the rendering function to finish (CPU_TP61). The part of the code responsible for presentation obviously has to wait, but the model does not. In fact, the model could start computing the next step as soon as the vertex data is delivered and only need to wait before entering the setVertexBufferData function. From here the application can be split into two threads and use a producer-consumer setup.

In the GPU version, instead of using a single SSBO, double buffering can be introduced. One buffer is used both as a render-input and compute-input. At the same time, the second buffer is populated by the compute shader with the Euler function output.

It is important to remember that there is an upper threshold to what can be achieved, which is limited by the capabilities of the hardware. The compute and render tasks executed on the same GPU will not always provide performance gains because of the finite number of compute units available.

## 8 Conclusion

Vulkan offers the ability to bypass the CPU bottleneck that exists in previous generations of graphics APIs. However, Vulkan has a steep learning curve and is more demanding when it comes to application design. Nonetheless, despite being very explicit, it is a very consistent and straightforward API.

It is worth remembering these few points which will help with application development, as well as allow achievement of better application performance:

  1. Start your development with the validation layers enabled and become familiar with tools like RenderDoc.
  2. Carefully design your application as you will have to make many decisions about various details.
  3. Pay attention to where your buffer memory is allocated as it might have significant performance implications.
  4. Understand the hardware you are working with. Not all the techniques will work equally well on every type of GPU. Although all Vulkan devices expose the same API, their properties and limitations might be fundamentally different from each other.

1

#### Product and Performance Information

1

Performance varies by use, configuration and other factors. Learn more at [www.Intel.com/PerformanceIndex](http://www.intel.com/PerformanceIndex).

Get Help

  * [Company Overview](/content/www/us/en/company-overview/company-overview.html)
  * [Contact Intel](/content/www/us/en/support/contact-intel.html)
  * [Newsroom](/content/www/us/en/newsroom/home.html)
  * [Investors](https://www.intc.com/)
  * [Careers](/content/www/us/en/jobs/jobs-at-intel.html)
  * [Corporate Responsibility](/content/www/us/en/corporate-responsibility/corporate-responsibility.html)
  * [Diversity & Inclusion](/content/www/us/en/diversity/diversity-at-intel.html)
  * [Public Policy](/content/www/us/en/company-overview/public-policy.html)
  * [ __ ](https://www.facebook.com/Intel)
  * [ __ ](https://twitter.com/intel)
  * [ __ ](https://www.linkedin.com/company/intel-corporation)
  * [ __ ](https://www.youtube.com/user/channelintel?sub_confirmation=1)
  * [ __ ](https://www.instagram.com/intel/)
  * © Intel Corporation
  * [ Terms of Use ](/content/www/us/en/legal/terms-of-use.html)
  * [ *Trademarks ](/content/www/us/en/legal/trademarks.html)
  * [ Cookies ](/content/www/us/en/privacy/intel-cookie-notice.html)
  * [ Privacy ](/content/www/us/en/privacy/intel-privacy-notice.html)
  * [ Supply Chain Transparency  ](/content/www/us/en/corporate-responsibility/statement-combating-modern-slavery.html)
  * [ Site Map ](/content/www/us/en/siteindex.html)
  * [ Do Not Share My Personal Information ](/#)

Intel technologies may require enabled hardware, software or service activation. // No product or component can be absolutely secure. // Your costs and results may vary. // Performance varies by use, configuration and other factors. // See our complete legal _[Notices and Disclaimers](https://edc.intel.com/content/www/us/en/products/performance/benchmarks/overview/#GUID-26B0C71C-25E9-477D-9007-52FCA56EE18C)_. // Intel is committed to respecting human rights and avoiding complicity in human rights abuses. See Intel’s _[Global Human Rights Principles_](https://www.intel.com/content/www/us/en/policy/policy-human-rights.html). Intel’s products and software are intended only to be used in applications that do not cause or contribute to a violation of an internationally recognized human right.

[ ![Intel Footer Logo](/content/dam/logos/intel-footer-logo.svg) ](/content/www/us/en/homepage.html)

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

[ ![Header image](rtr-header.png) ](http://www.realtimerendering.com/blog/)

  * [Blog](http://www.realtimerendering.com/blog/)
  * [Graphics books](books.html)
  * [Intersections](intersections.html)
  * [Portal](portal.html)
  * [Ray tracing](raytracing.html)
  * [Resources](index.html)
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
[Shirley 2016](https://psgraphics.blogspot.com/2016/02/new-simple-ray-box-test-from-andrew.html);  
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
on one side;([Moller jgt 2(2)](http://web.stanford.edu/class/cs277/resources/papers/Moller1997b.pdf));  
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
on one side;([Moller jgt 2(2)](http://web.stanford.edu/class/cs277/resources/papers/Moller1997b.pdf));  
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
[Moller jgt 2(2)](http://web.stanford.edu/class/cs277/resources/papers/Moller1997b.pdf);  
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
[Shirley 2016](https://psgraphics.blogspot.com/2016/02/new-simple-ray-box-test-from-andrew.html);  
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

Contact: [Eric](/cdn-cgi/l/email-protection#e18493888289a180828ccf8e9386)

* Game Physics Cookbook <https://gamephysicscookbook.com/>

* Stargazers · gszauer/GamePhysicsCookbook <https://github.com/gszauer/GamePhysicsCookbook>

* LearningUnrealEngine/Unit tests source notes.md at master · ibbles/LearningUnrealEngine

<https://github.com/ibbles/LearningUnrealEngine/blob/master/ Unit%20tests%20source%20notes.md>

* World Partition: Soft object pointers for actors that are in Data Layers or Spatially Loaded fail to resolve.

<https://udn.unrealengine.com/s/question/0D54z00008PRvloCAD/world-partition-soft-object- pointers-for-actors-that-are-in-data-layers-or-spatially-loaded-fail-to-resolve>

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