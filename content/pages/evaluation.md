---
title: "Evaluation"
date: 2020-04-18T10:07:21+06:00
# post image
image: "images/blog/post-1.jpg"
# post type (regular/featured)
type: "featured"
# meta description
description: "This is meta description"
# post draft
draft: false
---

ClyDe contains several subsystems(Described in "System" and "How it works" sections). Each of these have been thourogly tested, as we had to ensure they were functioning correctly before trying to inegrate them together. Havign confirmed the reliability and functionality of each subsystem, we could more easily put them together and resolve errors quickly.The three subsystems we have focused the most on are navigation, obstruction detection and QR code detection. 


## Navigation Quantitative Analysis

| Table | Goal Pose            | Mean Achieved Pose    | Success |
| ----- | -------------------- | --------------------- | ------- |
| 1     | 0.35 0.90 0.70 0.70  | 0.46 0.99 0.80 0.61   | 5/5     |
| 2     | -1.20 0.50 0.70 0.70 | -1.33 0.53 0.50 0.87  | 4/5     |
| 3     | 0.3 -4.7 0.0 1.0     | 0.24 -4.5 5 0.10 0.96 | 4/5     |
| 4     | 0.3 -3.7 0.0 1.0     | 0.23 -3.62 0.21 0.95  | 5/5     |
| 5     | 0.3 -2.7 0.0 1.0     | 0.18 -2.81 0.09 0.99  | 5/5     |
| 6     | 1.8 -4.7 0.0 1.0     | 1.77 -4.88 -0.09 1.11 | 3/5     |
| 7     | 1.8 -3.7 0.0 1.0     | 1.64 -3.58 -0.03 1.06 | 4/5     |
| 8     | 1.8 -2.7 0.0 1.0     | 1.73 -2.64 0.05 0.91  | 3/5     |


## Obstruction Detection

| **Attr. to change ↓** | **Brightness/cd** | **Obs. pos** | **Obs. size** | **Obs. color** | **Table color** | **Reflect light** | **Shadow (Gradient)** | **Outcome** |
| --------------------- | ----------------- | ------------ | ------------- | -------------- | --------------- | ----------------- | --------------------- | ----------- |
| **Illumination**      |                   |              |               |                |                 |                   |                       |
|                       | 0-20              | middle       | middle        | light          | brown           | None              | None                  | Success     |
|                       | 20-40             | middle       | middle        | green          | brown           | None              | None                  | Success     |
|                       | 40-60             | middle       | middle        | green          | brown           | None              | None                  | Success     |
|                       | 60-80             | middle       | middle        | green          | brown           | None              | None                  | Success     |
| **Position**          |                   |              |               |                |                 |                   |                       |
|                       | 40-60             | left         | middle        | green          | brown           | None              | None                  | Success     |
|                       | 40-60             | right        | middle        | green          | brown           | None              | None                  | Success     |
|                       | 40-60             | top          | middle        | green          | brown           | None              | None                  | Success     |
|                       | 40-60             | bottom       | middle        | green          | brown           | None              | None                  | Success     |
| **Size**              |                   |              |               |                |                 |                   |                       |
|                       | 40-60             | middle       | small         | green          | brown           | None              | None                  | Success     |
|                       | 40-60             | middle       | large         | green          | brown           | None              | None                  | Success     |
| **Obs. Colour**       |                   |              |               |                |                 |                   |                       |
|                       | 40-60             | middle       | middle        | brown          | brown           | None              | None                  | Success     |
|                       | 40-60             | middle       | middle        | black          | black           | None              | None                  | Fail        |
| **Table color**       |                   |              |               |                |                 |                   |                       |
|                       | 40-60             | middle       | middle        | brown          | dark            | None              | None                  | Success     |
| **Reflected light**   |                   |              |               |                |                 |                   |                       |
|                       | 40-60             | middle       | middle        | green          | brown           | Yes               | None                  | Success     |
| **Shadow**            |                   |              |               |                |                 |                   |                       |
|                       | 40-60             | middle       | middle        | green          | brown           | None              | low                   | Success     |
|                       | 40-60             | middle       | middle        | green          | brown           | None              | high                  | Fail        |

## QR Code detection

| Angle/degree | Distance/meter | Detected | Graph                                  |
| ------------ | -------------- | -------- | -------------------------------------- |
| 10           | 5              | no       | ![image](../media/evaluation/105.png)  |
| 10           | 10             | no       | ![image](../media/evaluation/110.png)  |
| 10           | 15             | no       | ![image](../media/evaluation/115.png)  |
| 30           | 5              | yes      | ![image](../media/evaluation/305.png)  |
| 30           | 10             | no       | ![image](../media/evaluation/310.png)  |
| 30           | 15             | no       | ![image](../media/evaluation/315.png)  |
| 45           | 5              | yes      | ![image](../media/evaluation/455.png)  |
| 45           | 10             | yes      | ![image](../media/evaluation/4510.png) |
| 45           | 15             | no       | ![image](../media/evaluation/4515.png) |
| 60           | 5              | yes      | ![image](../media/evaluation/605.png)  |
| 60           | 10             | yes      | ![image](../media/evaluation/6010.png) |
