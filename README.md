# Calculate the Roundness, and Sphericity (With Pattern Recognition)

[Google Colab Link](https://colab.research.google.com/github/J-TKim/apple_segmentation/blob/main/apple_segemetation.ipynb)    

## 1. Load origin image
<img src="https://github.com/J-TKim/apple_segmentation/blob/main/data/apple1.png?raw=true"  width="350">


## 2. Convert to Gray
<img src="https://github.com/J-TKim/apple_segmentation/blob/main/images/image1.png?raw=true" width="350">

## 3. Find Object (with Pattern Recognition)
<img src="https://github.com/J-TKim/apple_segmentation/blob/main/images/image2.png?raw=true" width="350">


<img src="https://github.com/J-TKim/apple_segmentation/blob/main/images/image3.png?raw=true" width="350">

## 4. Measure object's width, height (depth), and Circumscribed circle(sphere)
<img src="https://github.com/J-TKim/apple_segmentation/blob/main/images/image4.png?raw=true" width="350">


<img src="https://github.com/J-TKim/apple_segmentation/blob/main/images/image5.png?raw=true" width="350">

## Calculate the Roundness, and Sphericity

### Roundness

$$ Roundness = \frac{A_p}{A_c} \times 100 = \frac{A_p}{\frac{\pi}{4}L^{2}} \times 100
\\ \text{}
\\ Roundness = \text{원형률} (\%)\\
A_p = \text{생물체를 평면에 자연스럽게 놓았을 때의 투영면적} (m^2)\\
A_c = \text{생물체에 최소로 외접하는 원의 면적} (m^2)\\
L = \text{생물체의 최대치수 (길이)} (m)$$
------

### Sphericity

$$ Sphericity = \frac{\frac{\pi}{6} \cdot L \cdot W}{\frac{\pi}{6}L^3} \times 100 \\ \text{}
\\ = \frac{(L \cdot W \cdot T) ^ {1/3}}{L} \times 100
\\ \text{}
\\ Sphericity = \frac{d_e}{d_c} \times 100
\\
\\ \text{}
\\ Sphericity = \text{구형률} (\%)\\
L, W, T = \text{생물체의 길이, 폭 두께}(m)\\
d_e = \text{생물체의 체적과 같은 구의 직경}(m)\\
d_c = \text{생물체에 외접하는 최소 외접구의 직경 또는 그 생물체의 최대직경(길이)}(m)$$