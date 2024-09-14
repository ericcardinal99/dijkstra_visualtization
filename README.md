# Dijkstra’s Algorithm Visualization


https://github.com/user-attachments/assets/e5b6bfb4-9ae7-43a5-852b-72a4f4c9bf50


## Implementation

The first step of the implementation of Dijkstra’s Algorithm was to convert the input.txt and coords.txt files into useful data structures. From the input.txt file, the total number of vertices, starting vertex and goal vertex are saved. Then, the edges are saved in a dictionary. The format of this dictionary is as follows:
	
	{
           tail vertex 1: [
                (head vertex 1, vertex weight), 
                (head vertex 2, vertex weight), 
                ...],
	     tail vertex 2: [
                (head vertex 1, vertex weight), 
                (head vertex 2, vertex weight), 
                ...],
	     ...
      }


From the coord.txt file, the coordinates dictionary is created. The format of this dictionary is as follows:
	
	{
		vertex 1: (x_coordinate 1, y_coordinate 1),
		vertex 2: (x_coordinate 2, y_coordinate 2),
		...
      }


With these dictionaries, along with the starting and goal vertices, Dijktra’s algorithm could now be implemented. Wikipedia’s pseudo code was followed for the algorithm (https://en.wikipedia.org/wiki/Dijkstra%27s_algorithm).

The matplotlib.pyplot library was used to set up the 2-D representation of the edges and coordinates dictionaries. The plot was drawn over for each iteration of Dijkstra’s algorithm in order to create the video. In order to save the video to mp4, the matplotlib.animation.FFMpegWriter library was used. A frame was grabbed at every spot where the plot was drawn.

## How to Compile and Run

Assuming python is already installed, the only installation needed to compile and run this code is matplotlib. Following the installation instructions on matplotlib’s official website (https://matplotlib.org/stable/install/index.html), the only commands needed are as follows:

    python -m pip install -U pip
    python -m pip install -U matplotlib


At the time of submission, the ffmpeg.exe file is up to date and working as expected. If running the file gives an error message related to:

    with writer.saving(fig, "017856202.mp4", 100):
    OR
    writer.grab_frame()

Go to download the latest full ffmpeg build (https://www.gyan.dev/ffmpeg/builds/) and extract the ffmpeg.exe file into the folder where the file python file exists.

When matplotlib and ffmpeg.exe are properly installed, the last step is to run the python file:

    python 017856202.py


This will run Dijkstra’s Algorithm Visualization. If the visualization is taking too long and you don’t want to see it anymore, simply change line 6 from:

    create_video = True
    TO
    Create_video = False



