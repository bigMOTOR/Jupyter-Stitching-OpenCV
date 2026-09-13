# Document Image Stitching with OpenCV

A practical walkthrough of stitching overlapping document photos, written from a mobile developer’s perspective.

This notebook accompanies my article: [Document Image Stitching for Mobile Developers](https://bigmotor.medium.com/document-image-stitching-for-mobile-developers-b169868d023a).

## What’s inside

The notebook walks through image resizing, SIFT feature detection, feature matching, homography estimation with RANSAC, and image warping and stitching. Intermediate visualizations help explain each step.

Two sample photos are included. The final cell displays the stitched image and saves it as `result.jpg`.

## Run locally

With Python 3 installed, run:

```sh
git clone https://github.com/bigMOTOR/Jupyter-Stitching-OpenCV.git
cd Jupyter-Stitching-OpenCV
python3 -m venv .venv
source .venv/bin/activate
python -m pip install notebook opencv-python numpy matplotlib
python -m notebook Stitching-OpenCV.ipynb
```

On Windows, activate the environment with `.venv\Scripts\activate` instead.

Run the cells from top to bottom. To try your own photos, change `part1_file_name` and `part2_file_name` in the first image-loading cell.

## Working with other images

The example assumes overlapping photos of a mostly flat document. The document mask uses a fixed brightness threshold, so different backgrounds or lighting may require adjustments.

The notebook is intended for exploring the pipeline. Handling failed matches and other input edge cases needs additional work before using it in an application.
