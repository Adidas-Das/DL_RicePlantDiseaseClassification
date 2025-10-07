# DL_RicePlantDiseaseClassification
This repo contains the codes used to train the various models, and also the final trained models for phases 1 and 2. In short, this contains everything that I dealt with, but it does not contain the training code and models from my colleagues' part of the work yet. We plan to unify everything in the coming future.

The dataset(s) are to be uploaded to Kaggle under the name `<placeholder>`. It includes all the different versions of the dataset that has been used in the project. 

`old` contains an older variation of the working datasets at the early stage of the project included for legacy purposes, while `new` contains the latest dataset versions. The various sub folders are:
- `CP_DATASET_OGplusGA` is the original dataset, which has been geometrically augmented. (Imbalanced Classes)
- `CP_DATASET_GAN` is the modified OGplusGA dataset, involving artifical image generation using a GAN. (Balanced Classes)
- `CP_TEST` is raw data used for final testing purposes.

`CP_MODEL` contains (almost) all the trained models since the early stages of the work. These models involved the geometrically augmented dataset, and also other augmentations in the training code, which is present in the folder `ModelTrainingCode`. There are a few erroneous codes in `ModelTrainingCode`, so please cross-check before using them. In each notebook file, P1 stands for Phase 1 and P2 stands for Phase 2 training code.

We later migrated to using *WGAN-GP* to deal with the class imbalance problem, which ultimately resulted in better overall performance. In the later stages of the comparative study we focused on comparing the performance differences upon using various combinations of augmentations. The training code for these stages are present in the `NEW_STAGE_TrainingCode` folder, with the following sub folders:
- `og`: Stage 1, Working without any augmentations. This uses the dataset present in the `old` folder, named `CP_DATASET`
- `aug_noaug`: Stage 2, Working on geometrically augmented dataset but no further augmentations during training.
- `aug_aug`: Stage 3, Working on geometrically augmented dataset, along with further augmentations (gridmask and color jitter). This stage has been excluded from the final work, since gridmask and color jitter actually hindered the performance, ultimately lowering the accuracy.
- `gan`: Stage 4, Working on GAN-modified dataset.
- `test`: Testing code involving raw data.
  - `Results`: Includes the results for each stage.

The trained models from `NEW_STAGE_TrainingCode` are present in `NEW_STAGE_MODELS` folder, in their respective subfolders.

`Results of New Stage` is the folder containing the training results and the test results.

`Papers` actually consists of various papers I'm going through.

`ResultsSlideshow` is a summarized presentation that my cherished colleague Mr. Kshitij Ayush has compiled.
