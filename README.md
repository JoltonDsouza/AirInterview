# AirInterview

This document contains the assignment for role of computer vision position

## Requirements

Fork this project and create a pull request once finished the assignment.

## Goal

1. Verify candidate's ability to work with point cloud data
2. Verify candidate's ability to read documentation and implementation skill
3. Verify candidate's ability to write clean and testable code

## Assignment

### Cylinder model segmentation 

By using table_scene_mug_stereo_textured.pcd, find the cylinder inside the scene. 

### Input 

table_scene_mug_stereo_textured.pcd under this github repo

### Output

1. Cylinder inlier point cloud file
2. Visualization screenshot or video

### Bonus

1. Render the final result in web

2. TDD(test driven development) approach

3. Good documentation

4. Good git history which represents essencial thinking process

## Recommendation

1. Tutorial -- http://pointclouds.org/documentation/tutorials/cylinder_segmentation.php#cylinder-segmentation

2. Dev environment setup --- [docker image](https://github.com/Airsquire/PCL-Docker) provided by Airsquire or follow the tutorial [here](http://pointclouds.org/documentation/tutorials/)

3. Testing framework -- [Google Test](https://github.com/google/googletest)

4. Web rendering -- [Three.js](https://threejs.org/docs/index.html#manual/introduction/Creating-a-scene)