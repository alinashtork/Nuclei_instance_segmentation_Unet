# Nuclei_segmentation_Unet
This is a project for nuclei segmentation using residual Unet and MIScnn framework committed by @muellerdo where I changed subfunctions so that it works with newest versions of imported libraries.

Here I did a pipeline for nuclei instance segmentation for 2d images using residual Unet. As Unet is able to do only semantic segmentation, I did postprocessing, using OpenCV library. I chose those contours which had a low convexity and found points where convexity defect is maximal, which probably are starting points of a border between nuclei. This approach worked quite well on dataset from Kaggle competition(https://www.kaggle.com/competitions/data-science-bowl-2018), but only on two merged nuclei (look at the examples below). The advantage of this approach is that it is much faster and do not need big computational resourses. 

![Снимок экрана 2023-09-28 224208](https://github.com/alinashtork/Nuclei_instance_segmentation_Unet/assets/117568813/989abaf8-5b3a-464c-8add-fb235d4be108)
![Снимок экрана 2023-09-28 224150](https://github.com/alinashtork/Nuclei_instance_segmentation_Unet/assets/117568813/4ac30a6a-b115-4adc-a41a-b417506c4e11)
![Снимок экрана 2023-09-28 224016](https://github.com/alinashtork/Nuclei_instance_segmentation_Unet/assets/117568813/2aa90c69-2e90-4110-a19d-0307e1d1af68)
![Снимок экрана 2023-09-28 224030](https://github.com/alinashtork/Nuclei_instance_segmentation_Unet/assets/117568813/9fdb961c-dab1-42f1-a8aa-3f183defc2a8)
