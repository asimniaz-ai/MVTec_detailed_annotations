# MVTec Dataset Detailed Annotations

This repository contains detailed annotations for the MVTec dataset, which has been traditionally used for unsupervised anomaly detection tasks. These annotations are intended to enhance the existing MVTec dataset by providing **detailed descriptions** of the anomalies in the images, including **types**, **locations (bounding boxes)**, **sizes**, and **descriptions**.

## Contents

- **Annotations**: A JSON file containing detailed descriptions for each image in the MVTec dataset.
- **Code**: Scripts used to generate the annotations.
  
## Purpose

These annotations can be particularly helpful for:

- **Anomaly Localization**: By providing bounding box coordinates, these annotations allow researchers to focus on precisely localizing anomalies within images.
- **Model Training**: The data can be used for training anomaly detection models that not only detect the presence of anomalies but also localize them within the image.
- **Evaluation**: Researchers can use the annotations for more accurate evaluation of anomaly detection models by comparing predicted bounding boxes with ground truth.
- **Dataset Enhancement**: By augmenting the MVTec dataset with these detailed annotations, it becomes more valuable for fine-grained anomaly detection tasks.

## License

The annotations in this repository are made available under the [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License (CC BY-NC-SA 4.0)](https://creativecommons.org/licenses/by-nc-sa/4.0/), consistent with the MVTec dataset license.

## Citation

If you use this dataset in your scientific work, please cite the following papers from the MVTec website:

1. **Paul Bergmann, Kilian Batzner, Michael Fauser, David Sattlegger, Carsten Steger:**
   - *The MVTec Anomaly Detection Dataset: A Comprehensive Real-World Dataset for Unsupervised Anomaly Detection*.
   - **International Journal of Computer Vision 129(4):1038-1059, 2021.**
   - DOI: [10.1007/s11263-020-01400-4](https://doi.org/10.1007/s11263-020-01400-4)

2. **Paul Bergmann, Michael Fauser, David Sattlegger, Carsten Steger:**
   - *MVTec AD — A Comprehensive Real-World Dataset for Unsupervised Anomaly Detection*.
   - **IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR), 9584-9592, 2019.**
   - DOI: [10.1109/CVPR.2019.00982](https://doi.org/10.1109/CVPR.2019.00982)

### Additional Citation for the Annotations

If you use the detailed annotations provided in this repository, please also cite this work:

> **Asim Niaz, Muhammad Umraiz, Kwang Nam Choi** (2024). *MVTec Dataset Detailed Annotations for Anomaly Detection*. Retrieved from [[GitHub Repository URL](https://github.com/asimniaz-ai/MVTec_detailed_annotations)].

## How to Use the Annotations

The annotations in this repository are stored in a JSON format, and each entry contains the following fields:

- **class**: The class of the object (e.g., "pill").
- **anomaly**: The type of anomaly (e.g., "faulty_imprint").
- **image**: The name of the image file (e.g., "016.png").
- **num_anomalies**: The number of anomalies in the image.
- **size_anomalies**: The total size of the anomalies in pixels.
- **coordinates**: A list of bounding boxes for each anomaly. Each bounding box contains the following keys:
  - `min_row`: The minimum row (y-coordinate) of the bounding box.
  - `min_col`: The minimum column (x-coordinate) of the bounding box.
  - `max_row`: The maximum row (y-coordinate) of the bounding box.
  - `max_col`: The maximum column (x-coordinate) of the bounding box.
- **description**: A textual description of the anomaly in the image.

### Example of Annotation Structure

```json
{
    "class": "pill",
    "anomaly": "faulty_imprint",
    "image": "016.png",
    "num_anomalies": 2,
    "size_anomalies": 26388,
    "coordinates": [
        {
            "min_row": 225,
            "min_col": 260,
            "max_row": 414,
            "max_col": 415
        },
        {
            "min_row": 297,
            "min_col": 425,
            "max_row": 462,
            "max_col": 548
        }
    ],
    "description": "Anomaly of type 'faulty_imprint' found in pill images. Image name: 016.png. Number of anomalies: 2, Size of anomalies: 26388 pixels."
}

