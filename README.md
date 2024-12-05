# hf-a-smol-course-

This repo will be a walk through of [a smol course](https://github.com/huggingface/smol-course) by Huggingface.

## Wednesday, December 4, 2024

Created a local mamba environment for this course.

 1) mamba create --name smol python==3.11
 2) mamba activate smol
 3) mamba install conda-forge::jupyterlab
 4) mamba install pytorch torchvision torchaudio pytorch-cuda=11.8 -c pytorch -c nvidia
 5) mamba install conda-forge::transformers
 6) pip install trl # this looked like it would replace a ton of torch/cuda stuff but it did not!
 7) mamba install conda-forge::ipywidgets

Hmm strange. pip shows trl installed but mamba does not. I'm gonna rebuild ... 

mamba remove --name smol --all

 1) mamba create --name smol python==3.11
 2) mamba activate smol
 3) mamba install conda-forge::jupyterlab
 4) mamba install conda-forge::ipywidgets
 5) pip install trl
 6) mamba install conda-forge::transformers

Whelp, that too fails! WTF!? ... time to remove the environment and try something different 

mamba remove --name smol --all

 1) mamba create --name smol python==3.11
 2) mamba activate smol 
 3) mamba install conda-forge::jupyterlab
 4) mamba install conda-forge::ipywidgets
 5) mamba install pytorch==2.4.1 torchvision==0.19.1 torchaudio==2.4.1  pytorch-cuda=11.8 -c pytorch -c nvidia
 6) mamba install conda-forge::transformers
 7) pip install trl

Dammit! Again! mamba cannot see trl! WTF!? ... maybe I just need to install everything through pip into a virtual environment and NOT use mamba/conda ...


