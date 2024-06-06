# PBRify_Remix
My custom (ethical) set of AI models to upscale textures and generate PBR maps. Intended for use with RTX Remix

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

### Extra info:
- You can use the upscaler without generating PBR by disabling the Load Model nodes for Roughness and Normal maps (the switch in the bottom left of each node)
  - The upscaling model is trained to remove noise, DXT1 compression, dithering, and oversharpening/halos
- The chain will save your textures into a single output folder. They're labelled with the original texture name.
- These were trained exclusively on high quality CC0 content from ambientCG, complying with their license. This makes it an ethical upscaler that you can use without concern 🙂
- These models are licensed as CC0.

![alt text](https://github.com/Kim2091/PBRify_Upscaler/blob/main/Tutorial.png)
