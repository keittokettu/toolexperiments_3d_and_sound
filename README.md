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
.

i got a sense for the weak points of this method, and just how much effort it required. KIRI's photogrammetry features, while AI-assisted, still required some amount of 35+ photos to be functional, and taking the photos physically or screenshotting and advancing 70 frames got tiring quick. 

this led to my interests shifting towards (single) image-to-model AI workflows and tools. i wanted to exploit the weirdness of dimensional guesswork, given only one view of an object, and see what funk it would produce. and, i wanted to work with my craigslist free stuff collection (see https://github.com/keittokettu/craigslist_freestuff_repo/), to see if i could bring these objects back to physical existence: take the images, 3d-ify them, and then 3d print them so they live anew. and so,

## 3d bits (2)

hehe

## sound bits
a parallel interest of mine were sound and music-related tools– i thought of it as a foil to how many visually oriented tools we had encountered in class and how those seemed to dominate the 'AI mainstream' (other than let's say voice cloning/generated speech tools). i mainly focused on tinkering with:

- _Audimee - https://audimee.com/_

- _ElevenLabs - https://elevenlabs.io/_

**Audimee** had some harmonization tools which briefly interested me, and a variety of 'unique voices' you could employ to sing your harmonies. i got a bored of it though, and was put off by its front-page endorsement of Ye's recent use of the tool. sometimes tools are a little too polished, and i think i'm in the search of some sloppy gunk that isn't quite flawless. 

(excuse the weird blank video files– github didn't like my .wav files and this was the easiest way to stick audio into this repo.)

https://github.com/user-attachments/assets/613696f2-59d8-451f-ba1a-a514c0f95b9b

_experiments in harmony generation with Audimee, using an existing sound i had made in Ableton with a train whistle sample. it's nicest when it acts least like a real singing voice._

i then moved on to **ElevenLabs** and had a way better time. it has some formidable speech tools, but i focused on its "sound effects" feature. there's a nice toggle that allows you to control the percentage of faithfulness with which it follows your prompt. i think this is a great way to introduce some crunk and texture into generated sounds. here are some nice generation results (1), and then a short beat made from only these samples. i wish to extend this workflow of sampling my generations into my final project, or at least into further play and exploration.

https://github.com/user-attachments/assets/faf08c2d-a48b-44e1-a30c-2b8092994533

_(1)_

https://github.com/user-attachments/assets/806f924d-b423-4f30-9472-aebbf32fcfbb

_(2)_


**P.S.** some useful supplementary tools i encountered were:
- _heic to jpg converter_ (https://picflow.com/convert/heic-to-jpg) - used during my KIRI Engine explorations, since i was taking a lot of images on my (i)phone and they were in an obtuse heic file. jpgs can be read better!
- _glb to obj converter_(https://convert3d.org/glb-to-obj) - some 3d model gen tools output as glbs; for use in Unity, Blender, and 3-d printing, this site works well for converting in between 3d formats.
- _compression_ (https://www.freeconvert.com/video-compressor/download) - files can get a little too big sometimes.

