---
language:
- en
license: creativeml-openrail-m
tags:
- stable-diffusion
- stable-diffusion-diffusers
- text-to-image
- diffusers
inference: true
---
<center><h1><b>Pastel Mix</b></h1></center>
 <p align="center">Welcome to Pastel Mix - a mixed latent diffusion model. This model is intended to produce high-quality, highly detailed anime style with just a few prompts.</p>

   <p align="center">This model is made with the thought of imitating pastel-like art and the potential of mixing LORAs into a model altogether to create a fantastic mix. 
   Recipe for this mix could be found below. Like other anime-style Stable Diffusion models, it also supports danbooru tags to generate images. </p>

<p align="center">e.g. <b>masterpiece, best quality, upper body, 1girl, looking at viewer, red hair, medium hair, purple eyes, demon horns, black coat, indoors, dimly lit</b></p>

<p align="center"><img src="https://huggingface.co/andite/Pastel-Mix/resolve/main/example-images/grid-0020.png">
<img src="https://huggingface.co/andite/Pastel-Mix/resolve/main/example-images/grid-0018.png"></p>

## 🧨 Diffusers

Soon.


## Examples

Under construction.

## Recipe

Merging the models.

| Model: A | Model: B | Weight | Base alpha | Merge Name |
| --- | --- | --- | --- | --- |
| [dpepmkmp](https://huggingface.co/closertodeath/dpepmkmp)  | [Tea](https://huggingface.co/andite/desserts) | 1,0.9,0.7,0.5,0.3,0.1,1,1,1,1,1,1,0,1,1,1,1,1,1,0.1,0.3,0.5,0.7,0.9,1 | 0 | dpeptea |
| dpeptea | [basil-mix](https://huggingface.co/nuigurumi/basil_mix) | 1,1,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0 | 0 | dpeptea-basil |

Merging the loras into the model.

| Model | Lora | Weight | Merge Name |
| --- | --- | --- | --- |
| [dpeptea-basil](https://huggingface.co/closertodeath/dpepteahands3) | [Magic LORA](https://cdn.discordapp.com/attachments/1065289257243115540/1066346221876301845/MagicLORA.pt) | 0.3 | dpeptea-1 |
| dpeptea-1 | [Jordan_3](https://huggingface.co/SatyamSSJ10/ConceptArt) | 1 | dpeptea-2 |
| dpeptea-2 | [sttabi_v1.4-04](https://huggingface.co/dolphinz/stlora) | 0.5 | dpeptea-3 |
| dpeptea-3 | [xlimo768](https://huggingface.co/closertodeath/ctdlora) | 0.6 | dpeptea-4 |
| dpeptea-4 | [dpep 2 768](https://huggingface.co/closertodeath/ctdlora)| 0.35 | Pastel-Mix |

## License

This model is open access and available to all, with a CreativeML OpenRAIL-M license further specifying rights and usage.
The CreativeML OpenRAIL License specifies: 

1. You can't use the model to deliberately produce nor share illegal or harmful outputs or content.
2. The authors claims no rights on the outputs you generate, you are free to use them and are accountable for their use which must not go against the provisions set in the license
3. You may re-distribute the weights and use the model commercially and/or as a service. If you do, please be aware you have to include the same use restrictions as the ones in the license and share a copy of the CreativeML OpenRAIL-M to all your users (please read the license entirely and carefully)
[Please read the full license here](https://huggingface.co/spaces/CompVis/stable-diffusion-license)

## Big Thanks to

The 東方Project AI community for their wonderful LORAs.

- [Closertodeath](https://huggingface.co/closertodeath) for dpepmkmp model, and the loras: xlimo768, dpep 2 768
- [dolphinz/sometimes#9353](https://huggingface.co/dolphinz) for tabi artstyle Lora.
- [SatyamSSJ10](https://huggingface.co/SatyamSSJ10/ConceptArt) for Jordan_3 Lora.
- randomaccessmemories#4004 for Magic Lora