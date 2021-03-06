This repository contains an implementation of [*StarDist 3D *](https://arxiv.org/abs/1908.03636) used for segmenting the results presented [*here*](https://www.biorxiv.org/content/biorxiv/early/2021/07/27/2021.07.27.453460.full.pdf).
Additionally, this repository contains a custom script for computing multiple metrics such as volume, position, etc. of the segmented results.


## Installation

Follow the steps below to setup all packages on which the notebooks depend. <br>
(i) Move to the command prompt and enter `git clone https://github.com/mangalp/Zebrafish_Segmentation_Setup/`. <br>
(ii) Move to the folder where the repository was cloned by `cd Zebrafish_Segmentation_Setup`. <br>
(iii)Install tensorflow by `conda install tensorflow-gpu=1.14` <br>
(iv) Install StarDist by `pip install "stardist[tf1]"` <br>
(v) Install jupyter with the command `pip install jupyter`. <br>
(vii) Finally, execute the command `pip install ipykernel` followed by the command `python -m ipykernel install --user --name segmentation_stardist --display-name 'segmentation_stardist'`. <br>

You are all set to run the notebooks now. Note that when running any notebook, you should select from within the notebook, `Kernel` and set it to `segmentation_stardist`.

## Usage

Go to the folder `examples/3D/`. This contains three notebooks: `0_ddata.ipynb` (for visualizing the training data and automatic determination of Z-stack anisotropy factor to be usedd later), `1_training.ipynb` (for training a new StarDist 3D model if you have raw images and corresponding GT segmentation images for training), `2_prediction.ipynb` (for predicting on unseen test images after training is performed or if you already have a trained model), `Fish_statistics.ipynb`(this computes the metrics such as volumes given segmented images and writes the resultrs out as .xls spreadsheets).
