Hello, this is Phil.

I worked on these files to help us get started (and so we have something to write about for our report)
- cnn.ipynb
- npzDatasets.zip
  - Dataset1Data.npz
  - Dataset2Data.npz
  - Dataset3Data.npz

- - cnn.ipynb - -

This is a Jupyter notebooks file. This code basically imported the images from the provided dataset (not included in the repository - they take a lot of space. Download it for yourself if you want to see them or try running the file on your own).

Specifically, FOR EACH DATASET, this file...
- Reads the information from the provided files
  - Each Dataset has a different size standard for their entries.
    - Dataset1 has 224 x 224 pixel images with 3 color channels.
    - Dataset2 has 300 x 300 pixel images with 3 color channels.
    - Dataset3 has 512 x 512 pixel images with 3 color channels.
  - Each class has 2000 entries.
    - Classes for Dataset 1: "STR", "MUS", "NORM"
    - Classes for Dataset 2: "gland", "nongland", "tumor"
    - Classes for Dataset 3: "wild", "dog", "cat"
    - These have been saved internally as 0, 1 and 2 respectively
  - This was saved as a series of parallel arrays:
    - c1_X, c2_X, c3_X, c1_y, c2_y, c3_y
- Shuffles the file information
  - concatenates c1_X, c2_X and c3_X into all_X
  - concatenates c1_y, c2_y and c3_y into all_y
  - shuffles all_X and all_y using the same index permutation
- Splits these arrays into train and test sets
  - Train 7:3 Test
  - Saved as trn_X, trn_y, tst_X, tst_y
- Saves all of this data as a .npz file
  - This link should show you how to open one of these files using numpy: https://numpy.org/devdocs/reference/generated/numpy.load.html

The zip folder containing all the .npz files was WAY too big for GitHub, so I had to put it on Google Drive. Share link:
https://drive.google.com/file/d/1QfNy6RR7p4pRKEmL3eOPC5sNNaz4uUgn/view?usp=sharing

If you have any questions at all, do not hesitate to ask me!