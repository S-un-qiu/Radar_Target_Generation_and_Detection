# SFND-Radar_Target_Generation_and_Detection 

This project uses Matlab simulate a FMCW radar signal, simulate measurements and calculate range and velocity by appropriate signal processing using FFT.

please refer to the attached pdf file for results visualization.

Notes:

CFAR implementation & Selection of Training, Guard cells and offset.
1. define number of Training and Guard cells. The selected number is a trade off between computational complexity and performance. Numbers figured out experimentaly.
2. define threshold value. Value selected experimentaly and noise statistics observation
3. For each possible CUT cell slide a 2D window. Possible CUT cells are those for which the sliding window fits within the boundaries of the RDM matrix.
4. Average the values of the training cells. Appropriately convert values from logarithmic scale to linear and vica versa.
5. Compare the average value to CUT value. Assign to CUT cell 1 if its value exceeds the average value plus a factor, else assign zero.
6. Assigne zero value to the unthresholded cells.

In my implementation the Non-thresholded cells at the edges are initialized with zero, so no need to suppress them later 
