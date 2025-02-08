# Finger Vein Recognition

![Finger Vein Recognition](https://www.kaggle.com/datasets/ryeltsin/finger-vein/data)

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
