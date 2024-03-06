![Origen](https://github.com/Rearth/UnnamedTerraConfigPack/assets/10100603/0657306f-4f00-4003-b3da-33e32e99e855)

> This pack is still in a testing phase, so bugs and issues are to be expected

An overworld configuration pack for minecraft 1.20 and terra 6.4 and higher. It is based on the default Terra overworld config pack v2.0, which you can find 
[here](https://github.com/PolyhedralDev/TerraOverworldConfig/tree/2.0). A lot of content is used from the default pack, especially regarding the terrain features such as trees, flora and palettes.

Origen focuses on adding a new and more creative / diverse terrain generation, without using any new blocks or items. This means that it is compatible with vanilla installations.

You can find Terra - the main project this config pack is designed for
[here](https://github.com/PolyhedralDev/Terra).

Huge thanks to everyone on the Terra Discord that has helped with my countless questions and with giving feedback. Most notably to Astrash and Aureus, without them this pack wouldn't have made it anywhere.  Some of the screenshots are taken with the [Bare Bones texture pack](https://modrinth.com/resourcepack/bare-bones).

Most top level settings, such as biome and river sizes, can be found in the file [customization.yml](customization.yml).

## Installation

Origen is just a config pack for the Terra mod. Make sure you have Terra installed first. You can find it on [Modrinth](https://modrinth.com/plugin/terra). 

You can grab the latest release from the Github [releases section](https://github.com/Rearth/Origen/releases/latest), from there just download the origen-v\*.\*.\*.zip file, and copy it to your Terra pack directory. For more information on installing Terra config packs, see the [docs here](https://terra.polydev.org/config/pack-installation.html).

---

## Biome distribution

Considerable effort has been invested in ensuring that biomes are renderer in the desired size and shape. This enables the design of landform features within biomes of relatively specific dimensions, while also preventing the terrain itself from becoming overly large, small, or distorted.

At a fundamental level, biomes are established using cellular noise, resulting in a uniform size and shape for most biomes. These cellular units are subsequently categorized into land and ocean cells, determined by a continental value situated at the center of each cell. This approach ensures that land cells adjacent to oceans maintain their full size, without being truncated at the point where the "continental" equation would transition into ocean cells. This principle is also extended to ocean biomes.

The identification and placement of coastal biomes involve utilizing the boundary between ocean and land cells. Subsequently, the coastal areas are divided into discrete units using a distinct seed. Furthermore, coastal zones are classified into three categories: none, narrow, and wide. This results in some coastlines either being absent altogether (e.g. the ocean directly borders land biomes) or being categorized as narrow or significantly wider.

Rivers are added throughout all biomes tagged with "USE_RIVER". These rivers are generally broader and deeper than standard vanilla rivers, allowing smoother boat navigation. Certain biomes also feature river variants, often generating rivers that meander through cavernous sections of large mountains, thus negating the need for the river to cut entirely through these substantial landforms.

## Currently available biomes

Here is a full list of all biomes used in Origen. Note that some biomes are already included in the default terra overworld config pack, and will be marked as such.

### Land

**Foliage Fortress**

> ![2023-09-04_21 59 24_cropped](https://github.com/Rearth/Origen/assets/10100603/e7210ff4-d62d-42c8-93c2-39925123cdc5)
Giant plateau with sharp overhangs surrounding it. These overhangs are supported by large stone pillars. A savanna-like environment is found at and around the bottom of the plateau, while the top is covered with all sorts of trees.

**Gloomy Gorge**

> ![2023-10-24_22 53 48_2](https://github.com/Rearth/Origen/assets/10100603/91e68bbe-5a3b-408b-93a8-b93b78b782a0)
High mountains, with deep valleys and dark, eroded cliffs running through them. The mountainsides are glowing in the dark, and the whole environment is surrounded by all kinds of lush vegetation.

**Snowy Spires**

> ![2023-10-20_15 56 28](https://github.com/Rearth/Origen/assets/10100603/7a63755b-334c-4309-9ffc-8a6c913d5c8a)
A snowy mesa biome, with giant terracotta pillars. The sandy ground is mostly covered in snow. The pillars are partialy frozen, with large ice chunks often connecting them, and icicles hanging from them.

**Black Forest**

> ![2023-08-27_16 23 50](https://github.com/Rearth/UnnamedTerraConfigPack/assets/10100603/6e802a05-1993-4720-a23c-64bbfbe99782)
Inspired by the german black forest, this mountainy biome has is covered in spruce and birch trees. Includes flat clearings spread throughout the forest. Some of those clearings have a small chance of turning into a mountain lake.

**Carving Creaks**

> ![2023-08-07_23 58 53](https://github.com/Rearth/UnnamedTerraConfigPack/assets/10100603/73406873-ccb2-4d3c-aa7a-71e86f8a39dd)
An environment made of very high terracotta plateous, with large canyons and rivers cutting through it. The edges also have a slight terrace visible.

**Fossilized Fenlands**

> ![2023-08-09_23 40 35](https://github.com/Rearth/UnnamedTerraConfigPack/assets/10100603/c8fb50da-f7cd-4222-8200-b8dd74e2b6f6)
The dinosaur biome. Mostly flat with some segmented elevations. Can spawn dinosaur fossils, which usually have multiple "rib" segments and a chance to include a giant head on the front.

**Arid Arboretum**

> ![2023-10-25_22 09 37](https://github.com/Rearth/Origen/assets/10100603/cd92b628-a35d-456c-9b97-69e9bf12e609)
Badlands biome that has been overtaken by an evergreen forest. The arid ground is a mix of grass and sand, with granite patches and giant terracotta pillars, covered in vegetation.

**Bamboo Basins**

> ![2023-08-29_17 29 53](https://github.com/Rearth/Origen/assets/10100603/88610a27-3f33-4464-bc33-3a337c14f10b)
This biome usually has features a central mountain without any steep cliffs. Multiple rivers flow out from the lakes at the mountain top, and the surfance is covered with eucalyptus trees and bamboo. The ground has both grass and podzol.

**Frosty Fingers**

> ![2023-08-27_16 40 21](https://github.com/Rearth/UnnamedTerraConfigPack/assets/10100603/44ad0eb0-71d7-4aa4-a6b4-596d9fd4e32c)
Cold environment, with weaving snow and ice dunes. Also includes large snow spikes in the valleys between the snow dunes.

**Mountain Mirrors**

> ![2023-08-27_14 59 37](https://github.com/Rearth/UnnamedTerraConfigPack/assets/10100603/21589086-f37c-4209-9e0d-7c980d9b6b64)
The mountain mirrors consist of huge mountains, with multiple terrace layers and steep walls inbetween them. The walls are covered with ice and can result in a mirror-like appearance. Between mountains there often appear frozen lakes. Also has frozen rivers that go through the higher parts of mountains using frozen cave rivers. On the flatter parts of the terrain there can spawn snow-covered trees and ice spikes.

**Canopy Cascades**

> ![2023-08-27_12 22 30](https://github.com/Rearth/UnnamedTerraConfigPack/assets/10100603/d126e85c-8670-47cb-a774-27d4aba5bf81)
Jungle version of the mountain mirrors. Features huge mountains with terraces along it. Usually covered with large jungle trees and a few lush lakes at the bottom.

**Badland Balconies**

> ![2023-08-31_18 23 03](https://github.com/Rearth/Origen/assets/10100603/ecb12535-da74-4674-887a-71810e99e12d)
Terracotta-covered mountains, with flat areas inbetween, and some terraces along the mountain ridges. Allows for a thin layer of oak trees in the mountains.

**Lush Loops**

> ![2023-08-23_22 49 45](https://github.com/Rearth/UnnamedTerraConfigPack/assets/10100603/005a6e8c-fd1c-4433-b502-8ae629c765ae)
A lush jungle environment, with massive eye-catching stone arches looping through the skies.

**Sandy Splits**

> ![2024-01-09_00 14 05](https://github.com/Rearth/Origen/assets/10100603/b8b73f8d-9bc4-41dd-83fb-861b710a018f)
Large canyon biome that can carve through any land biome. Very deep, with terracotta walls and sand with vegetation at the bottom.

**Mesa Monuments**

> ![2023-07-26_23 29 34](https://github.com/Rearth/UnnamedTerraConfigPack/assets/10100603/cfb8098b-4cab-4e1d-b442-b0d2372fa024)
Covered by giant terracotta pillars, the mesa monuments biome is a warm badlands / desert mix. The main feature are the big terracotta pillars in it, which can reach up to 100 blocks into the sky.

**Rocky refuge**

> ![2023-09-21_23 41 42](https://github.com/Rearth/Origen/assets/10100603/b31639fa-60fe-4c40-b0c4-a66617d2a9ed)
Forested badlands biome, with large, overhanging terracotta boulders. The boulders are covered in leaf vines, and there are sparse tree patches on the floor.

**White Wallows**

> ![2023-10-25_23 12 48](https://github.com/Rearth/Origen/assets/10100603/1ef4fe83-dad1-4f00-8bed-1e83039bebb1)
Identified by white trenches dug through eroded mountains, the white wallows are home to giant azalea trees. The mountains also house white flowers and deep valleys.

** Icy Incisions**

> ![2024-01-09_21 58 52](https://github.com/Rearth/Origen/assets/10100603/cb6730fb-dcc4-4756-936d-975bfe8ff73a)
A deep, frozen trench carving through any other cold biome. Covered in webs of snow, with a few snow-covered trees at the bottom

**Murky Marshlands**

> ![2023-08-27_14 58 22](https://github.com/Rearth/UnnamedTerraConfigPack/assets/10100603/c3b66b84-9597-46b0-99f9-fa0d2b7db7d0)
Imagine a unique and exotic rendition of the familiar vanilla swamp. This variant is blanketed by imposing, shadowy trees that exude a mysterious aura. The ground seamlessly blends the realms of water and land, creating a captivating environment. On the land, the terrain showcases a series of interconnected, level expanses that intertwine, each marked by sharp transitions in elevation.

**Pillow Plains**

> ![2023-08-27_15 04 35](https://github.com/Rearth/UnnamedTerraConfigPack/assets/10100603/c3ead62b-bbfa-495e-b9d4-0fe8805ecf64)
Split into a high border segment and a low inner segment, the pillow plains is marked by its small pillars through a green valley. Due to the low height of the inner segment, there are no rivers in this biome, though this will be changed in the future by adding a special low river variant.

**Scarlet Sanctuary**

> ![2023-09-20_21 05 43](https://github.com/Rearth/Origen/assets/10100603/37302429-6dfb-47ac-bf1b-e600cbd5b3b3)
Sloped biome, with giant cliffs on the sides. Covered in abundant vegetation, some if it with red leaves. The trees in this terrain can grow much larger than usual, and the floor is filled with grass and more vegetation.

**Watery Wilds**

> ![2023-09-08_14 50 16](https://github.com/Rearth/Origen/assets/10100603/339771fb-c33d-4449-adb7-aab9946d568a)
Savanna-like biome, but partially covered in water, wild small paths leading through the water. Covered in acacia trees and a lot of grass, with small and flat hills.

**Tall Timberland**

> ![2023-08-23_22 31 10](https://github.com/Rearth/UnnamedTerraConfigPack/assets/10100603/685e7708-0a6a-48ff-ac26-cdfbb3e49d0c)
These mountains are covered by giant redwood trees. Similar to the black forests, they also feature flat clearing and lakes in between their forest-covered mountains.

**Tundra Tracks**

> ![2023-09-11_22 30 56](https://github.com/Rearth/Origen/assets/10100603/bda44763-6728-4b6a-803a-17cb04ca5194)
Cold lowlands biome, covered in lakes and small hills. Frozen paths are woven through the lakes. Snow-covered trees are scattered across the landscape.

**Frozen Fungi**

> ![2023-09-20_22 23 46](https://github.com/Rearth/Origen/assets/10100603/7df4325b-7fe6-4748-baa5-49e022f70abc)
Frozen mushroom biome. The terrain itself is slightly tilted, with huge cliffs on one side. There are small and large mushrooms growing, along with some trees. The ground is covered in snow, mycelium and podzol.

**Oasis**

> ![2023-09-11_22 38 52](https://github.com/Rearth/Origen/assets/10100603/55b26ccd-9419-46a2-a126-5688afa997d8)
Micro-biome, usually found in the middle of desert biomes. Identified by a small lake in the sand dunes, with palm trees and grass surrounding it.

**Secluded Valley**

> ![2023-07-28_11 47 03](https://github.com/Rearth/UnnamedTerraConfigPack/assets/10100603/9d9705c2-fbcb-4665-9a89-4e44121b724d)
At a first glance, the secluded valley is just a large and flat sunflower field. However, there are also huge valleys with a small entrance hidden spread throughout this biome. The valleys containt cherry trees and have a small chance to spawn a giant cherry tree in the middle.

**Sakura Streams**

> ![2023-08-28_23 44 56](https://github.com/Rearth/Origen/assets/10100603/609e7642-1bc4-4663-a531-3beb77206229)
Giant mountain, with a lake at the top and multiple rivers flowing down the mountainside. Covered with sakura trees and large leaf vines. Has a small chance to small giant sakura trees.

**Bare Boulderfields**

> ![2023-10-16_17 20 02](https://github.com/Rearth/Origen/assets/10100603/1660f170-b85f-4aac-8d0a-44ef8efaddab)
Barren, rocky mountain, made out of stone plaes. Small trenches are running through the tilted stone plates.

**Verdant Valley**

> ![2023-08-27_15 07 02](https://github.com/Rearth/UnnamedTerraConfigPack/assets/10100603/4433a0f4-e33b-4568-a416-b704ebd32ba0)
The verdant valley is a mostly flat valley with sparse acacia trees. The valley is surrounded by smaller hills which usually have small steep patches with a darker surface.

**Vertical Vistas**

> ![2023-08-23_22 48 15](https://github.com/Rearth/UnnamedTerraConfigPack/assets/10100603/9c2b2375-ad04-4974-bf98-e9599583479c)
Huge, towering green mountains. The often are high enough that their peak is covered in snow. At the bottom of these mountains, there is also often a small lake. Few trees and boulders can be found on the surface.

** WIP **

More biomes will follow soon.

### Cave

**Inferno Isles**

> ![2023-08-27_15 00 32](https://github.com/Rearth/UnnamedTerraConfigPack/assets/10100603/c70a92a2-e8eb-4182-83e4-0ff51526e3ba)
Giant cave biome that usually is found around -20 to +40. Contains a big lava lake with interconnected platforms hanging on chains over it. The cave roof is covered with glowing plants.

**Terracotta Tombs**

> ![2023-09-08_21 29 17](https://github.com/Rearth/Origen/assets/10100603/373ab5da-44a1-45b5-8272-c4138e050bb3)
Underground cavern biome, with a similar shape to the inferno isles. However, this biome is made from terracotta walls, with huge pillars of terracotta in the center.

**Vine Vault**

> ![2023-10-20_15 19 00](https://github.com/Rearth/Origen/assets/10100603/0b88368c-6261-4189-bda2-3002d4a71abf)
Huge cave, with both the floor and the ceiling covered in lush vegetation. There are crossing and glowing vines on the ceiling, wiih moss and jungle trees on the floor. Enormous pillars connect the floor to the ceiling.

** TODO **

### Coast

**Marine Monolits**

> ![2023-08-23_22 45 49](https://github.com/Rearth/UnnamedTerraConfigPack/assets/10100603/29eadfc2-169a-4385-93c2-a2adad62ade7)
Towering cliffs biome, only found at the bigger coasts. The biome has a mostly flat area, which is held by large white pillars that reach deep into the water.

** TODO **

### Ocean

**Stonegate Seas**

> ![2023-09-08_17 59 02](https://github.com/Rearth/Origen/assets/10100603/5e903435-c998-4eea-a078-b0dfc81e4c3c)
Medium-depth ocean, with giant stone arches under and on the surface. The arches are made mossy and partially green, with lush green foliage covering it.

**Abyssal Alleys**

> ![2023-10-24_21 25 44](https://github.com/Rearth/Origen/assets/10100603/4995f68d-3df5-4ef5-ad36-c95c8a92e58e)
Deep ocean variant, with trenches reaching all the way down to bedrock level. There are large, semi-open caves to explore, with fossils at the bottom of the trenches and corals near the top.

**Arctic Arches**

> ![2023-09-08_18 40 55](https://github.com/Rearth/Origen/assets/10100603/31ecbfe8-2785-4ea8-a48c-a830223bf63a)
Frozen version of the Stonegate Seas, with frozen water segments, and large ice arches reaching through the sky. Icicles are found on the ceiling of the arches.

### Special

**Sinkholes**

> ![2023-08-27_14 51 16](https://github.com/Rearth/UnnamedTerraConfigPack/assets/10100603/27346dee-53c4-4ebd-a577-e12d8e915f43)
**Currently disabled**

Sinkholes can be found anywhere in the world, ignoring the usual biome cell spawns. However, they are quite rate. They reach down to Y -40 and have steep cliffs and are usually streched at an angle. There currently are 3 sinkhole variations:

**Jungle Sinkhole**

Contains a warm surface with big jungle trees covering it.

**Forest Sinkhole**

Contains mossy stone walls and a diverse mix of trees covering the bottom of the sinkhole.

**Frozen Sinkhole**

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
