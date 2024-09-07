# PBRify_Remix
My custom (ethical) set of AI models to upscale textures and generate PBR maps from diffuse or albedo texture maps. Intended for use with RTX Remix

## 🚀 Support my work!


Any donations help pay training costs + other living costs that would hinder my work on these models. Any donation helps, even if it's just $1!

(The name won't be Kim on the checkout page, that's okay)

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/J3J3BCC3L)


## Features
This is a complete set, consisting of a pre-made chain for chaiNNer & 3 models. These models do the following:
1. Upscale
2. Generate Normal Map
3. Generate Roughness Map
4. Generate Height Map (Disabled by default)


## Guide
1. Download [chaiNNer](https://chainner.app/) and install the dependencies in the top right
2. Download the [latest release](https://github.com/Kim2091/PBRify_Remix/releases) and extract.
3. Open the `.chn` file in chaiNNer
4. Set an input and output directory for the textures
5. Load the model files by following the notes in the chain (refer to the image for more details)
6. Press the green run button at the top!
7. Ingest the saved textures in Remix's Ingestion tab


### ComfyUI
You can also use PBRify in ComfyUI thanks to Nvidia! They have an implementation of it in their official repository here: <https://github.com/NVIDIAGameWorks/ComfyUI-RTX-Remix>

This implementation allows you to use PBRify directly with the toolkit. You can select textures in the toolkit to process, send them to ComfyUI to be processed with PBRify, then sent back to be added 🙂

<details>

<summary>Steps:</summary>

- These steps assume you've already installed [ComfyUI](https://github.com/comfyanonymous/ComfyUI), the [ComfyUI-RTX-Remix](https://github.com/NVIDIAGameWorks/ComfyUI-RTX-Remix) extensions, and the [RTX Remix toolkit](https://www.nvidia.com/en-us/geforce/rtx-remix/) with an existing project file. Look in the [RTX Remix Discord server](https://discord.gg/rtxremix) for further details.

1. Download PBRify's latest package from [here](https://github.com/Kim2091/PBRify_Remix/releases)
2. Open the zip file
3. Find the Models folder
4. Extract the contents of the folder to `ComfyUI\models\upscale_models`
5. Open the RTX Remix Toolkit
6. Open your project
7. Select the objects with textures you want to upscale
8. Launch ComfyUI
9. Load the workflow using the `rtx_remix_pbrify_workflow.png` file located in `ComfyUI\custom_nodes\ComfyUI-RTX-Remix\workflows` and hit "Queue Prompt"
10. It will now upscale and generate PBR textures. Simply switch back to the toolkit to observe the improvement

Tips:
- The default displacement value is far too strong. Set it per texture to 0.1 or even less, such as 0.05
</details>

## Tips & Additional Info:
- You can use the upscaler without generating PBR by disabling the Load Model nodes for Roughness and Normal maps (the switch in the bottom left of each node)
  - The upscaling model is trained to remove noise, DXT1 compression, dithering, and oversharpening/halos
- The chain will save your textures into a single output folder. They're labelled with the original texture name.
- These were trained exclusively on high quality CC0 content from ambientCG, complying with their license. This makes it an ethical upscaler that you can use without concern 🙂
- These models are licensed as CC0.

![alt text](https://github.com/Kim2091/PBRify_Upscaler/blob/main/Tutorial.png)
