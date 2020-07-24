# Pectoral-Muscle-segmentation from Mammograms
<div> 
  Pectoral segmentation is important as the pectoral muscle region and the breast region may have similar intensity or texture appearance. Both the the tumor cells and pectoral muscle region tend to be brighter (more dense) than the breast region in the mammogram.
Thus, including the pectoral muscle region into breast density quantification may lead to inaccurate breast density estimation.
</div>

## Glossary
### Mammograms
A mammogram is an X-ray picture of the breast. Doctors use a mammogram to look for early signs of breast cancer. The one shown above is called a mediolateral mammogram.

### Pectoral muscle
Pectoral muscles (colloquially referred to as "pecs") are the muscles that connect the front of the human chest with the bones of the upper arm and shoulder. 

### Canny edge detection
Canny Edge Detection is a popular edge detection algorithm. Using Canny Edge Detector solely for pectoral muscle segmentation produces quite unsatisfactory results. Thus, we use hough transform line detection.

### Hough Transfrom
The Hough transform is a technique which can be used to isolate features of a particular shape within an image. Because it requires that the desired features be specified in some parametric form, the classical Hough transform is most commonly used for the detection of regular curves such as lines, circles, ellipses, etc.

## Further improvements
- The algorothm seems to produce satisfactory result on the images.
- However, not so much on the 5'th image . This is so because the pectoral region here can not simply be modelled by a single line.
- We can try to apply this algorithm again on such images, and try to chisel away remaining parts of the pectoral muscle in each iteration
- The parameters for the shortlisting lines have been chosen manually. However, they can be easily learned given a bigger dataset.

<details>
  <summary>Resources and references</summary>
  
  1. Github repo by [@anoo6527](https://github.com/anoo6527/PectoralMuscle_Removal)
  2. Science Direct article: https://www.sciencedirect.com/science/article/pii/S1361841518301129
  3. Paper: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6510623/
  4. Paper: https://core.ac.uk/download/pdf/82133766.pdf
</details>
