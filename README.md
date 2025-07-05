# Sea Surface Temperature Reconstruction under Cloud Occlusion

This project addresses the problem of reconstructing missing Sea Surface Temperature (SST) data in satellite images affected by cloud occlusion. SST readings, derived from MODIS infrared satellite data (Aqua satellite), are often incomplete due to atmospheric interference, particularly over the North Adriatic Sea.

## Objective
Reconstruct occluded SST data using deep learning techniques, with a focus on improving over a statistical baseline.

## Dataset
- Source: MODIS Aqua Nightly SST
- Region: North Adriatic Sea
- Time span: 2002–2023
- Preprocessed with land-sea masking, Gaussian normalization, and artificial occlusion generation

## Methodology
- Created a custom data generator to simulate realistic occlusion scenarios for training
- Explored various models including:
  - Simple CNN
  - ResNet
  - GAN-based inpainting networks
  - U-Net (final selected model)
- Implemented a deep U-Net architecture with a custom loss function targeting masked (occluded) regions
- Integrated early stopping and adaptive learning rate scheduling

## Evaluation
- Performance measured using Root Mean Squared Error (RMSE) on masked areas
- Compared against a tuned statistical baseline
- Evaluation followed strict separation of training, validation, and test periods with consistent normalization

## Technologies Used
- Python, TensorFlow, NumPy, Pandas, Matplotlib
- Satellite data handling and preprocessing
- Custom data augmentation and masking logic

## Notes
This project was developed as part of a university deep learning exam and focuses on scientific reproducibility, practical model implementation, and fair evaluation.
