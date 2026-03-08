# LW3-Custom-Image-Classifier

# Google Colab Link: <a href="https://colab.research.google.com/drive/1DpKGtxicC9IIrR9GR7sy3HxLThfevpJ4#scrollTo=iokgOW_-RTh8">CLICK HERE</a>!

# Laboratory Work 3 – Guide Questions Answers

# 1. Dataset Preparation

# ○ How did you organize your dataset in Google Drive?

Ans: I organized the dataset in Google Drive using a folder-based structure where each plant category had its own folder. Inside the main folder named ImageDataset, I created separate folders for each plant species. Each folder contained 250+ images belonging to that specific plant class. For example, folders such as Chamomile, Echinacea, and Safflower contained 250+ of images of that specific plant. This structure allowed TensorFlow to automatically assign labels based on the folder names.

# ○ Why is folder structure important for TensorFlow image loading?

Ans: Folder structure is important because TensorFlow’s image_dataset_from_directory() function automatically uses the folder names as labels for classification. This means the model can easily determine which images belong to which category. If the images are not properly organized into folders, TensorFlow cannot correctly identify the classes, which may cause errors or incorrect labeling during training.

# 2. Model Training

# ○ What is the role of convolutional layers in image classification?

Ans: Convolutional layers are responsible for extracting important features from images. These layers apply filters to detect patterns such as edges, textures, shapes, and colors. As the data moves through multiple convolutional layers, the model gradually learns more complex features that help it distinguish between different image categories. This process is essential for accurate image classification.

# ○ Why do we split data into training and validation sets?

Ans: The dataset is split into training and validation sets to evaluate how well the model performs on unseen data. The training set is used to teach the model by adjusting its weights, while the validation set is used to test the model’s performance during training. This helps detect problems like overfitting, where the model memorizes the training data but performs poorly on new data.

# 3. Performance Analysis

# ○ What accuracy did your model achieve?

Ans: After training the convolutional neural network for multiple epochs, the model achieved an approximate validation accuracy of 71.46%. depending on the dataset quality and number of images. This means the model correctly classified most of the validation images.

# ○ How did the number of images affect the model’s performance?

Ans: The number of images significantly affected the model’s performance. Having more images per category allowed the model to learn more variations of each plant species, which improved classification accuracy. When the dataset contains too few images, the model may struggle to generalize and may produce lower accuracy or overfit the training data.

# 4. Critical Thinking

# ○ What challenges did you encounter while using your own dataset?

Ans: One challenge was collecting a large number of high-quality images for each category. Some images also had different lighting conditions, backgrounds, and angles, which made classification more difficult. Another challenge was organizing the dataset correctly and ensuring all images were properly labeled so that TensorFlow could load them without errors.

# ○ How can data augmentation improve your model?

Ans: Data augmentation improves the model by creating variations of existing images through transformations such as flipping, rotation, and zooming. This increases the diversity of the dataset without needing to collect more images. As a result, the model becomes more robust and can generalize better to new images that it has not seen before.

# 5. Application

# ○ Suggest a real-world application for your trained model.

Ans: A real-world application of this trained model is a plant identification system. Farmers, gardeners, or students can take a photo of a plant, and the system will automatically identify the plant species. This can help with agriculture, plant research, and educational purposes.

# ○ How can this system be integrated into a mobile or web application?

Ans: The trained model can be integrated into a mobile or web application using a backend server. The model can be exported and deployed using frameworks such as TensorFlow Lite for mobile apps or TensorFlow Serving for web applications. Users can upload an image through the application, and the system will process the image and return the predicted plant species along with a confidence score.

# Activity 3A: Improving and Evaluating a Custom Image Classifier

# Visualization & Overfitting

# ○ What signs indicated overfitting in your first model?

Ans: Overfitting was observed when the training accuracy continued to increase while the validation accuracy stopped improving or started decreasing. Additionally, the validation loss increased while the training loss decreased. This indicated that the model was memorizing the training data instead of learning general patterns.

# ○ How did data augmentation affect validation accuracy?

Ans: Data augmentation helped improve validation accuracy because it introduced more variation in the training images. By randomly flipping, rotating, and zooming images, the model learned to recognize objects under different conditions. This improved the model’s ability to classify unseen images.

# Model Improvement

# ○ What is the purpose of dropout layers?

Ans: Dropout layers help reduce overfitting by randomly disabling a percentage of neurons during training. This prevents the model from relying too heavily on specific neurons and forces it to learn more generalized features.

# ○ Why does data augmentation improve generalization?

Ans: Data augmentation improves generalization because it exposes the model to different versions of the same image. This helps the model learn patterns that are independent of orientation, scale, or position, making it more capable of handling new images.

# Performance Comparison

# ○ Compare accuracy before and after improvements.

Ans: Before applying improvements such as data augmentation and dropout, the model showed a noticeable gap between training and validation accuracy. After implementing these techniques, the validation accuracy improved and became closer to the training accuracy, indicating better generalization and reduced overfitting.

# ○ Which technique contributed most to improvement?

Ans: Among the applied techniques, data augmentation contributed the most improvement because it effectively increased the diversity of the dataset. This allowed the model to learn from more varied examples, which significantly improved validation accuracy.

# Deployment & Application

# ○ Why is saving the model important?

Ans: Saving the model is important because it allows the trained model to be reused without retraining. This saves time and computational resources and makes it easier to deploy the model in real-world applications.

# ○ How can this model be deployed in a real-world system?

Ans: The model can be deployed by integrating it into a server or application that processes images uploaded by users. For example, a web application could allow users to upload a plant image, and the server would run the trained model to predict the plant species and return the result. The model could also be converted to TensorFlow Lite for use in mobile applications.
