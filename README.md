# ml_matlab_images
Creating windows and *nix images for MatLab to support ML micro-services.


## General Usage

> docker run -v `app/dir/matlab_app`:C:/applications/matlab/app/`matlab_app` mobyware/matlab_compiler_run-time:`version` `<params>`


## R-peak 
It's best to have the application and the signal file in the same directory or find some way to relate the volumes. Command below assumes the application and signal file are in the same directory.

>docker run -v `path/to/get_r_peaks/dir`:C:/applications/matlab/app matlab_compiler_run-time:9.0.0 get_r_peaks.exe `signal_file_name`