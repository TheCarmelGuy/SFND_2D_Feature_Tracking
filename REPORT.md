# MP.1
-------


For this, all I did was added a check after pushing the first element into the queue that if the size was greater than some max (3 in this case), simply call erase on the first element. That way, there are never more than 2 elements when in local memory.

# MP.2.
-------

For this, I simply added the detectors from previous exersizes into the code. For the Harris detector, it was simply adding my code for Harris Corner detector as well as my non-maxsupress code. For SIFT, it was a matter of using the SIFT class found in xfeatures2d library. And for the rest, it was a matter of simply using the correspoind detectors "create" function to intitialize the detectors with the correct hyperparameters and run the detectors on. 



# MP.7
-------

YOU CAN FIND MY RESULTS IN keypoints



If you look in the keypoints folder, you'll find the number of key points found in each image. The files are labeled as such:

"Name-of-detector".csv

# SHI-TOMASI

* Seems like there's a lot of points along the sillohette as wall as along color gradient of the car
* Neighbood size for each points is small and the distribution is close 


# FAST

* Very close spread with a significant number of key points
* Key point neighborhood sizes are uniform 

# BRISK

* There seems to be a significant number of points mainly around sillohette of the car
* Neighborhood sizes are large and the spread of sizes seems small

# ORB

* About the same number of points as SHI and TOMASI 
* large detection neighborhood sizes with a large spread

# AKAZE

* Number of key points resembles SHI-TOMASI and ORB. 
* The neighborhood sizes are small but the spread of the sizes are high 


# HARRIS 

* Number of key points is extra small (due to non-maxsupress size)
* Neighborhood sizes are small and uniform (block size) 

# SIFT

* Neighborhood sized seem medium sized with a very large spread. Some are 2 pixels wide where as other are 20 




# MP 8+9
--------
YOU CAN FIND MY RESULTS IN detector-descriptor-pairs. The Files are labeled as such: "DetectorName-DescriptorName.csv"

For this section, the best desriptor should be fast, and should generate very unique and sparser keypoints with a high percentage of matches. The reason I chose this heuristic, was becuase the few keypoints there are, the more salient the feature is. I looked at this qualitatively as well, noting that in each successive frame, feature were match "straight across" (true positive) rather than "diagonally" false negative.

Using this criterion of both speed and matching performance, I came up with the following detector-descriptor pairs: 

* SHITOMASI-BRIEF 
* HARRIS-SIFT
* SHITOMASI-SIFT

All of these pai


Due to the sparcity of keypoints from HARRIS, it was easy and surprising to see how often the same patches were selected as key points and how easily the points were matched from the frame to frame. 




