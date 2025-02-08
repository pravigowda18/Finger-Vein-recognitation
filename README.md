# Finger Vein Recognition

![Finger Vein Recognition](https://storage.googleapis.com/kagglesdsdata/datasets/413742/791635/Finger%20Vein%20Database/001/left/index_1.bmp?X-Goog-Algorithm=GOOG4-RSA-SHA256&X-Goog-Credential=databundle-worker-v2%40kaggle-161607.iam.gserviceaccount.com%2F20250208%2Fauto%2Fstorage%2Fgoog4_request&X-Goog-Date=20250208T175735Z&X-Goog-Expires=345600&X-Goog-SignedHeaders=host&X-Goog-Signature=2c6e184ea9cfa8f1dc0e9ef4e6912624971f8dc4e6ba061e2ead9365516d1fa475dba9c5f7c8c86ff2de41112da50adc101e37ebaf724496314f014b7418b229e870b452f4bea6438405ed922c8f56cd1aa5895767844c3f87c0fc6810ff1131727fe3e370cd60b5ebd826d092be7591846ea131dede458354616cd112f43cbb23ceddee1c155b92dfe7537cf87c3a8ff268bbb936868e57990ad05767b2609c3b90581c494c051cf8dffed0a94c0cb90207944901658776aa4b250162d24573cfad670318e0d82af8ea6eea8136502886606924926f0f8397e1ead442bbf1f73223b50bff3492201b12102336126e2d8e62d2b532399ea42ba852e15a2b0a75)

A deep learning-based finger vein recognition system that processes finger vein images to extract unique features and identify individuals.

## Features
- Preprocessing of finger vein images
- Feature extraction using HOG, LBP, and Gabor filters
- Model building using CNN
- Supports dynamic adjustment of `num_classes`, `epochs`, and neuron count based on dataset size

## Dataset Structure
Your dataset is structured as follows:
```
Finger Vein/
├── subfolder1/
│   ├── left/
│   │   ├── index/
│   │   │   ├── image1.bmp
│   │   │   ├── image2.bmp
│   │   ├── middle/
│   │   │   ├── image1.bmp
│   │   │   ├── image2.bmp
│   │   ├── ring/
│   │   │   ├── image1.bmp
│   │   │   ├── image2.bmp
│   ├── right/
│   │   ├── index/
│   │   │   ├── image1.bmp
│   │   │   ├── image2.bmp
│   │   ├── middle/
│   │   │   ├── image1.bmp
│   │   │   ├── image2.bmp
│   │   ├── ring/
│   │   │   ├── image1.bmp
│   │   │   ├── image2.bmp
│   ...
├── subfolder2/
...
```

## Files in Repository
1. **finger_folder_crctn.py**
   - Modifies the dataset structure by adding `index`, `middle`, and `ring` folders under `right` and `left`.
   - Moves respective images into the correct folders.

2. **Finger-vein-recognition.py**
   - Reads the dataset structure.
   - Extracts features using HOG, LBP, and Gabor.
   - Builds a CNN model for classification.
   - Designed for a dataset with 50 persons' finger vein samples.
   - `num_classes`, `epochs`, and neuron counts can be adjusted based on dataset size.

3. **LICENSE**
   - The project is licensed under the Apache License Version 2.0, January 2004.

## Installation
To set up the project, follow these steps:

1. Clone the repository:
   ```sh
   git clone https://github.com/pravigowda18/Finger-Vein-recognitation.git
   cd Finger-Vein-recognitation
   ```
2. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```
3. Run the dataset structure correction script:
   ```sh
   python finger_folder_crctn.py
   ```
4. Train the model:
   ```sh
   python Finger-vein-recognition.py
   ```

## Usage
To use the trained model for recognition:
```sh
python recognize.py --image path/to/image.bmp
```

## Model
- Built using TensorFlow.
- Uses CNN for classification.
- Feature extraction is performed using HOG, LBP, and Gabor filters.
- Designed for 50 persons' finger vein samples.

## License
This project is licensed under the Apache License Version 2.0, January 2004. See [LICENSE](LICENSE) for details.

## Contributing
Contributions are welcome! Feel free to fork the repository and submit a pull request.

## Contact
For any queries, contact [Praveen s](mailto:pravisb0002@gmail.com).

---
*Star this repository if you found it helpful!* ⭐
