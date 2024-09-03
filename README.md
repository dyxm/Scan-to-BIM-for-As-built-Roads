# Scan-to-BIM for As-built Roads: Automatic Road Digital Twinning from Semantically Labeled Point Cloud Data

All figures and results will be released once the paper is accepted.


## Abstract
Creating geometric digital twins (gDT) for as-built roads still has many limitations, such as low automation level and accuracy, limited asset types and shapes, and reliance on engineering experience. A novel scan-to-building information modeling (scan-to-BIM) framework is proposed for automatic road gDT creation based on semantically labeled point cloud data (PCD), which considers six asset types: **Road Surface**, **Road Side (Slope)**, **Road Lane (Marking)**, **Road/Traffic Sign**, **Road/Street Light**, and **Guardrail**. The framework first segments the semantic PCD into spatially independent instances or parts, then extracts the sectional polygon contours as their representative geometric information, stored in JavaScript Object Notation (JSON) files using a new data structure. Primitive gDTs are finally created from JSON files using corresponding conversion algorithms. The proposed method achieves an average distance error of 1.46 centimeters and a processing speed of 6.29 meters per second on six real-world road segments with a total length of 1,200 meters. 


## Method

![1725344497913](https://github.com/user-attachments/assets/6fa5f9bb-5437-45d1-93aa-f5a01442e8df)

Figure 1. Proposed research framework.


![1725344497913](https://github.com/user-attachments/assets/6fa5f9bb-5437-45d1-93aa-f5a01442e8df)

Figure 4. Geometric information extraction algorithm for Plane-like asset instances.


![1725344497913](https://github.com/user-attachments/assets/6fa5f9bb-5437-45d1-93aa-f5a01442e8df)

Figure 5. Geometric information extraction algorithm for Guardrail asset instances.


![1725344497913](https://github.com/user-attachments/assets/6fa5f9bb-5437-45d1-93aa-f5a01442e8df)

Figure 6. Geometric information extraction algorithms for Pole-like asset instances’ a) pole, b) panel art, and c) light parts.


## Data
This study used six semantically labeled PCD segments of the A11 trunk road in the U.K. for experiments. The data is sourced from the [Digital Roads of the Future](https://drf.eng.cam.ac.uk/research/camhighways-dataset) project of the University of Cambridge. Each PCD is approximately a 200 m road segment. The original data was annotated with 12 semantic labels. However, only six types of road assets were considered in this study: the Road Surface, Road Lane (Marking), Road Side (Slope), Road/Traffic Sign, Road/Street Light, and Guardrail. The length of an instance is approximated as the longest side of its oriented bounding box (OBB), i.e., $length^{inst.}=max⁡(width^{OBB},length^{OBB},height^{OBB})$. The total length of all instances of six road segments is up to 13,593 m.

![image](https://github.com/user-attachments/assets/e61d0b73-2d08-470e-98a6-391fd0195ce4)

Figure 8. The six semantically labeled PCD segments for experiments.

Table 2. Detailed information for each road segment.
![1725345560118](https://github.com/user-attachments/assets/cfdd5a26-445a-4b8c-a268-0c65082f3175)
