# FootbaAI - UNDER DEVELOPMENT
 
**Football Video Analysis and Data Extraction Project**

## Project Purpose

This project is designed to extract and analyze player data from football match videos. By detecting and tracking players and the ball, the system converts camera coordinates into real-world pitch measurements. This enables detailed analysis of performance metrics such as speed, direction, and distance, providing valuable insights for coaches, analysts, and sports enthusiasts.

![image](https://github.com/user-attachments/assets/0b7b8622-8a57-42ed-980c-1b74488c2d13)


## Features

- **Image Transformation and Pitch Calibration:**  
  The project calculates a homography matrix to transform camera coordinates into real-world pitch coordinates, ensuring accurate measurement-based analyses.
  
 ![image](https://github.com/user-attachments/assets/0660058c-26b3-401c-bf88-45610be35ffa)

- **Player and Ball Detection:**  
  YOLO-based models detect players, the ball, goalkeepers, and referees within the video frames.
  
 ![image](https://github.com/user-attachments/assets/070eb0cb-5ce1-45fd-8e2c-37e2d1207576)

- **Movement Tracking and Analysis:**  
  Using Kalman filters and ByteTrack algorithms, the system tracks player and ball movements, calculating instantaneous speed, movement direction, and cumulative distance.

  ![image](https://github.com/user-attachments/assets/3f92fd35-0f9b-457e-914c-23d855353c3d)

- **Team Classification:**  
  Visual features are extracted with a pre-trained SiglipVisionModel, reduced in dimension via UMAP, and then clustered using KMeans to classify players by team.

  ![image](https://github.com/user-attachments/assets/bb2b959a-53b2-4ea1-9f56-83d8b9ccfe2d)

- **Visualization:**  
  The system visualizes the pitch with overlaid tracking data and a radar view that displays player positions and movement metrics on the field.

  ![image](https://github.com/user-attachments/assets/cf219d8a-54ca-4b86-b4fe-d414c88c55fe)

- **RL Data Extraction:**  
  Detailed real-world metrics—including position, speed (km/h), direction (degrees), and total distance (m) are extracted for each player, providing a comprehensive dataset for further reinforcement learning or performance analysis.
