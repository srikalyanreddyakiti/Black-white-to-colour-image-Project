🎨 Image Colorization with OpenCV and Deep Learning
This project uses a pre-trained deep learning model to automatically colorize black and white images using OpenCV's dnn module and a Caffe-based model.

🔧 Requirements
Python 3.x

OpenCV (with dnn module support)

NumPy

Install dependencies:
pip install opencv-python numpy

📁 Project Structure

model/

colorization_deploy_v2.prototxt – Model architecture

colorization_release_v2.caffemodel – Pre-trained model weights

pts_in_hull.npy – Cluster centers for ab channels

images/

albert_einstein.jpg – Input grayscale image

colorize.py – Main colorization script
▶️ How to Run
Run the script using:
python colorize.py
Make sure the model files and image are in the correct folders as shown above.

🧠 How It Works
Loads the pre-trained Caffe model and ab color cluster points.

Converts the input image to LAB color space and extracts the L (lightness) channel.

Feeds the L channel into the model to predict the ab (color) channels.

Combines L with ab to reconstruct the LAB image.

Converts LAB back to BGR and displays both original and colorized images.

📷 Output
Displays the original and colorized image side-by-side using OpenCV windows.

📌 Notes
The input should be grayscale or low-color.

The model is trained on natural images; performance may vary with synthetic or artistic images.

📄 License
This project is for educational purposes. The model is based on the work of Richard Zhang et al. (paper).
