# Image-Classification
The task assigned was to classify the given image into different sports celebrities. there were 5 celebreties virat kohli,federer,serena williams etc.
necessary libraires such as ,numpy, cv2 (OpenCV), os, tensorflow (tf), PIL (Pillow), train_test_split from sklearn.model_selection, classification_report from sklearn.metrics, and tqdm are imported.
Using os.listdir, the code creates an image directory (image_dir) and lists of files for various personalities (e.g., Lionel Messi, Maria Sharapova)
using loops we append images into the dataset lists and labells into the labelled list. then we resize the image size .
The dataset is split into training and testing sets using train_test_split from sklearn. The split is 80% training and 20% testing.
Then the pixel values are normalised
tf.keras.models is used to define the neural network model.Sequential. It is made up of three max-pooling convolutional layers, two dense layers, and an output layer with softmax activation. it is optimised using ADAM and sparse categorical cross entropy is used for classification because multiclass classification.The model is trained using the training data with a validation split of 10% and an early stopping callback to prevent overfitting.
The trained model is evaluated on the test set, and accuracy is printed.
A function (make_prediction) is defined in the code to make predictions on a single picture. It loads the image, preprocesses it, and then predicts the class using the learned model.
final we test the set using a test image and predicted to get the correct classification
