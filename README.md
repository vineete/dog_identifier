# Dog Classifier

Given 10,000 training images of 120 different species of dogs (obtained via Kaggle from the Stanford Dogs dataset), the objective of this work was to develop a classifier that could maximize performance on a testing set (also comprised of 10,000 images). 

To achieve this goal, a multi-layer convolutional neural network was implemented and trained using an AWS EC2 instance to minimize compute time. Additional training data was generated by performing rotations and flips on the original data in order to make the model more robust to different camera angles and positions. For each testing image, the model outputs probabilities corresponding to each of the 120 breeds of dogs, with its "prediction" being the breed with the highest assigned probability.

Below are sample testing images that the model correctly classified as a Mexican Hairless Dog and a Staffordshire Bull Terrier, respectively, each with a probability greater than 0.99.

![759edf89ed163128e485238a7c7cd21b](https://user-images.githubusercontent.com/29763261/34633576-d9dc64a0-f231-11e7-9356-ec8da0290879.jpg)
![e783e22d4f370b6cc0b1f44b4d6584a8](https://user-images.githubusercontent.com/29763261/34633578-db17b1e4-f231-11e7-9159-50113baf4f41.jpg)

As seen above, the model definitely displayed promise in terms of being able to recognize very distinct breeds. However, to limit expense, the number of convolutional layers was limited and the model was only trained for 100 epochs. Thus, it is likely that further tuning the network and allowing for more training time would have added a significant improvement to performance.

Future work could involve developing a site enabling users to upload a picture of a dog and immediately determine its breed.
