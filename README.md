
# People Counting System for Smart Building Management

## Description
The **People Counting System** is a computer vision-based project aimed at counting the number of people entering or exiting a building, room, or any other specified area. The system uses a camera to detect and count individuals in real-time. This project was developed as part of the **NVIDIA GRIL Training**, which focuses on leveraging AI and computer vision technologies for real-world applications.

The primary objective of this project is to:
- **Detect people** in a given area.
- **Count the number of people** in the field of view.
- **Track people** as they enter or exit.
- Provide **real-time monitoring and data collection**.

The system can be used for smart building management, ensuring efficient energy consumption, occupancy monitoring, or crowd control. It can be integrated with existing building systems for automated actions based on occupancy, such as controlling lighting, ventilation, or security measures.

### Requirements
- **Hardware**: A camera (webcam or surveillance camera) to capture live video feeds.
- **Software**: Python 3.8+, OpenCV, and other dependencies as listed in the `requirements.txt`.
- **Environment**: The system needs to be executed on a machine capable of running OpenCV and processing video feeds in real-time.

### Files and Annotations
- **Dataset and Images**: The project requires images of people that will be processed for detecting and counting.
- **Annotations**: Annotations are used to mark the regions of interest in the images to help the system identify people in those regions. For human detection, annotations should be placed around each individual, marking the bounding boxes around them.
  
To annotate images:
1. Use tools like **LabelImg** or **CVAT** for annotating the bounding boxes around people.
2. Annotate each person in the image with the correct bounding box.
3. Save the annotations in the **XML format** (Pascal VOC format) or **JSON format**.
4. These annotations will be used to train the model for detecting people in the video streams.

### Technologies Used
- **Python**: The core programming language used to implement the project.
- **OpenCV**: A powerful computer vision library for real-time image and video processing.
- **TensorFlow/Keras**: Used for training deep learning models for object detection.
- **CUDA**: Utilized for GPU acceleration to speed up model training and inference.
- **Flask**: Used for the web interface to display real-time monitoring results.

---

### Steps to Setup the Project

1. **Clone the Repository**:
   Clone the repository to your local machine using the following command:
   ```bash
   git clone https://github.com/your-repository/people-counting-system.git
   ```

2. **Setup DGX Server**:
   The project utilizes NVIDIA DGX systems for GPU-powered training and model deployment.

   - Access the DGX server by navigating to the IP address in your web browser:
     ```
     http://<DGX_IP_address>:<application_port>
     ```
   - Log in with the required username and password.

   - Set up the environment:
     ```bash
     sudo apt update
     sudo apt install python3.8-venv
     python -m venv newenv
     source newenv/bin/activate
     ```

   - Install the required dependencies:
     ```bash
     pip install -r requirements.txt
     ```

3. **Transfer Files to DGX Server**:
   To transfer files from your local machine to the DGX server, use the `scp` command:
   ```bash
   scp -r -P <port_number> <local_folder> user@<DGX_IP>:<remote_folder>
   ```

4. **Run the System**:
   After setting up the environment and transferring the necessary files, run the system:
   ```bash
   python3 app.py
   ```

---

### Conclusion
The People Counting System efficiently tracks the number of people in a given area by using real-time object detection techniques. It is a highly scalable solution for smart building management and occupancy monitoring.

By completing this project, we learned how to apply machine learning and computer vision techniques to real-world problems. The system helps in understanding the challenges and requirements of building intelligent systems for real-time human detection and counting.

## Thanks for going through my project.
Have a great learning!!

Built by: Vidhi Jindal
