# Scan-to-BIM for As-built Roads: Automatic Road Digital Twinning from Semantically Labeled Point Cloud Data

[Paper](https://arxiv.org/abs/2406.12404) | [Citation](#citation) | [Dataset](#data)

All figures and results will be released once the paper is accepted.


## Abstract
Creating geometric digital twins (gDT) for as-built roads still has many limitations, such as low automation level and accuracy, limited asset types and shapes, and reliance on engineering experience. A novel scan-to-building information modeling (scan-to-BIM) framework is proposed for automatic road gDT creation based on semantically labeled point cloud data (PCD), which considers six asset types: **Road Surface**, **Road Side (Slope)**, **Road Lane (Marking)**, **Road/Traffic Sign**, **Road/Street Light**, and **Guardrail**. The framework first segments the semantic PCD into spatially independent instances or parts, then extracts the sectional polygon contours as their representative geometric information, stored in JavaScript Object Notation (JSON) files using a new data structure. Primitive gDTs are finally created from JSON files using corresponding conversion algorithms. The proposed method achieves an average distance error of 1.46 centimeters and a processing speed of 6.29 meters per second on six real-world road segments with a total length of 1,200 meters. 


## Method

![image](https://github.com/user-attachments/assets/df6506d8-ac76-4f18-b026-cd67cc3c1fa5)

<div align="center">Figure 1. Research framework.</div>
<br>
<br>

![image](https://github.com/user-attachments/assets/f42e215e-21c6-42ca-8ae5-1d002ae25abf)

<div align="center">Figure 4. Geometric information extraction algorithm for Plane-like asset instances.</div>
<br>
<br>


![image](https://github.com/user-attachments/assets/cba19de0-d805-4d50-9adc-029c86fc6150)

<div align="center">Figure 5. Geometric information extraction algorithm for Guardrail asset instances.</div>
<br>
<br>

![image](https://github.com/user-attachments/assets/dedf2397-b62a-4f5e-be56-5ad28c655f69)

<div align="center">Figure 6. Geometric information extraction algorithms for Pole-like asset instances’ a) pole, b) panel art, and c) light parts.</div>
<br>
<br>


## Data
This study used six semantically labeled PCD segments of the A11 trunk road in the U.K. for experiments. The data is sourced from the [Digital Roads of the Future](https://drf.eng.cam.ac.uk/research/camhighways-dataset) project of the University of Cambridge. Each PCD is approximately a 200 m road segment. The original data was annotated with 12 semantic labels. However, only six types of road assets were considered in this study: the Road Surface, Road Lane (Marking), Road Side (Slope), Road/Traffic Sign, Road/Street Light, and Guardrail. The length of an instance is approximated as the longest side of its oriented bounding box (OBB), i.e., $length^{inst.}=max⁡(width^{OBB},length^{OBB},height^{OBB})$. The total length of all instances of six road segments is up to 13,593 m.

![image](https://github.com/user-attachments/assets/e61d0b73-2d08-470e-98a6-391fd0195ce4)

Figure 8. The six semantically labeled PCD segments for experiments.

Table 2. Detailed information for each road segment.

![1725345560118](https://github.com/user-attachments/assets/cfdd5a26-445a-4b8c-a268-0c65082f3175)


## Results
Please download files from the "results" folder for details.

![image](https://github.com/user-attachments/assets/7281fc65-bcb7-4bf7-a093-79fb2b95e623)

Figure 9. Geometric information extraction and IFC representation results: a) instance-level results, b) results for Road Surface and Road Side using different grid sizes, and c) road segment-level results.



## Citation
If you find this research useful, consider citing it using:
```
@misc{ding2024scantobimasbuiltroadsautomatic,
      title={Scan-to-BIM for As-built Roads: Automatic Road Digital Twinning from Semantically Labeled Point Cloud Data}, 
      author={Yuexiong Ding and Mengtian Yin and Ran Wei and Ioannis Brilakis and Muyang Liu and Xiaowei Luo},
      year={2024},
      eprint={2406.12404},
      archivePrefix={arXiv},
      primaryClass={cs.CV},
      url={https://arxiv.org/abs/2406.12404}, 
}
```


