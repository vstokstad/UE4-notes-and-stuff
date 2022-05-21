* Animation Optimization | Unreal Engine Documentation
https://docs.unrealengine.com/4.26/en-US/AnimatingObjects/SkeletalMeshAnimation/Optimization/ <br/>
* Skeletal Mesh Animation System in Unreal Engine | Unreal Engine Documentation <br/> https://docs.unrealengine.com/5.0/en-US/skeletal-mesh-animation-system-in-unreal-engine/

* Unreal - Tick Functions, Delta Time, and the Task Graph <br/> https://www.casualdistractiongames.com/post/2018/12/10/unreal-tick-functions-delta-time-and-the- task-graph

* Using Async Collision Traces in Unreal Engine 4 - Bryan Corell - Medium <br/> https://web.archive.org/web/20200530051219/https://medium.com/@bryan.corell/using-async- collision-traces-in-unreal-engine-4-2cc312c825f5

* https://github.com/ajweeks/FlexEngine <br/> https://github.com/ajweeks/FlexEngine

* Flex Engine <br/> http://ajweeks.com/flex-engine/

  * [Manual](../Manual/index.html)
  * [Scripting API](../ScriptReference/index.html)

  * [unity3d.com](https://unity.com/)

Version: **2021.3**

  * Supported
  * Legacy

Language : English

  * [English](/Manual/class-ComputeShader.html)
  * [中文](/cn/current/Manual/class-ComputeShader.html)
  * [日本語](/ja/current/Manual/class-ComputeShader.html)
  * [Español](/es/current/Manual/class-ComputeShader.html)
  * [한국어](/kr/current/Manual/class-ComputeShader.html)
  * [Русский](/ru/current/Manual/class-ComputeShader.html)

## Unity Manual

Version: 2021.3Select a different version

Language : English

  * [English](/Manual/class-ComputeShader.html)
  * [中文](/cn/current/Manual/class-ComputeShader.html)
  * [日本語](/ja/current/Manual/class-ComputeShader.html)
  * [Español](/es/current/Manual/class-ComputeShader.html)
  * [한국어](/kr/current/Manual/class-ComputeShader.html)
  * [Русский](/ru/current/Manual/class-ComputeShader.html)

  * [ Unity User Manual 2021.3 (LTS)](UnityManual.html)
  * [Graphics](Graphics.html)
  * [ Shaders](Shaders.html)
  * [ Shaders core concepts](ShadersOverview.html)
  * Compute shaders

Replacing shaders at runtime

Error and loading shaders

# Compute shaders

[Switch to Scripting](../ScriptReference/ComputeShader.html)

Compute shaders are **shader**A program that runs on the GPU. [More info](Shaders.html)  
See in [Glossary](Glossary.html#Shader) programs that run on the GPU, outside of the normal rendering pipeline.

They can be used for massively parallel GPGPU algorithms, or to accelerate parts of game rendering. In order to efficiently use them, an in-depth knowledge of GPU architectures and parallel algorithms is often needed; as well as knowledge of [DirectCompute](http://msdn.microsoft.com/en-us/library/windows/desktop/ff476331.aspx), [OpenGL Compute](https://www.khronos.org/opengl/wiki/Compute_Shader), [CUDA](http://en.wikipedia.org/wiki/CUDA), or [OpenCL](http://en.wikipedia.org/wiki/OpenCL).

Compute shaders in Unity closely match [ DirectX](https://en.wikipedia.org/wiki/DirectX) 11 DirectCompute technology. Platforms where compute shaders work:

  * Windows and Windows Store, with a DirectX 11 or DirectX 12 graphics API and Shader Model 5.0 GPU

  * macOS and **iOS**Apple’s mobile operating system. [More info](iphone.html)  
See in [Glossary](Glossary.html#iOS) using [Metal graphics](https://developer.apple.com/metal/) API

  * Android, Linux and Windows platforms with [Vulkan](https://www.khronos.org/vulkan/) API

  * Modern [OpenGL](https://www.opengl.org/) platforms (OpenGL 4.3 on Linux or Windows; OpenGL ES 3.1 on Android). Note that Mac OS X does not support OpenGL 4.3

  * Modern consoles

Compute shader support can be queried runtime using [SystemInfo.supportsComputeShaders](../ScriptReference/SystemInfo-supportsComputeShaders.html).

## Compute shader Assets

Similar to [shader assets](class-Shader.html), compute shader assets are files in your project. with a _.compute_ file extension. They are written in DirectX 11 style [HLSL](http://msdn.microsoft.com/en-us/library/windows/desktop/bb509561.aspx) language, with a minimal number of #pragma compilation directives to indicate which functions to compile as compute shader kernels.

Here’s a basic example of a compute shader file, which fills the output texture with red:
    
    
    // test.compute
    
    #pragma kernel FillWithRed
    
    RWTexture2D<float4> res;
    
    [numthreads(1,1,1)]
    void FillWithRed (uint3 dtid : SV_DispatchThreadID)
    {
        res[dtid.xy] = float4(1,0,0,1);
    }
    
    
    
    
    
    
    The language is standard DX11 HLSL, with an additional #pragma kernel FillWithRed directive. One compute shader Asset file must contain at least onecompute kernel that can be invoked, and that function is indicated by the #pragma directive. There can be more kernels in the file; just add multiple #pragma kernel lines.
    
    
    
    
    
    When using multiple #pragma kernel lines, note that comments of the style // text are not permitted on the same line as the #pragma kernel directives, and cause compilation errors if used.
    
    
    
    
    
    The #pragma kernel line can optionally be followed by a number of preprocessor macros to define while compiling that kernel, for example:
    
    
    
    
    
    
    #pragma kernel KernelOne SOME_DEFINE DEFINE_WITH_VALUE=1337
    #pragma kernel KernelTwo OTHER_DEFINE
    // ...
    
    
    
    
    
    
    ## Invoking compute shaders
    
    
    
    
    
    In your script, define a variable of ComputeShader type and assign a reference to the Asset. This allows you to invoke them with [ComputeShader.Dispatch](../ScriptReference/ComputeShader.Dispatch.html) function. See Unity documentation on [ComputeShader class](../ScriptReference/ComputeShader.html) for more details.
    
    
    
    
    
    Closely related to compute shaders is a [ComputeBuffer](../ScriptReference/ComputeBuffer.html) class, which defines arbitrary data buffer (“structured buffer” in DX11 lingo). [Render Textures](../ScriptReference/RenderTexture.html)A special type of Texture that is created and updated at runtime. To use them, first create a new Render Texture and designate one of your Cameras to render into it. Then you can use the Render Texture in a Material just like a regular Texture. [More info](class-RenderTexture.html)  
    See in [Glossary](Glossary.html#RenderTexture) can also be written into from compute shaders, if they have “random access” flag set (“unordered access view” in DX11). See [RenderTexture.enableRandomWrite](../ScriptReference/RenderTexture-enableRandomWrite.html) to learn more about this.
    
    
    
    
    
    ## Texture samplers in compute shaders
    
    
    
    
    
    Textures and samplers aren’t separate objects in Unity, so to use them in compute shaders you must follow one of the following Unity-specific rules:
    
    
    
    
    
    
    
      * Use the same name as the Texture name, with sampler at the beginning (for example, Texture2D MyTex; SamplerState samplerMyTex). In this case, the sampler is initialized to that Texture’s filter/wrap/aniso settings.
    
    
    
      * Use a predefined sampler. For this, the name has to have Linear or Point (for filter mode) and Clamp or Repeat (for wrap mode). For example, SamplerState MyLinearClampSampler creates a sampler that has Linear filter mode and Clamp wrap mode.
    
    
    
    
    
    
    For more information, see documentation on [Sampler States](SL-SamplerStates.html).
    
    
    
    
    
    ## Cross-platform support
    
    
    
    
    
    As with regular shaders, Unity is capable of [translating](shader-compilation.html) compute shaders from HLSL to other shader languages. Therefore, for the easiest cross-platform builds, you should write compute shaders in HLSL. However, there are some factors that need to be considered when doing this.
    
    
    
    
    
    ### Cross-platform best practices
    
    
    
    
    
    DirectX 11 (DX11) supports many actions that are not supported on other platforms (such as [Metal](https://developer.apple.com/metal/) or [OpenGL ES](https://www.opengl.org/)). Therefore, you should always ensure your shader has well-defined behavior on platforms that offer less support, rather than only on DX11. Here are few things to consider:
    
    
    
    
    
    
    
      * Out-of-bounds memory accesses are bad. DX11 might consistently return zero when reading, and read some writes without issues, but platforms that offer less support might crash the GPU when doing this. Watch out for DX11-specific hacks, buffer sizes not matching with multiple of your thread group size, trying to read neighboring data elements from the beginning or end of the buffer, and similar incompatibilities.
    
    
    
      * Initialize your resources. The contents of new buffers and Textures are undefined. Some platforms might provide all zeroes, but on others, there could be anything including NaNs. 
    
    
    
      * Bind all the resources your compute shader declares. Even if you know for sure that the shader does not use resources in its current state because of branching, you must still ensure a resource is bound to it.
    
    
    
    
    
    
    ### Platform-specific differences
    
    
    
    
    
    
    
      * 
    [Metal](https://developer.apple.com/metal/) (for iOS and tvOS platforms) does not support atomic operations on Textures. Metal also does not support GetDimensions queries on buffers. Pass the buffer size info as constant to the shader if needed.
    
    
    
      * 
    [OpenGL ES](https://www.opengl.org/) 3.1 (for (Android, iOS, tvOS platforms) only guarantees support for 4 compute buffers at a time. Actual implementations typically support more, but in general if developing for OpenGL ES, you should consider grouping related data in structs rather than having each data item in its own buffer.
    
    
    
    
    
    
    ## HLSL-only or GLSL-only compute shaders
    
    
    
    
    
    Usually, compute shader files are written in [HLSL](https://en.wikipedia.org/wiki/High-Level_Shading_Language), and compiled or translated into all necessary platforms automatically. However, it is possible to either prevent translation to other languages (that is, only keep HLSL platforms), or to write [GLSL](https://en.wikipedia.org/wiki/OpenGL_Shading_Language) compute code manually.
    
    
    
    
    
    The following information only applies to HLSL-only or GLSL-only compute shaders, not cross-platform builds. This is because this information can result in compute shader source being excluded from some platforms. 
    
    
    
    
    
    
    
      * Compute shader source surrounded by CGPROGRAM and ENDCG keywords is not processed for non-HLSL platforms.
    
    
    
      * Compute shader source surrounded by GLSLPROGRAM and ENDGLSL keywords is treated as GLSL source, and emitted verbatim. This only works when targeting OpenGL or GLSL platforms. You should also note that while automatically translated shaders follow HLSL data layout on buffers, manually written GLSL shaders follow GLSL layout rules.
    
    
    
    
    
    
    ## Variants and keywords
    
    
    
    
    
    You can use keywords to produce multiple variants of compute shaders, the same as you can for graphics shaders.
    
    
    
    
    
    For general information on variants, see [Shader variants](shader-variants.html)A verion of a shader program that Unity generates according to a specific combination of shader keywords and their status. A Shader object can contain multiple shader variants. [More info](shader-variants.html)  
    See in [Glossary](Glossary.html#Shadervariant). For information on how to implement these features in compute shaders, see [Declaring and using shader keywords in HLSL](SL-MultipleProgramVariants.html) and the [ComputeShader API documentation](../ScriptReference/ComputeShader.html).
    
    
    
    
    
    
    
    
    
    
    
    
    
    Replacing shaders at runtime
    
    
    
    
    
    
    
    
    
    
     Error and loading shaders
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    Copyright © 2021 Unity Technologies. Publication Date: 2022-05-15.
    
    
    
    
    
    [Tutorials](https://learn.unity.com/)[Community Answers](https://answers.unity3d.com)[Knowledge Base](https://support.unity3d.com/hc/en-us)[Forums](https://forum.unity3d.com)[Asset Store](https://unity3d.com/asset-store)[Terms of use](https://docs.unity3d.com/Manual/TermsOfUse.html)
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    

* https://link.medium.com/Ho9inlRbdqb <br/> https://link.medium.com/Ho9inlRbdqb
