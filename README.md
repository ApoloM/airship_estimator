# airship_estimator

## First steps

1. Clone this project.

2. Install [robot_localization](http://www.dropwizard.io/1.0.2/docs/) 

3. Run command below for running the data set available
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

In file ```launch/play_data_set.launch``` you can comment/uncomment some lines to change between EKF/UKF/LPF filters as you want.
