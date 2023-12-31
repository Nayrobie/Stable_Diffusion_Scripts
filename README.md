# Stable Diffusion Image Generation Scripts

This repository contains a few scripts for image generation using the Stable Diffusion (SD) model and the automatic1111 webui API.
 
## SD_image_generation_A1111.py

<img src="https://res.craft.do/user/full/7a93547b-a2a3-6209-a5e3-1a49258c4f73/doc/4EDB58DA-8EE5-4FDC-801D-829937E8FF43/8420CE19-8F5F-4F2C-8169-7F43AD74A11F_2/HbHdD1nzlPcnJyMtOX4Pue7wIfL4x80X00NDVPUvkBsz/GAI%20-%20Frame%202.jpeg" width="600">

This script facilitates image generation using different methods:

- **Txt2img:** Generates images based on textual prompts.
- **Img2img:** Runs Stable Diffusion with a prompt and an initial image, allowing users to add an image as input.
- **ControlNet:** Utilises ControlNets for text-to-image generation with additional control conditions.

#### How to Run:

Execute the script and follow the interactive prompts to choose the method, input image, prompts, and other parameters.

## SD_prompt_matrix_A1111.py

<img src="https://res.craft.do/user/full/7a93547b-a2a3-6209-a5e3-1a49258c4f73/doc/4EDB58DA-8EE5-4FDC-801D-829937E8FF43/314F4E36-4BF7-4955-BA37-FB625A988364_2/2mTwhNFZFF0WeFgLJigihPtRUTL3MuOgya2hRNEqRcsz/GAI%20-%20Frame%201.jpeg" width="600">

This script generates a matrix of images, experimenting with blending keywords for diverse image outputs. It is useful for exploring the impact of different prompts on image generation.

#### How to Run:

Execute the script and follow the prompts to choose keywords for the X and Y axes of the matrix.

## SD_saving_steps_A1111.py

<img src="https://github.com/Nayrobie/Stable_Diffusion_Scripts/assets/80701265/df4f3459-1d49-48fc-9d8f-1dcc3ae6dad1" width="600">

This script saves every step of the denoising process during image generation. It can be helpful for analyzing and understanding the evolution of images through the denoising steps.

#### How to Run:

This script doesn’t need to be run, place it at this location `"\stable-diffusion-webui\scripts\saving_steps.py"` then choose this script in Automatic1111 webui and copy the path to your output folder. Simply generate an image, and the script will automatically produce images corresponding to the number of sampling steps.

<img src="https://res.craft.do/user/full/7a93547b-a2a3-6209-a5e3-1a49258c4f73/doc/4EDB58DA-8EE5-4FDC-801D-829937E8FF43/64B53CE5-A09F-499E-B6F6-05CC6752CE36_2/95yvSlZ3wu3EF3pw4VAFzPyzsEuemByoNvrb7dSm0sYz/Image.png" width="600">

## styles.csv

<img src="https://github.com/Nayrobie/Stable_Diffusion_Scripts/assets/80701265/271749ca-dc50-4088-bde0-7f97523f5238" width="600">

This file can help when prompting, it has different template that can be used in addition to the user's prompt. I suggest to always select the default negative prompt when generating images for better results.
In addition to the basic styles, there is also a template for generating Fortnite skins (using both the positive and the negative Fortnite styles)

<img src="https://github.com/Nayrobie/Stable_Diffusion_Scripts/assets/80701265/87892f83-a495-47e0-a040-8e071148a07c" width="600">

#### How to Run:

In Automatic1111 web-ui, select the styles below the generate button

<img src="https://github.com/Nayrobie/Stable_Diffusion_Scripts/assets/80701265/cb49d17b-8969-4333-9860-f0b6912f6f3bc" width="200">

## 🏗️ Prerequisites

- Install [automatic1111 webui](https://github.com/dvschultz/automatic1111) by following the instructions under the Read.me section
- Install the [ControlNet extension](https://github.com/Mikubill/sd-webui-controlnet) following their instructions and download at these four [ControlNet models](https://huggingface.co/lllyasviel/ControlNet-v1-1/tree/main) from the Hugging Face website:
	- `control_v11f1p_sd15_depth.pth`
	- `control_v11p_sd15_canny.pth`
	- `control_v11p_sd15_lineart.pth`
	- `control_v11p_sd15_scribble.pth`
- Download the `style.csv` document from this repository and place it at this location `"\stable-diffusion-webui\styles.csv"`
- Download the SD checkpoint models from [civitai.com](https://civitai.com/), the ones used in the scripts are 
	- `juggernautXL_version45.safetensors [ca4802bc3f]` 
	- `rundiffusionXL_beta.safetensors [f3efadbbaf]`
- The *prompt matrix* and *image generation* scripts can be run in [Visual Studio Code](https://code.visualstudio.com/)

## Contributors

- Yonah Bole
