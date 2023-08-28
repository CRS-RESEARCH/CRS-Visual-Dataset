# CRS Visual Dataset

## Table of Contents
- [Overview](#overview)
- [Dataset Details](#dataset-details)
- [Data Format](#data-format)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Overview

<p>The CRS Visual Dataset (CVD) is the first human-annotated and validated dataset of scanned archival documents from the field of 20th-century architectural programming. </p>
<p>Architectural programming is a professional service provided at the beginning of an architecture, engineering, construction, and operation (AECO) project, but it can be found equally in other domains as well. More generally, programming is defined as a research and decision-making process that identifies the values, priorities, and objectives of a prospective project. The results of this process are recorded and bound in a program document.</p>
<p>The Houston-based architectural firm CRS (Caudill Rowlett Scott, 1948-94) was well-known for its methodical approach to architectural programming. The landmark text on programming, Problem Seeking: An Architectural Programming Primer (1969, 1977, 1987, 2001, 2012) was written by William Merriweather Peña, the fourth founding partner of CRS.</p>
<p>In the 1990s, CRS established a research center at Texas A&M University, the CRS Center, with a twofold mission to promote innovation in the design and construction industry and to preserve the firm’s historical business and design records in an archive, the CRS Archives. Among the significant holdings of the CRS Archives is a collection of nearly 1400 architectural programs by CRS dating from the second half of the 20th century.</p>
<p>This dataset forwards the mission of the CRS center by making a portion of these architectural programs available as a human-annotated and validated dataset, the CRS Visual Dataset (CVD). The CVD, in its current inception, is prepared in the COCO annotation format using the newly established CRS Labeling Convention. The dataset has been prepared for document layout analysis as an object detection task and does not include segmentation mask information.</p>


## Dataset Details

The CRS Visual Dataset, in its current inception, is prepared in the COCO annotation format using the newly established CRS Labeling Convention. The dataset has been prepared for document layout analysis as an object detection task and does not include segmentation mask information. The CRS Visual Dataset includes 7,029 images from 62 architecture programs. The dataset consists of 4,920 images in the training subset, 1406 in the test subset, and 703 in the validation subset.

#### Table: CRS Labeling Convention.

| ID | Class Label | Count |
| --- | --- | --- |
| 1 | Page Title | 1889  |
| 2 | Page Header or Footer | 6701  |
| 3 | Page Number | 4379  |
| 4 | Paragraph Header | 3173  |
| 5 | Paragraph Body | 8595  |
| 6 | List | 1183  |
| 7 | Handwriting | 17419 |
| 8 | Figure Name | 1597  |
| 9 | Figure Caption | 2247  |
| 10 | Table | 2172  |
| 11 | Graph | 209  |
| 12 | Photograph | 408  |
| 13| Drafted Drawing | 1757  |
| 14 | Freehand Drawing | 2414  |
| 15 | Other Figure | 372
| 16 | N/A | 305



## Data Format

The CRS Visual Dataset is in COCO annotation format. The COCO annotation format is a widely used format for annotating and representing object detection, instance segmentation, and keypoint detection tasks in computer vision. It is commonly used in the field of image analysis and deep learning. The COCO annotation format is structured as a JSON (JavaScript Object Notation) file that contains information about the annotated objects within an image dataset. Here is an overview of the main components of the COCO annotation format:

1. **Info**: This section contains general information about the dataset, such as the name, description, version, and year of creation.

2. **Images**: This section includes information about each image in the dataset. Each image is represented by a dictionary with the following attributes:
   - "id": A unique identifier for the image.
   - "width": The width of the image in pixels.
   - "height": The height of the image in pixels.
   - "file_name": The file name or path of the image file.

3. **Annotations**: This section contains the annotations for each object within the images. Each annotation is represented by a dictionary with the following attributes:
   - "id": A unique identifier for the annotation.
   - "image_id": The ID of the image to which the annotation belongs.
   - "category_id": The ID of the object category to which the annotation corresponds.
   - "bbox": The bounding box coordinates of the object in the format [x, y, width, height].
   - "area": The area of the object bounding box.
   - "segmentation": The segmentation mask of the object, represented as a list of polygons or RLE (Run-Length Encoding) format.
   - "keypoints": (optional) The keypoints of the object, if applicable.

4. **Categories**: This section defines the object categories present in the dataset. Each category is represented by a dictionary with the following attributes:
   - "id": A unique identifier for the category.
   - "name": The name of the category.
   - "supercategory": (optional) The supercategory to which the category belongs.


## Usage

**To download the dataset visit [the CVD's Kaggle page](https://www.kaggle.com/datasets/crsresearch/crs-visual-dataset-2).**

**If you use CRS Visual Dataset in your research or publication, we kindly request that you cite the following paper:**

[Oliaee, A. H., & Tripp, A. R. (2023, August). Layout Analysis of Historic Architectural Program Documents. In Proceedings of the ACM Symposium on Document Engineering 2023 (pp. 1-4).](https://dl.acm.org/doi/abs/10.1145/3573128.3609339)


## License

This dataset is licensed under the [Creative Commons Attribution-NoDerivatives 4.0 International License (CC BY-ND)](LICENSE.md).

