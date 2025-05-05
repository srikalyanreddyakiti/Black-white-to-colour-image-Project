Image Colorization with OpenCV and Deep Learning
This project uses a pre-trained deep learning model to automatically colorize black and white images using OpenCV's dnn module and a Caffe-based model.

🔧 Requirements
Python 3.x

OpenCV (with dnn module support)

NumPy

Install dependencies with:

bash
Copy
Edit
pip install opencv-python numpy
📁 Project Structure
bash
Copy
Edit
.
├── model/
│   ├── colorization_deploy_v2.prototxt     # Model architecture
│   ├── colorization_release_v2.caffemodel  # Pre-trained model weights
│   └── pts_in_hull.npy                     # Cluster centers for ab channels
├── images/
│   └── albert_einstein.jpg                 # Input grayscale image
├── colorize.py                             # Main colorization script
▶️ How to Run
Run the script:

bash
Copy
Edit
python colorize.py
Make sure the model files and input image are in the correct directories as shown above.

🧠 How It Works
Loads the pre-trained colorization model and cluster centers.

Preprocesses the input image and converts it to the LAB color space.

Passes the L (lightness) channel through the network to predict the ab (color) channels.

Combines L with predicted ab to reconstruct the color image.

Converts the result back to BGR and displays both original and colorized images.

📷 Output
Displays the original and colorized image side-by-side using OpenCV's GUI window.

📌 Notes
The input image should be grayscale or low-color.

The model is trained on natural images; performance may vary for synthetic or artistic inputs.
