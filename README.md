# dipprojectg2
Computational Photography and Image Enhancement
README.md file:
________________________________________
Computational Photography and Image Enhancement (Group 2)
Digital Image Processing with CNNs and GANs
This project focuses on enhancing HDR images using CNN and GAN-based approaches. The workflow involves preprocessing DNG files, converting them to JPEG format, applying deep learning models, and visualizing the results through an interactive UI.
________________________________________
Project Structure
Digital Image Processing/
├── subset_photos/                        # Folder containing raw .dng files
│   ├── img_0001.dng
│   ├── img_0002.dng
│   ├── ...
├── subset_photos_jpg/                    # Folder containing preprocessed .jpg files (after conversion)
│   ├── img_0001.jpg
│   ├── img_0002.jpg
│   ├── ...
├── subset_photos_augmented/              # Folder with augmented images
│   ├── img_augmented_0001.jpg
│   ├── img_augmented_0002.jpg
│   ├── ...
├── subset_photos_denoised/               # Folder with denoised images
│   ├── img_denoised_0001.jpg
│   ├── img_denoised_0002.jpg
│   ├── ...
├── subset_photos_normalized/             # Folder with normalized images
│   ├── img_normalized_0001.jpg
│   ├── img_normalized_0002.jpg
│   ├── ...
├── subset_photos_preprocessed_updated/   # Final folder with preprocessed images for training
│   ├── img_final_0001.jpg
│   ├── img_final_0002.jpg
│   ├── ...
├── outputs/                              # Folder for storing model-generated images
│   ├── enhanced_img_0001.jpg
│   ├── enhanced_img_0002.jpg
│   ├── ...
├── notebooks/                            # Jupyter notebooks for various tasks
│   ├── Task1_Preprocessing.ipynb         # Preprocessing of raw images
│   ├── Task2_Image_Enhancement.ipynb     # Image enhancement logic
│   ├── Task3_CNN_and_GANs.ipynb          # Implementation of CNN and GANs
│   ├── Task4_Evaluation_PSNR_SSIM.ipynb  # Evaluation using PSNR and SSIM metrics
│   ├── Task5_Save_Model.ipynb            # Saving the models in pickle format
├── models/                               # Saved model checkpoints
│   ├── generator.pth
│   ├── discriminator.pth
├── intermediate_data/                    # Folder containing pickle files for preprocessed/intermediate data
│   ├── preprocess_data.pkl
│   ├── metrics_data.pkl
│   ├── colab_session.pkl
│   ├── colab_session_filtered.pkl
├── saved_models/                         # Additional model files
│   ├── best_model.pth
│   ├── image_enhancement_model.h5
├── README.md                             # Project documentation
└── requirements.txt                      # Python dependencies
________________________________________
Features
1.	Image Preprocessing:
o	Converts DNG files to JPEG for compatibility with OpenCV.
o	Normalizes and resizes images to 256x256 resolution.
o	Organizes preprocessed images into labeled folders.
2.	Deep Learning Models:
o	Baseline CNN model for image enhancement (e.g., U-Net).
o	GAN-based Pix2Pix model for HDR enhancement.
3.	Evaluation:
o	Quantitative metrics: PSNR and SSIM.
o	Visual inspection using matplotlib.
4.	User Interface:
o	Interactive UI for uploading images and displaying enhanced results (Gradio, Streamlit, or Flask).
________________________________________
Setup Instructions
1. Dataset Preparation
1.	Ensure you have the Digital Image Processing folder on your Google Drive.
2.	Create a shortcut to this folder in your "My Drive" following these steps: 
o	Go to the "Shared with me" tab in Google Drive.
o	Right-click on Digital Image Processing and select Organize.
o	Select Create a shortcut and place it in "My Drive".
o	Confirm you can see the folder in your Google Drive root directory.
2. Preprocessing
Run the preprocessing script to convert DNG files to JPEG and organize them into respective folders:
python scripts/preprocess.py
3. Training
Train the CNN baseline:
python scripts/train_cnn.py
Train the GAN:
python scripts/train_gan.py
4. Evaluation
Evaluate the trained model's performance:
python scripts/evaluate.py
5. UI for Image Enhancement
Run the UI for visualizing enhanced results:
python scripts/ui.py
________________________________________
Key Concepts
Why Convert DNG to JPEG?
DNG files are raw and less universally supported, while JPEG files are lightweight and have better compatibility with OpenCV. This simplifies image processing and ensures efficient handling.
Model Pipeline:
•	CNN: Used as a baseline to measure enhancement quality.
•	GAN (Pix2Pix): Advanced model for improving HDR enhancement.
________________________________________
Dependencies
Install the required dependencies using:
pip install -r requirements.txt
Key Packages:
•	torch, torchvision: For deep learning models.
•	Pillow: Image manipulation.
•	OpenCV: Computer vision operations.
•	Gradio/Streamlit/Flask: UI integration.
________________________________________
Results
Enhanced images are saved in the outputs/ folder. Evaluation metrics such as PSNR and SSIM validate the enhancement quality.
________________________________________
Future Work
1.	Integrate more advanced GAN architectures (e.g., CycleGAN, StyleGAN).
2.	Implement automated dataset augmentation techniques.
3.	Deploy the UI to a cloud platform (e.g., AWS, Google Cloud, or Heroku).
________________________________________
Contact
For inquiries or issues, please reach out to Goutham Reddy Kasireddy at:
•	Email: gkasired@CougarNet.uh.edu
________________________________________

