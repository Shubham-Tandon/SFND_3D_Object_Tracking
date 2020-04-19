# Performance Evaluation

## FP.5 Performance Evaluation 1

The TTC calculated using Lidar point clouds is reasonable accurate as seen from the table as well as the graph below. There is, however, an anomaly at image 6 and image 7 when the TTC drops to 0.73s and then shoots to 3.78s. This can be due to the fact that TTC is calculated on minimum Lidar point associated to the car in front at each time step. No filtering of vehicle position was done to crop out spurious minimum distances. Once the position of the preceeding vehicle is tracked using techniques such as Kalman Filtering, we can get a smoother TTC over time graph. 

<img src="images/LiDAR_Summary" width="302" height="461" />

<img src="images/LiDAR_TTC_Graph" width="808" height="500" />

## FP.6 Performance Evaluation 2

Camera TTC was calculated using the median of the sorted list of distance ratios of matched keypoints between successive frames. Different detector/ descriptor combinations were used to calculate the TTC. The table shows the the mean TTC value and standard deviation of the TTC values. Also, the TTC for various images were plotted on the graph (only the four best combinations are shown). Based on these two information, the best four combinations were chosen which tracked the TTC in consistent anner. These combinations are highlighted in yellow. 
There can be several reason for inaccuracies in TTC value (when compared to TTCs calculated using LiDAR data). The calibration of the camera may be inaccurate. 

<img src="images/Det_Desc_Evaluation" width="414" height="800" />

<img src="images/Camera_TTC_Comp" width="808" height="500" />



