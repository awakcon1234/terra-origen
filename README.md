# WIP Config pack

An overworld configuration pack for terra 6.4 and higher. It is based on the default terra overworld config pack v2.0, which you can find 
[here](https://github.com/PolyhedralDev/TerraOverworldConfig/tree/2.0). A lot of content is used from the default pack, especially regarding the terrain features such as trees, flora and palettes.

<Name here> focuses on adding a new and more creative / diverse terrain generation, without using any new blocks or items. This means that it is compatible with vanilla installations. 

You can find Terra - the main project this config pack is designed for
[here](https://github.com/PolyhedralDev/Terra).

Huge thanks to everyone on the terra discord that has helped with my countless questions and with giving feedback. Most notably to Astrash and Aureus, without them this pack wouldn't have made it anywhere.

Most top level settings, such as biome and river sizes, can be found in the file [costumization.yml](customization.yml)

---

## Biome distribution

A lot of work has gone into making sure that biomes are in the desired size and form. This allows designing landform features in biomes with somewhat specific sizes and then makes sure that the terrain's themselfes are not too big/small or squashed.

On a basic level, terrains are placed using cellular noise. This means that most biomes have a similar size and form. Those cells are then split into land and ocean cells, based on a continnental value *in the middle of the cell*. This means that land cells close to the ocean will keep their full size, without being cut off at the point where the "continental" equation would transition into oceans. The same also applies to ocean biomes. 

To find and place coast biomes, the edge between the cells of ocean and land are used. Then the coasts themselfes are split into cells aswell, however using a different seed. The coasts are also split into 3 categories: none, small and wide, resulting in some coasts either being not there at all (the oceans goes directly against the land biomes), or being small or very wide.

Rivers are spread on all biomes that have the "USE_RIVER" tag, and a generally a bit more wide and deep than vanilla rivers, making it easier to travel via boat. Some biomes also have river variants, which usually generate the river as a caved version through larger mountains so the river doesn't have to fully cut through large mountains.

## Currently available biomes

Here is a full list of all biomes used in <pack name>

### Land

### Cave

### Coast

### Ocean

### Special

## Navigating through the config

This pack is organized into many top level directories, each containing configs
specific to a different domain of configuration:

- `biomes`
  Where all biome configs are defined.

- `biome-distribution`
  Contains configuration files related *where* biomes generate.

- `structures`
  Where all files loaded as structures are stored. (This includes things like
  trees, boulders, flower patches, etc.)

- `features`
  Where all feature configs go - These determine *how structures are
  generated in the world.*

- `palettes`
  Contains all palette configs - These are used by biomes to determine what
  blocks make up the base terrain.

- `math`
  Common mathematical functions used in the pack as well as generic noise 
  samplers are defined here.

- `*/rearth/`
  Completely new content that has been added, which is not available in the default config pack. These subfolders are where you'll find most of the new stuff.

For more in-depth explanations of each directory's files and subdirectories, you
can refer to their respective README files.

## Customization

### How do I make biomes larger / smaller?

You can find some easy to modify parameters in the [`meta.yml`](./meta.yml) file
under `biome-distribution`, which control the scales of different areas of biome
distribution.

### How do I remove all oceans / all land / all hot biomes / etc?

This pack comes with several biome distribution presets, which can be chosen
within the [`pack.yml`](./pack.yml) file. If none of these presets do exactly
what you want, you can further modify biome distribution presets with alternate
sources and stages. Check out the
[`biome-distribution/presets/default.yml`](./biome-distribution/presets/default.yml)
config for these alternative sources and stages.

### Where can I learn more about configuration?

If you want more in-depth customization, or simply just want to know what makes
this pack tick, you can check out the
[config development](https://terra.polydev.org/config/development/index.html)
section of the Terra wiki to learn more.
