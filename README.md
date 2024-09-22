# Facial Expression Detection Based on Machine Learning for Public Service Evaluation

## Overview
This project focuses on developing a machine learning framework to detect facial expressions and evaluate the friendliness of public service officers in real-time. The framework utilizes images from popular datasets like the Karolinska Directed Emotional Faces (KDEF) and Real-world Affective Faces Database (RAF-DB) to train machine learning models using two distinct approaches.

## Models
The first approach implements two pre-trained models based on transfer learning, MobileNet and VGGNet, with additional patch extraction and self-attention mechanisms. The second approach leverages classical machine learning techniques such as Random Forest, XGBoost, Neural Network, and Support Vector Machine (SVM) based on facial landmarks.

### Best Model Performances:

| Model          | Accuracy | Precision | Recall | F1 Score |
|----------------|----------|-----------|--------|----------|
| **MobileNet**  | 0.96      | 0.97       | 0.97    | 0.97      |
| **SVM**        | 0.75      | 0.74       | 0.75    | 0.74      |

## Datasets
1. **KDEF**: Contains 4,900 images of human faces displaying seven different expressions (angry, disgust, fear, happy, neutral, sad, surprise). Each expression is captured from five different angles. We used 700 images per class, splitting them into 80% for training and 20% for testing.
![image](https://github.com/user-attachments/assets/4d5aaeef-42fb-4c5b-887e-09b502f80556)
**Dataset [LINK](https://www.kaggle.com/datasets/tom99763/testtt)**
3. **RAF-DB**: Composed of approximately 30,000 images with seven facial expressions. Due to class imbalance, data augmentation techniques such as horizontal flips and brightness adjustments were applied to increase dataset variability.
![image](https://github.com/user-attachments/assets/92c48dec-f8fd-42ed-8603-e04eeb25a2dc)
**Dataset [LINK](https://www.kaggle.com/datasets/raufmomin/facial-expressions-dataset)**

## Methodology
1. **Data Augmentation**: Applied horizontal flips, rotation, width and height shifts, and brightness adjustments for under-represented classes in RAF-DB.
2. **Model Training**: Transfer learning with MobileNet and VGGNet was employed using the pre-trained ImageNet weights. We also implemented patch extraction and self-attention mechanisms to improve the model's focus on facial landmarks. The SVM model was trained using distance-based features from the facial landmarks extracted using the Dlib library.
3. **Evaluation**: Model performance was evaluated using accuracy, precision, recall, and F1-score metrics. Real-time simulations were performed to test the models on real-world scenarios.
![image](https://github.com/user-attachments/assets/a4387a84-54e8-4ac3-9b2e-7716089d8ba8)

## Simulation
We conducted a simulation using the best-performing model, MobileNet, to assess the friendliness of a public service officer from Universitas Bina Nusantara’s promotion team. The simulation ran for 10 minutes, and facial expressions were recorded and classified in real-time.
![WhatsApp Image 2024-09-18 at 15 58 51_c422222a](https://github.com/user-attachments/assets/cfa4d55a-d36d-4a83-9cc5-612d52247d81)


## Conclusion
This project successfully developed a framework for detecting facial expressions to evaluate public service officers' friendliness. The MobileNet-based model outperformed other models, and further improvements could include integrating other modalities, such as voice or body movement, to increase prediction accuracy.

## Future Work
We suggest creating a larger, more representative dataset that reflects the diverse facial expressions of the Indonesian population for further improvement in the model’s accuracy and real-world applicability.

## Authors
- Marvel Martawidjaja
- Matthew Lefrandt
- Steve Marcello Liem
- Ni Luh Putu Satyaning Pradnya Paramita

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
