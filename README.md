# Preparation
## environment
```shell
pip install -r requirements.txt
```
## dataset
To download the data for train you can go [`link`](https://drive.google.com/drive/folders/1cBvZsesp2JVvdPzaOePEzB8bqs_ehKG7?usp=drive_link).
It is recommaned to put the data file in the dataset folder like
```
data/
    nerf_llff_data/
        amx/
            images/
            images8/
            sparse/
            poses_bounds.npy
            ...
```
If you want to use your own data for modeling, you may need to refer to [`COLMAP`](https://github.com/colmap/colmap) and [`LLFF`](https://github.com/Fyusion/LLFF).

# Train & Evaluation
There are a number of options that can be set, most of which can be used by default, which you can view in [`run_nerf.py`].

## for train
```
python run_nerf.py --config configs/amx.txt # if you want to train the NeRF model.

```
Thanks to [`nerf-PyTorch`](https://github.com/yenchenlin/nerf-pytorch) for the algorithmic implementation of NeRF.

## for evaluation
```
python eval_and_generate.py --ft_path <model_ckp_path> --render # test and generate the video.  '--render_test' will generate the video in test views
```
The weights after model training can be downloaded [`here`](https://drive.google.com/drive/folders/1cBvZsesp2JVvdPzaOePEzB8bqs_ehKG7?usp=drive_link)



