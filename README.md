# Finger Vein Recognition

![Finger Vein Recognition](https://storage.googleapis.com/kagglesdsdata/datasets/413742/791635/Finger%20Vein%20Database/028/left/middle_1.bmp?X-Goog-Algorithm=GOOG4-RSA-SHA256&X-Goog-Credential=databundle-worker-v2%40kaggle-161607.iam.gserviceaccount.com%2F20250208%2Fauto%2Fstorage%2Fgoog4_request&X-Goog-Date=20250208T175956Z&X-Goog-Expires=345600&X-Goog-SignedHeaders=host&X-Goog-Signature=770fc963eabaf801a4c34abe93d60feb0f4987fc99b7b852e554cb05141dc3943565d1a0631cf347689b0d66e6ca0a3d479139c31833222a67aa615f572c0883d5abdb0ed1dfe323da5bb147421a415eb5313943115574ed2d43b25ab7733f934af29a8171cf5e87c4731e7554ec969e65e10c636952950ce062e365144526076e600195a12d27f616dd4e843eb5c1f57a84455814c32837034b9612772df73ce8a20fd1612becab168ab67e3fe152067d8ac81c70a1c85befbd3997b799223fda0ed77e5a737386626e6a85d252abf0c95f663aab57596c3fa872ee5bdb08e36cb90a3e5ae824488a1ac3ca9c266580cce02e1a7c4f32447d6c5964bed0cc9f)

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
