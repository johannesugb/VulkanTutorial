# Vulkan Tutorial set-up for Visual Studio 2019

Source from https://vulkan-tutorial.com       

The current state of the single implementation file [`source/vulkan_tutorial.com`](source/vulkan_tutorial.com) is set to the state of the ["Loading models"](https://vulkan-tutorial.com/Loading_models) chapter of Alexander Overvoorde's [vulkan-tutorial.com](https://vulkan-tutorial.com).

Running the application will show the following scene: 

![Vulkan Tutorial's "Loading models" scene](drawing_model.png)

Everything is readily set-up including:
* Source Code 
* External Dependencies
  * tinyobjloader
  * stb_image
  * GLM
  * GLFW
* Ready-to-use Visual Studio 2019 solution including a Custom Build Step which:
  * Deploys models and textures to the target directory
  * Compiles shaders to SPIR-V using `glslc.exe` and deploys them to the target directory
    
## Setup

1. Ensure to have a [Vulkan SDK](https://www.lunarg.com/vulkan-sdk/) installed.
2. Ensure that your `VULKAN_SDK` environment variable points to the Vulkan SDK's install location.      
   The custom build step needs to find `glslc.exe` in `$(VULKAN_SDK)\Bin\`
3. Checkout this repository.
4. Open [`visual_studio/vulkan_tutorial.sln`].
5. Build and run.
