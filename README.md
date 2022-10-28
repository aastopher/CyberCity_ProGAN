# ProGAN (Progressive Generative Adversarial Network) Trained on Cyberpunk Cityscapes

The purpose of this project is to expand knowledge of traditional GAN architectures by exploring NVIDIA's Progressive GAN research. [Progressive Growing of GANs for Improved Quality, Stability, and Variation](https://research.nvidia.com/publication/2018-04_progressive-growing-gans-improved-quality-stability-and-variation)


## Explore Tensorboard Results
* `tensorboard --logdir logs` - to start the tensorboard and explore the current models training progress.

## Download the Data
* `python utils.py download` - download the cybercity images dataset.
* As a safety pre-caution you must **REMOVE** the imgs folder this command will **NOT** overwrite an existing imgs folder.

## Train the model
* **WARNING! This can overwrite existing models!** 
* `python .\train.py` - continue training or re-train model.
* Changing the `LOAD_MODEL` global in `config.py`; chooses between re-training (`False`) or continuing training (`True`) for the model.

## Generate Samples
* `python utils.py sample` - generates sample images, by default this will generate 10 images at 32x32.
* This command can be customized to generate a chosen amount of images at a chosen size `python utils.py sample <num_images> <size_factor>`
* Size factors: `0 = 4x4, 1 = 8x8, 2 = 16x16, 3 = 32x32, 4 = 64x64, 5 = 128x128, 6 = 256x256, 7 = 512x512, 8 = 1024x1024`
* **WARNING:** Clear results folder before pushing changes.

### References

```
@misc{https://doi.org/10.48550/arxiv.1701.07875,
  doi = {10.48550/ARXIV.1701.07875},
  url = {https://arxiv.org/abs/1701.07875},
  author = {Arjovsky, Martin and Chintala, Soumith and Bottou, Léon},
  keywords = {Machine Learning (stat.ML), Machine Learning (cs.LG), FOS: Computer and information sciences, FOS: Computer and information sciences},
  title = {Wasserstein GAN},
  publisher = {arXiv},
  year = {2017},
  copyright = {arXiv.org perpetual, non-exclusive license}
}
```
```
@misc{https://doi.org/10.48550/arxiv.1704.00028,
  doi = {10.48550/ARXIV.1704.00028},
  url = {https://arxiv.org/abs/1704.00028},
  author = {Gulrajani, Ishaan and Ahmed, Faruk and Arjovsky, Martin and Dumoulin, Vincent and Courville, Aaron},
  keywords = {Machine Learning (cs.LG), Machine Learning (stat.ML), FOS: Computer and information sciences, FOS: Computer and information sciences},
  title = {Improved Training of Wasserstein GANs},
  publisher = {arXiv},
  year = {2017},
  copyright = {arXiv.org perpetual, non-exclusive license}
}
```
```
@misc{https://doi.org/10.48550/arxiv.1710.10196,
  doi = {10.48550/ARXIV.1710.10196},
  url = {https://arxiv.org/abs/1710.10196},
  author = {Karras, Tero and Aila, Timo and Laine, Samuli and Lehtinen, Jaakko},
  keywords = {Neural and Evolutionary Computing (cs.NE), Machine Learning (cs.LG), Machine Learning (stat.ML), FOS: Computer and information sciences, FOS: Computer and information sciences},
  title = {Progressive Growing of GANs for Improved Quality, Stability, and Variation},
  publisher = {arXiv},
  year = {2017},
  copyright = {arXiv.org perpetual, non-exclusive license}
}
```