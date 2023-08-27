# WIP Config pack

An overworld configuration pack for terra 6.4 and higher. It is based on the default terra overworld config pack v2.0, which you can find 
[here](https://github.com/PolyhedralDev/TerraOverworldConfig/tree/2.0). A lot of content is used from the default pack, especially regarding the terrain features such as trees, flora and palettes.

PLACEHOLDER focuses on adding a new and more creative / diverse terrain generation, without using any new blocks or items. This means that it is compatible with vanilla installations. 

You can find Terra - the main project this config pack is designed for
[here](https://github.com/PolyhedralDev/Terra).

Huge thanks to everyone on the terra discord that has helped with my countless questions and with giving feedback. Most notably to Astrash and Aureus, without them this pack wouldn't have made it anywhere.

Most top level settings, such as biome and river sizes, can be found in the file [costumization.yml](customization.yml)

---

## Biome distribution

Considerable effort has been invested in ensuring that biomes are crafted to the desired size and shape. This enables the design of landform features within biomes of relatively specific dimensions, while also preventing the terrain itself from becoming overly large, small, or distorted.

At a fundamental level, biomes are established using cellular noise, resulting in a uniform size and shape for most biomes. These cellular units are subsequently categorized into land and ocean cells, determined by a continental value situated at the center of each cell. This approach ensures that land cells adjacent to oceans maintain their full size, without being truncated at the point where the "continental" equation would transition into ocean cells. This principle is also extended to ocean biomes.

The identification and placement of coastal biomes involve utilizing the boundary between ocean and land cells. Subsequently, the coastal areas are divided into discrete units using a distinct seed. Furthermore, coastal zones are classified into three categories: none, narrow, and wide. This results in some coastlines either being absent altogether (e.g. the ocean directly borders land biomes) or being categorized as narrow or significantly wider.

Rivers are added throughout all biomes tagged with "USE_RIVER". These rivers are generally broader and deeper than standard vanilla rivers, allowing smoother boat navigation. Certain biomes also feature river variants, often generating rivers that meander through cavernous sections of large mountains, thus negating the need for the river to cut entirely through these substantial landforms.

## Currently available biomes

Here is a full list of all biomes used in PLACEHOLDER. Note that some biomes are already included in the default terra overworld config pack, and will be marked as such.

### Land

** Black Forest **

Inspired by the german black forest, this mountainy biome has is covered in spruce and birch trees. Also included some flat clearing spread throughout the forest. Some of those clearing have a small change of turning into a mountain lake.

** Carving Creaks **

An environment made of very high terracotta plateous, with large canyons and rivers cutting through it. The edges also have a slight terrace visisble.

** Fossilized Fenlands **

The dinosaur biome. Mostly flat with some segmented elevations. Can spawn dinosaur fossils, which usually have multiple "rib" segments and a chance to include a giant head on the front.

** Frosty Fingers **

Cold environment, with weaving snow and ice dunes. Also includes large snow spikes in the valleys between the snow dunes.

** Mountain Mirrors **

The mountain mirrors consist of huge mountains, with multiple terrace layers and steep walls inbetween them. The walls are covered with ice and can result in a mirror-like appearance. Between mountains there often appear frozen lakes. Also has frozen rivers that go through the higher parts of mountains using frozen cave rivers. On the flatter parts of the terrain there can spawn snow-covered trees and ice spikes.

** Canopy Cascades **

Jungle version of the mountain mirrors. Features huge mountains with terraces along it. Usually covered with large jungle trees and a few lush lakes at the bottom.

** Lush Loops **

A lush jungle environment, with massive eye-catching stone arches looping through the skies.

** Mesa Monuments **

Covered by giant terracotta pillars, the mesa monuments biome is a warm badlands / desert mix. The main feature are the big terracotta pillars in it, which can reach up to 100 blocks into the sky.

** Murky Marshlands **

Imagine a unique and exotic rendition of the familiar vanilla swamp. This variant is blanketed by imposing, shadowy trees that exude a mysterious aura. The ground seamlessly blends the realms of water and land, creating a captivating environment. On the land, the terrain showcases a series of interconnected, level expanses that intertwine, each marked by sharp transitions in elevation.

** Pillow Plains **

Split into a high border segment and a low inner segment, the pillow plains is marked by its small pillars through a green valley. Due to the low height of the inner segment, there are no rivers in this biome, though this will be changed in the future by adding a special low river variant.

** Redwood Forests **

The Redwood Forests are covered by giant redwood trees. Similar to the black forests, they also feature flat clearing and lakes in between their forest-covered mountains.

** Secluded Valley **

At a first glance, the secluded valley is just a large and flat sunflower field. However, there are also huge valleys with a small entrance hidden spread throughout this biome. The valleys containt cherry trees and have a small chance to spawn a giant cherry tree in the middle.

** Verdant Valleys **

The verdant valley is a mostly flat valley with sparse acacia trees. The valley is surrounded by smaller hills which usually have small steep patches with a darker surface.

** Vertical Vistas **

Huge, towering green mountains. The often are high enough that their peak is covered in snow. At the bottom of these mountains, there is also often a small lake. Few trees and boulders can be found on the surface.

** WIP **

More biomes will follow soon.

### Cave

** Inferno Isles **

Giant cave biome that usually is found around -20 to +40. Contains a big lava lake with interconnected platforms hanging on chains over it. The cave roof is covered with glowing plants.

** TODO **

### Coast

** Marine Monolits **

Towering cliffs biome, only found at the bigger coasts. The biome has a mostly flat area, which is held by large white pillars that reach deep into the water.

** TODO **

### Ocean

** TODO **

### Special

** Sinkholes **

Sinkhole can be found anywhere in the world, ignoring the usual biome cell spawns. However, they are quite rate. They reach down to Y -40 and have steep cliffs and are usually streched at an angle. There currently are 3 sinkhole variations:

** Jungle Sinkhole**

Contains a warm surface with big jungle trees covering it.

** Forest Sinkhole **

Contains mossy stone walls and a diverse mix of trees covering the bottom of the sinkhole.

** Frozen Sinkhole **

Cold version of the sinkhole. Has a snowy surface with ice spikes on it.

** TODO **

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
