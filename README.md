# airship_estimator

This package was developed for comparative purposes. It contains algorithms for pose and velocity estimation of a robotic airship. The algorithms available are: Extended Kalman Filter (EKF), Unscented Kalman Filter (UKF) and Low-pass Filter (LPF).

## Visual results

LPF
[![YouTube](https://img.youtube.com/vi/VL5dvCyOZwY/maxresdefault.jpg)](https://youtu.be/VL5dvCyOZwY)

EKF
[![YouTube](https://img.youtube.com/vi/jaATwV0rG30/maxresdefault.jpg)](https://youtu.be/jaATwV0rG30)

UKF
[![YouTube](https://img.youtube.com/vi/B26xaKtAyWo/maxresdefault.jpg)](https://youtu.be/B26xaKtAyWo)

## First steps

1. Clone this project.

2. Install [robot_localization](https://wiki.ros.org/robot_localization) 

3. Download the file [data_set.bag](https://www.dropbox.com/s/abjkcnbxy7qy39h/data_set.bag?dl=0) and save inside the folder bag_files

4. Run command below for running the data set available
```
roslaunch airship_estimator play_data_set.launch
```
## How to use

You can configure UKF and EKF parameters by editing the file:
```
config/ukf_params.yaml
```
You can configure LPF parameters by editing the file:
```
launch/lpf.launch
```
You can configure Acceleration correction parameters by editing the file:
```
config/accel_estimator_params.yaml
```

In files ```launch/play_data_set.launch``` and ```launch/play_results.launch``` you can comment/uncomment some lines to change between EKF/UKF/LPF filters as you want.

Before running ```launch/play_results.launch``` you will have to change the name of the bag file inside the launch with the one generated by ```launch/play_data_set.launch```.

## Other Resources
Further details can be found in this paper: https://proceedings.science/sbai-2019/papers/comparative-study-for-robotic-airship-state-estimation-with-lpf--ekf-and-ukf.

## How to cite
If you find this code useful in your research, please consider citing:

    @inproceedings{marton2019SBAI,
        year = {2019},
        month = {oct},
        author = { Marton, A. S. and Nogueira, L. A. C. de O. and Fioravanti, A. and de Paiva, E. C.},
        title = {Comparative study for Robotic Airship State estimation with {LPF}, {EKF} and {UKF}},
        booktitle = {2019 {SBAI} - XIV  Simp{\'{o}}sio Brasileiro de Automa{\c{c}}{\~{a}}o Inteligente}
    }
  
