## Additional Technical Details
- PBRify is trained on the most efficient architectures per the quality provided that I'm aware of
  - DAT2 for the upscaler, and SPAN for the PBR generation

The training process was the following:

Upscaler:

- Gather textures
- Sort and separate
- Tile textures
- Degrade using datasetDestroyer (wtp or my own)
- Apply DXT1 compression through chaiNNer
- train with [traiNNer-redux](https://github.com/the-database/traiNNer-redux)

Normal, Roughness, Height Map Generators:
- Gather textures
- Sort and separate
- Tile textures
- train with [traiNNer-redux](https://github.com/the-database/traiNNer-redux)

Textures were sourced from ambientCG and PolyHaven. To help support them and also make gathering easier, I donated to their Patreon (or equivalent) pages.

### Height Maps
The height map generator is disabled by default due to the current lack of a "delighting" pipeline within PBRify. 

### Delighting
The goal of a delighting pipeline is to remove baked lighting from textures. This lighting is what causes the majority of issues with PBR and height map generation. 

It's also incredibly difficult to pull off however. I trained an experimental delighting model and it simply does not perform well enough to be worthwhile. I'm considering adding it for height map generation specifically.
