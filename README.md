# FootbaAI - UNDER DEVELOPMENT
 
**Football Video Analysis and Data Extraction Project**

## Project Purpose

This project is designed to extract and analyze player data from football match videos. By detecting and tracking players and the ball, the system converts camera coordinates into real-world pitch measurements. This enables detailed analysis of performance metrics such as speed, direction, and distance, providing valuable insights for coaches, analysts, and sports enthusiasts.

![image](https://github.com/user-attachments/assets/0b7b8622-8a57-42ed-980c-1b74488c2d13)


## Features

- **Player and Ball Detection:**  
  YOLO-based models detect players, the ball, goalkeepers, and referees within the video frames.
  
![image](https://github.com/user-attachments/assets/a8c8a14a-a45b-4757-96c1-b5f538a3055d)


![image](https://github.com/user-attachments/assets/82d3eb00-cbe4-4e36-8505-6ad57d3d5bb2)


- **Movement Tracking and Analysis:**  
  Using Kalman filters and ByteTrack algorithms, the system tracks player and ball movements, calculating instantaneous speed, movement direction, and cumulative distance.

![image](https://github.com/user-attachments/assets/13ab8e64-0ea2-422d-8332-6f8439a89bfc)


- **Team Classification:**  
  Visual features are extracted with a pre-trained SiglipVisionModel, reduced in dimension via UMAP, and then clustered using KMeans to classify players by team.

![image](https://github.com/user-attachments/assets/8c5838fb-b1de-40de-8cc8-8f112f524186)

- **Image Transformation and Pitch Calibration:**  
  The project calculates a homography matrix to transform camera coordinates into real-world pitch coordinates, ensuring accurate measurement-based analyses.
  
![image](https://github.com/user-attachments/assets/447bc0cd-f76a-41a3-87d3-73e008a63873)

- **Visualization:**  
  The system visualizes the pitch with overlaid tracking data and a radar view that displays player positions and movement metrics on the field.

![image](https://github.com/user-attachments/assets/cf219d8a-54ca-4b86-b4fe-d414c88c55fe)

- **RL Data Extraction:**  
  Detailed real-world metrics—including position, speed (km/h), direction (degrees), and total distance (m) are extracted for each player, providing a comprehensive dataset for further reinforcement learning or performance analysis.
