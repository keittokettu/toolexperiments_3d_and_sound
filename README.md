# experiments in tool-research: 3d and sound

i came into this wanting to explore 3d stuff, and sound stuff.. and indeed i did! here was some of what i got up to:

.
.

## 3d bits (1)
i started my explorations with KIRI Engine (https://www.kiriengine.app/), which offers a variety of tools; what interested me most was its photogrammetry-esque "Photo Scan" (https://www.kiriengine.app/features/photo-scan). i think it exists at a nice and crunky middle point in between photogrammetry and ai/intelligent guesswork as to what an object should look like in 3-dimensional space. 

i started straightforwardly with scanning real-life people, objects, and spaces...

<img width="833" alt="Screen Shot 2025-03-25 at 21 23 25" src="https://github.com/user-attachments/assets/2841bf44-caad-4254-a2a7-af87d9aaabbd" />

_my studio in 3d space!_

https://github.com/user-attachments/assets/d170a353-085d-430c-bf44-e4a33b8c10e0

_the above model brought into an existing Unity file i had lying around_

.

i then took interest in how KIRI renders a space depicted in frames from a video, pulled either from my own records or from online sources. some aspects of horizontally steady video (such as parallax effect) and shortcomings of google maps images (cruddy models) reflect in KIRI's outputs.

<img width="1431" alt="Screen Shot 2025-03-25 at 21 42 17" src="https://github.com/user-attachments/assets/74698384-5028-498f-9fc3-4f92c1334c54" />

_https://www.youtube.com/watch?v=TXyueQlKOv8_

<img width="973" alt="Screen Shot 2025-03-26 at 23 46 25" src="https://github.com/user-attachments/assets/b685f83f-ba11-4cbd-af62-4157ac202700" />

_failed google maps -> 3d model attempt. something about the camera not moving naturally.._

https://github.com/user-attachments/assets/50da44dc-e3d3-424f-9e0e-b47a40a004fd

https://github.com/user-attachments/assets/88a3ff56-9d26-497d-8619-a34b8941b471

_parallex effect in view– a model originating from a steady video i had shot outside a train window._

.

i got a sense for the weak points of this method, and just how much effort it required. KIRI's photogrammetry features, while AI-assisted, still required some amount of 35+ photos to be functional, and taking the photos physically or screenshotting and advancing 70 frames got tiring quick. 

this led to my interests shifting towards (single) image-to-model AI workflows and tools. i wanted to exploit the weirdness of dimensional guesswork, given only one view of an object, and see what funk it would produce. and, i wanted to work with my craigslist free stuff collection (see https://github.com/keittokettu/craigslist_freestuff_repo/), to see if i could bring these objects back to physical existence: take the images, 3d-ify them, and then 3d print them so they live anew. and so,

.
.

## 3d bits (2)

i then began exploring tools hosted on HuggingFace and RunComfy/ComfyUI that handle generation of a 3d model from a single image. with the former, i most played around with Image to 3D (https://huggingface.co/spaces/themanfrom/image-to-3d), and found it to be a credible tool:

<img width="513" alt="Screen Shot 2025-03-26 at 23 36 39" src="https://github.com/user-attachments/assets/ecd94562-f97e-419e-b66c-33b6731547b2" />
<img width="511" alt="Screen Shot 2025-03-26 at 23 36 04" src="https://github.com/user-attachments/assets/72ba866b-e469-4eac-8067-23f803d92491" />

_base images from my craiglist free stuff collection, a chair and a free male rat._

<img width="453" alt="Screen Shot 2025-03-26 at 23 35 18" src="https://github.com/user-attachments/assets/9f89d4bc-ff91-4ae7-8623-1559a5f57674" />
<img width="436" alt="Screen Shot 2025-03-26 at 23 34 43" src="https://github.com/user-attachments/assets/3cc9fcf9-fa0a-46c0-bffb-6d8251e750e4" />

_3d-ification results of above, with Image to 3D. note the charmingly bad object isolation when this tool encounters a visually confusing scene._

.

my main roadblocks with this tool were quickly expiring daily HuggingFace credits and a lack of fine tuning controls. both naturally led me to ComfyUI (using the https://www.runcomfy.com/ cloud-hosted build of it), and tools which others have developed for it. after some confusion with downloading custom nodes, i discovered that pre-made workflows in https://www.runcomfy.com/comfyui/1bb0f87f-8d29-4b90-8298-ae18ba9627d8 contain working and easy-to-launch workflows of different 3d diffusion models. i worked with:

- _Hunyuan3D-2_ - https://www.runcomfy.com/comfyui-workflows/hunyuan3d-2-workflow-in-comfyui-create-3d-assets-from-images /

- _Stable Fast 3D_ - https://www.runcomfy.com/comfyui-workflows/create-3d-content-with-stable-fast-3d-model / https://github.com/MrForExample/ComfyUI-3D-Pack/tree/main

i found Stable Fast to be a little crummy, and gave me results i didn't feel worked for me, and so i have gravitated towards preferring Hunyuan's outputs. Stable Fast, for future reference, requires images to be pngs containing some transparency, ideally isolating the intended 'object' to model. Hunyuan has some nodes which handle this masking for you, which i prefer. there is some room for tinkering with insertion of nodes or manipulating parameters of the patch which i have yet to do, but i have these generated examples from a variety of sources:

<img width="430" alt="Screen Shot 2025-04-01 at 17 54 14" src="https://github.com/user-attachments/assets/26a26e7c-c6e1-481b-8d99-2d4363c10cc9" />

_selfie on zoom– exploring how this workflow renders flatness (aka. when an object is not clearly determinable and the scene is read as one flat image object)_

<img width="630" alt="Screen Shot 2025-04-01 at 18 01 52" src="https://github.com/user-attachments/assets/52b16da8-3d26-4f43-80d0-2f5ac54c0f34" />

_craigslist stumps_

<img width="704" alt="Screen Shot 2025-04-01 at 18 07 11" src="https://github.com/user-attachments/assets/75a9b21f-529f-4ee0-927f-7315389b9061" />

_maxmsp split-scan sketch which made my body wonky; reflects well in the resulting model_

https://github.com/user-attachments/assets/5870be71-4388-4cb5-be13-81d51ece71f6

_craigslist cats_

.
.

## sound bits
a parallel interest of mine were sound and music-related tools– i thought of it as a foil to how many visually oriented tools we had encountered in class and how those seemed to dominate the 'AI mainstream' (other than let's say voice cloning/generated speech tools). i mainly focused on tinkering with:

- _Audimee - https://audimee.com/_

- _ElevenLabs - https://elevenlabs.io/_

**Audimee** had some harmonization tools which briefly interested me, and a variety of 'unique voices' you could employ to sing your harmonies. i got a bored of it though, and was put off by its front-page endorsement of Ye's recent use of the tool. sometimes tools are a little too polished, and i think i'm in the search of some sloppy gunk that isn't quite flawless. 

(excuse the weird blank video files– github didn't like my .wav files and this was the easiest way to stick audio into this repo.)

https://github.com/user-attachments/assets/9006f3c6-4eda-449e-9d04-eea4a1049734

_experiments in harmony generation with Audimee, using an existing sound i had made in Ableton with a train whistle sample. it's nicest when it acts the least like a real singing voice._

.

i then moved on to **ElevenLabs** and had a way better time. it has some formidable speech tools, but i focused on its "sound effects" feature. there's a nice toggle that allows you to control the percentage of faithfulness with which it follows your prompt. i think this is a great way to introduce some crunk and texture into generated sounds. here are some nice generation results _(1)_, and then a short beat _(2)_ made from purely these samples. i wish to extend this workflow of sampling my generations into my final project, or at least into further play and exploration. the compressed folder of all the generated samples is also on this repo, if you wish to use these sounds yourself.

https://github.com/user-attachments/assets/faf08c2d-a48b-44e1-a30c-2b8092994533

_(1)_

https://github.com/user-attachments/assets/7522f52f-7ce8-4169-bfac-a767538a5a48

_(2)_

.
.
.

**P.S.** some useful supplementary tools i encountered were:
- _heic to jpg converter_ (https://picflow.com/convert/heic-to-jpg) - used during my KIRI Engine explorations, since i was taking a lot of images on my (i)phone and they were in an obtuse heic file. jpgs can be read better!
- _glb to obj converter_(https://convert3d.org/glb-to-obj) - some 3d model gen tools output as glbs; for use in Unity, Blender, and 3-d printing, this site works well for converting in between 3d formats.
- _compression_ (https://www.freeconvert.com/video-compressor/download) - files can get a little too big sometimes.

