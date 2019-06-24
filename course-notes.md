DETECTION
Viola Jones Algorithm

- Changes image to greysale
- Scans image right to left && top to bottom to try and detect what it is looking for.
- Very basic algorithm in how it works and can be hacked to make it faster through time.

Haar-like Features

- Edge features
  - A feature that detects the end of an area or image.
  - Like the end of a table
- Line Features
  - A feature that has a break in between 2 sections
- Four-rectangle features

Integral Image

- Hacks the way that we find Haar-like feature.
- In a regular we calculate all the pixels in a certain range rectangle.
- This looks at the four corners of a certain pixel range and calculates the sum of the pixels.
- THis does not scale with the size of the image meaning that it stays constant no matter the size of the image.

TRAINING
Training Classifiers

- Training is to identify what you want it to detect and to and help identify certain threshholds
- Algorithm shrinks the image to 24px by 24px
- Supply a multitude of faces or whatever you want to get yur model detecting properly.
  - Supply a lot that have common features
  - Also supply images that are not not faces.
    A General Framework for Object Detection (Book)
    Viola Jones Paper

ADAPTIVE BOOSTING (Adaboost)

- Constucting the stropngest classifier from the stong and weak features
- As the training runs it builds the strong clasifiers and focuses on the false positives and false negatives
- Once you have a success rate above 99.whatever% you will only have to compute a few thousand to get the correct results
  Kinh Tieu & Paul Viola (Paper)

CASCADING

- Take a sub window and look for an important feature. If it is not there then we reject that sub window
- if it finds all the features needed for a face or something else then it will succeed.
