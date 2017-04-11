This dataset was recorded at seventh floor in a dorm. The scene is the hallway in the front of another dorm. 
The pedestrians are tracked with KCF method proposed by Joao F. Henriques. The matlab code is downloaded from http://www.robots.ox.ac.uk/~joao/circulant/ 
This dataset has 361 agent and 14375 frames. The fps of video is 25.


dorm_2_track.avi is the video with tracking rectangle and agent number after compression.


dorm_2.txt keeps the positions of agents every 10 frames(every 0.4 second). The mean of every column is as followed:
frame	agent	X	Y	U	V
X,Y are the positions in world. U,V are the pixels.


dorm_2_calibration.txt records the coordinate of calibration points. The mean of every column is as followed:
U	V	X	Y
And the dorm_2.jpg show the background and these calibration points in figure.


dorm_2_matrix means the transform matrix from world to pixel.
The transform and revise process is as followed:

[M,N,1]' = dorm_2_matrix^-1 * [U,V,1]';
Dist = exp(N/60);
X = M*Dist;
Y = N*Dist;

M,N are the coordinate before revision.
Dist is coefficient for revision.

Any question please email to me 15244608332@163.com