This folder contains additional files that may suit your needs better.


### Alternate_Models

`4x-PBRify_UpscalerSPAN_Neutral.pth` - A derivative of V4 of my SPAN upscaler, but with neutral colors. Essentially, it has no color shifting at all. This is good for upscaling specular, roughness, normal maps, etc. but not as good for upscaling albedos.


### Old_Models

`4x-PBRify_UpscalerSPANV2.pth` - My first released PBRify upscaler. This one has some major issues, namely color shifting & lack of detail

`4x-PBRify_UpscalerSPANV3.pth` - The second release of my PBRify SPAN upscaler. This one improved on V2 a LOT with additional detail, deblurring, and colors, but is also oversharpened and unbalanced on many textures

`4x-PBRify_UpscalerSPANV3.pth` - The third release of my PBRify SPAN upscaler. This one is an interpolation of V3 and a beta V3.5. It's a huge improvement from V4, but was rendered outdated by 4x-PBRify_UpscalerSIR-M_V2

`1x-PBRify_Normal.pth` - My initial version of the normal map models

`1x-PBRify_NormalV2.pth` - My short lived second version. This was interpolated with V1 to make V3, since it provides a great balance.

### Chains

`PBR Upscale Chain_6GB_VRAM.chn` - This is a version of the main chain that's intended for 6 GB VRAM GPUs. This is not guaranteed to be updated regularly. It was last updated on 6-5-24 (mm-dd-yy)

`PBR Upscale Chain_With_Color_Fix` - This is the chain from release 1.6.2. This includes Wavelet Color Fix on both the RGB and Alpha layers to ensure 100% correct color reproduction. It is quite intensive however!
