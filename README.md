# Road Surface Condition Detection

A computer vision project for analyzing road surface conditions and identifying potential hazards using Python and OpenCV.

## Overview

Road surface conditions can affect vehicle safety, particularly in the presence of wet roads, ice, snow, or potholes. This project explores how traditional computer vision techniques can be used to analyze road images and videos and identify potentially hazardous conditions.

The system processes visual input using image preprocessing, edge detection, morphological operations, contour analysis, and rule-based decision logic.

**Note:** This project is an educational prototype and is not intended for direct use in real vehicle control or safety-critical applications.

## Features

- **Road condition analysis:** Processes road images and videos to identify visual characteristics associated with different surface conditions.
- **Pothole detection:** Analyzes road imagery to identify potential potholes.
- **Image processing:** Applies filtering, contrast enhancement, thresholding, and edge detection.
- **Morphological operations:** Helps refine image regions and detected features.
- **Multiple input modes:** Supports images, videos, and camera input.
- **Debug mode:** Displays intermediate processing results to help understand and evaluate the detection pipeline.
- **Output generation:** Saves processed results to the output directory.

## Technologies

- Python
- OpenCV
- Computer Vision
- Image and Video Processing
- Rule-Based Detection

## Project Structure

```text
road-surface-condition-detection/
├── input/
│   ├── dry_road.jpg
│   ├── icy_road.mp4
│   ├── large_pothole.jpg
│   ├── roads.mp4
│   ├── snow_road.jpg
│   ├── wet_road.jpg
│   └── wet_road_video.mp4
├── output/
│   └── .gitkeep
├── main.py
├── preprocessing.py
├── road_surface_detector.py
├── pothole_detector.py
├── visualization.py
├── utils.py
├── requirements.txt
├── instructions.txt
└── README.md
```

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/ImaneC07/road-surface-condition-detection.git
cd road-surface-condition-detection
```

### 2. Create a virtual environment

**Windows (PowerShell):**

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

**Linux / macOS:**

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

## Usage

Run the following commands from the project root directory.

### Process an image

```bash
python main.py --mode image --input input/dry_road.jpg --output output/dry_result.jpg
```

Other available image samples include:

- `input/wet_road.jpg`
- `input/snow_road.jpg`
- `input/large_pothole.jpg`

For example, to process a wet road image:

```bash
python main.py --mode image --input input/wet_road.jpg --output output/wet_result.jpg
```

### Process a video

```bash
python main.py --mode video --input input/wet_road_video.mp4 --output output/wet_video_result.mp4
```

Other available video samples include `input/icy_road.mp4` and `input/roads.mp4`.

### Use a camera

```bash
python main.py --mode camera
```

### Enable debug mode

Add the `--debug` flag to inspect intermediate image-processing results:

```bash
python main.py --mode image --input input/wet_road.jpg --output output/wet_result.jpg --debug
```

The exact detection results depend on the input, lighting, camera quality, and road visibility.

## Computer Vision Pipeline

The project combines several traditional image-processing techniques:

1. **Preprocessing:** Filters and enhances input images to improve visual analysis.
2. **Edge detection:** Uses the Canny edge detector to identify prominent boundaries.
3. **Morphological operations:** Refines detected regions and image structures.
4. **Contour analysis:** Examines shapes and regions that may correspond to road features or potholes.
5. **Decision logic:** Applies predefined rules to interpret extracted visual information.
6. **Visualization:** Displays or saves the processing results and detection messages.



*Academic project — Computer Vision and Road Surface Analysis.*
