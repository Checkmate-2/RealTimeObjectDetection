This is [demo] 5-words sign_language realtime_detection
===============
1- First up install Python  3.7.4. Download and install the package for your OS that has the words 2019.07 in it from here https://repo.anaconda.com/archive/. This should give you 3.7.4 to work with. 

2- Then install Visual Studio C++ 2015 from here: https://go.microsoft.com/fwlink/?LinkId=691126. Tensorflow needs this in order to compile 

3- OPTIONAL IF YOU HAVE A GPU - Install Cuda and Cudnn. Install Cuda first, then install Cudnn. 

.. code:: shell
     
     https://developer.nvidia.com/cuda-10.1-download-archive-base     #Cuda: 10.1
     https://developer.nvidia.com/rdp/cudnn-download   #Cudnn: 7.6.5

Once Cudnn is installed you need to copy the Cudnn files into their respective folders inside the Cuda directory. I used this as a guide: https://towardsdatascience.com/installing-tensorflow-with-cuda-cudnn-and-gpu-support-on-windows-10-60693e46e781
 
 
Prerequisite
-----------------
1- Install python packages using the pip command: 

.. code:: shell
    
    pip install tensorflow    #Tensorflow: 2.3.1
    pip install opencv-contrib-python   #OpenCV: 4.4.0

2- Install Protoc 3.13 from here: https://github.com/protocolbuffers/protobuf/releases. For windows, download the repository and then add it to your PATH file. 

3- Install Tensorflow object detection API. To do this, run these commands from a command prompt or terminal:

.. code:: shell

    git clone https://github.com/tensorflow/models
    cd tensorflow/models/research 
    protoc object_detection/protos/*.proto --python_out=.
    copy "object_detection/packages/tf2/setup.py" .
    python -m pip install .
 
4- Install Tensorflow Pre-trained Model: http://download.tensorflow.org/models/object_detection/tf2/20200711/ssd_mobilenet_v2_fpnlite_320x320_coco17_tpu-8.tar.gz then add it to your PATH file.

For LabelImg-Windows
-----------------

Install `Python <https://www.python.org/downloads/windows/>`__,
`PyQt5 <https://www.riverbankcomputing.com/software/pyqt/download5>`__
and install `lxml <http://lxml.de/installation.html>`__.

.. code:: shell

     pip install pyqt5
     pip install lxml
     
Open cmd and go to the `labelImg <#labelimg>`__ directory

.. code:: shell

    pyrcc5 -o libs/resources.py resources.qrc
    python labelImg.py

Windows + Anaconda
~~~~~~~~~~~~~~~~~~~~~~

Download and install `Anaconda <https://www.anaconda.com/download/#download>`__ (Python 3+)

Open the Anaconda Prompt and go to the `labelImg <#labelimg>`__ directory

.. code:: shell

    conda install pyqt=5
    conda install -c anaconda lxml
    pyrcc5 -o libs/resources.py resources.qrc
    python labelImg.py
    python labelImg.py [IMAGE_PATH] [PRE-DEFINED CLASS FILE]
    
