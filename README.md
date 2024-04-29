# downScaleML-MasterThesis
Code and Notebook submission for my Master Thesis at the Insitute for Geoinformatics(ifgi) at the University of Münster

Note: This repository is derived from the GitHub project - 'https://github.com/suriyahgit/downScaleML', which is the development environment of the downScaleML module dedicated to downscale climate data for the interTwin project at Eurac Research. To enhance clarity and facilitate replication, the scripts and programs have been renamed in this repository. The dataset utilized for downscaling will soon be made available as a SpatioTemporal Asset Catalog (STAC) as part of the ongoing efforts of the interTwin project. Nevertheless, this repository contains all the codes and notebooks utilized in the development of my master's thesis titled "Enhancing Seasonal Climate Forecasting to Support Extreme Event Prediction in the Alpine Region Through Statistical Downscaling with Machine Learning."

# downscaleml
First information first!
The dist folder contains the **''downscaleml"** package, install it using `pip install downscaleml-4.0.tar.gz`. Make sure you already have GDAL dependencies installed in your conda/venv/any_environments. If suppose you face problems with the GDAL installation in your system as well as in your environment, don't worry, I am here for you.

This package requires GDAL==3.4.3. 

Follow this link to keep your GDAL installation clean and working:
https://mothergeo-py.readthedocs.io/en/latest/development/how-to/gdal-ubuntu-pkg.html

You could also probably face a problem similar to what i faced, after installation of GDAL, it's the **libstdc++.so.6** linkage problem. This is to do with either **path linking** or **file missing in the directory**. This file has to be found in your system and to be linked with the virtual environment you are working. This can be done by just following **stackoverflow**. I can drop a little clue, which can help you in linking, kindly change the paths relative to your system.
`ln -sf /usr/lib/x86_64-linux-gnu/libstdc++.so.6 /home/anavani/anaconda3/envs/dmcgb/bin/../lib/libstdc++.so.6` 

You could also follow compatibility issue beterrn GDAL and Numpy or GDAL array now, you could arrest this issue by following the process:-

`pip uninstall gdal`
`pip install numpy`
`pip install GDAL==$(gdal-config --version) --global-option=build_ext --global-option="-I/usr/include/gdal"`

# Recommended steps to get going!

1. Clone the git project in your local.
2. `pip install poetry` in your virtual environment
3. `poetry install` in the project local with the same local environment

You are good to go exploring

## Additional Information

The data is not provided in this package, the paths for the input-output data is provided in the `downscaleml/core/config.py`. You can make necessary changes here to reflect elsewhere in the project.
