# Perceptual-Risk-Aware-Adaptive-Responsibility-Sensitive-Safety-for-Autonomous-Driving
Includes synthetic data, perceived risk levels, perception rules and partial coding.

## synthetic data
The scene features: including environment features and vehicle features. 

The environment features: consist of nine indicators: time, cloudiness, precipitation, road water accumulation, wind, fog density, fog distance, wetting intensity, and road type For simplicity of subsequent expression, we have sampled the following illustrations: I is straight road, R is circle road, T is T-intersection, X is cross intersection. 

The vehicle features: include seven indicators: vehicle HSV value, vehicle type, vehicle distance, pitch angle, heading angle, cross-roll angle, and traffic flow. According to the rules of the RSS model, the vehicles at risk are mainly the nearest frontal vehicles and lateral vehicles. 

Based on SCENIC and CARLA simulation generation.

The camerapos: Coordinates of the target vehicle bounding box on the composite image.

## perceived risk levels
Classification based on the IOU of the target vehicle coordinates predicted by the target detector in tensorflow garden versus the true coordinates.
(Classification based on a threshold \theta_1 = 0.25, \theta = 0.5 and the presence or absence of undetected neighboring vehicles)

perceived risk levels: Safety level, Low Risk Level, Medium Risk Level, High Risk level

## perception rules
The scene features，level -> model + rule

Training interpretable perceptual risk assessment models.



