# PlantSeg introduction

PlantSeg is a tool for 3D and 2D segmentation.
The methods used are very generic and can be used for any instance segmentation workflow,
but they are tuned towards cell segmentation in plant tissue. The tool is fundamentally composed of two main steps.

![Main Figure](https://github.com/kreshuklab/plant-seg/raw/assets/images/main_figure.png)

* ***Cell boundary predictions***: A convolutional neural network (CNN) is utilized to perform voxel-wise boundary classification. This network is adept at filtering out diverse types and intensities of noise, homogenizing signal strength, and correcting imaging defects such as blurred or missing cell boundaries. This step ensures a high-quality boundary prediction which is crucial for accurate segmentation.

* ***Cell Segmentation as graph partitioning***: The boundary predictions from the first step serve as the basis for automated segmentation. PlantSeg implements four distinct algorithms for this task, each with unique features tailored to different segmentation needs. This graph partitioning approach is particularly effective for segmenting densely packed cells.

For a detailed description of the methods employed in PlantSeg, please refer to our [manuscript](https://elifesciences.org/articles/57613)..

If you find PlantSeg useful in your research, please consider citing our work:

```bibtex
@article{wolny2020accurate,
  title={Accurate and versatile 3D segmentation of plant tissues at cellular resolution},
  author={Wolny, Adrian and Cerrone, Lorenzo and Vijayan, Athul and Tofanelli, Rachele and Barro, Amaya Vilches and Louveaux, Marion and Wenzl, Christian and Strauss, S{\"o}ren and Wilson-S{\'a}nchez, David and Lymbouridou, Rena and others},
  journal={Elife},
  volume={9},
  pages={e57613},
  year={2020},
  publisher={eLife Sciences Publications Limited}
}
```
