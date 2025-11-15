# Identify-Groundwater-Infiltration-Types-in-caverns-using-LiDAR-and-MATLAB
Use MATLAB script to identify three flow infiltration pathways of groundwater using the stalactite morphology (aspect ratio and cross sectional area). Method developed by Dr. Kashif Mahmud (Mahmud et al. 2015) and tested by Kathryn Brown and Matthew Kaspar using LiDAR data from the Natural Bridge Caverns.

First, the method takes LiDAR bin/text files, interpolates them into .SGEMS files that can be input into the script to identify flow infiltration pathways. 

The script creates an average surface using a moving average window grid that represents a smoothed ceiling surface. The average window size must be optimized depending on cave site and ceiling clip sizes for best results. The smoothed ceiling surface is then subtracted from the actual ceiling surface to create a map of ceiling anomolies (possible stalactites). A histogram of the anomolies is plotted and used to identify the threshold of individual stalactites (stalactite percentile threshold) and grouped flow types (flow percentile threshold). Any anomalies below the stalactite percentile threshold represents natural rock surface variability. A connected component analysis groups stalactites into water flow types using the flow percentile threshold according to the method identified in Mahmud et al. (2015).  The thresholds must be optimized depending on cave site.

The flow types identified in this method are matrix, fracture, and combination flow. Matrix flow is slow, percolating water, often characterized by small singular stalactites such as soda straws. Fracture flow is fast moving water circulating in cracks and fractures, forming large linear stalactites. Combination flow combines fracture and matrix, and often formes circular stalactites and columns.

Find the LiDAR repository for the northern section of the Natural Bridge Caverns (Comal County, Texas) here:
https://1drv.ms/f/c/dbf2914ff65b23aa/Ery6vrorpQhFrnqg3AoFhUMBAo4y5_73WoTQ2324t0yzgg?e=1ixTw4 
