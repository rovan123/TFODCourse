
<b>Error:</b> No module named ‘xxxxxx’<br/>
<b>Solution:</b> Install that module
<pre>!pip install xxxxxx</pre>

<i>Example:</i><br/>
Error: No module named typeguard<br/>
Solution: pip install typeguard  # note the name of the module will not always equal the package name

<b>Error:</b> AttributeError: module 'sip' has no attribute 'setapi'<br/>
<b>Solution:</b> Downgrade matplotlib to version 3.2 by running the following command
<pre>!pip install matplotlib==3.2</pre>

<b>Error:</b> ValueError: numpy.ndarray size changed, may indicate binary incompatibility. Expected 88 from C header, got 80 from PyObject<br/>
<b>Solution:</b>  Reinstall pycocotools
<pre>Pip uninstall pycocotools -y
Pip install pycocotools</pre>

<b>Error:</b> ValueError: 'images' must have either 3 or 4 dimensions.<br/>
<b>Solution:</b> Restart your jupyter notebook as the Webcam is unavailable. If using images, this normally means your image name and path is incorrect.

<b>Error:</b>error: (-2:Unspecified error) The function is not implemented. Rebuild the library with Windows, GTK+ 2.x or Cocoa support. If you are on Ubuntu or Debian, install libgtk2.0-dev and pkg-config, then re-run cmake or configure script in function 'cvDestroyAllWindows'<br/>
<b>Solution:</b> Reinstall opencv and uninstall opencv-headless
<pre>
pip uninstall opencv-python-headless -y
pip install opencv-python --upgrade
</pre>

<b>Error:</b>When running GenerateTFRecords script you receive an error like the following:
  File "Tensorflow\scripts\generate_tfrecord.py", line 132, in create_tf_example
    classes.append(class_text_to_int(row['class']))
  File "Tensorflow\scripts\generate_tfrecord.py", line 101, in class_text_to_int
    return label_map_dict[row_label]
KeyError: 'ThumbsDown' # YOUR LABEL HERE
 <br/>
<b>Solution:</b> This is likely because you mismatches between your annotations and your labelmap. Ensure that the label names from your annotations match the label map exactly, note it is case sensitive. 

<b>Error:</b>When running training script from the command line, you get a No module error. e.g. ModuleNotFoundError: No module named 'cv2'
 <br/>
<b>Solution:</b> Remember you need to activate your environment at the command line in order to leverage all the packages you have installed in it. 

<b>Error:</b> When training, only the CPU is used and the GPU is ignored. 
<br/>
<b>Solution:</b> Ensure you have a matching CUDA and cuDNN version for your Tensorflow version installed. Windows:https://www.tensorflow.org/install/source_windows, Linux/macOS: https://www.tensorflow.org/install/source

<b>Error:</b>CUBLAS_STATUS_ALLOC_FAILED or CUDNN_STATUS_ALLOC_FAILED <br/>
<b>Solution:</b> This is because the available VRAM on your machine is completely consumed and there is no more memory available to train. Quit all of your Python programs and stop your Jupyter Notebook server to free up the VRAM and run the command again. 


<b>Error:</b> Cloning into 'large-repository'...
remote: Counting objects: 20248, done.
remote: Compressing objects: 100% (10204/10204), done.
error: RPC failed; curl 18 transfer closed with outstanding read data remaining 
fatal: The remote end hung up unexpectedly
fatal: early EOF
fatal: index-pack failed
<br/>
<b>Solution: Add a "-- depth" after the github link</b> 
<pre>git clone http://github.com/large-repository --depth 1</pre>


<b>Error:</b> 
When installing protobuf using brew. "!brew install protobuf"

Error: protobuf: Calling `cellar` in a bottle block is disabled! Use `brew style --fix` on the formula to update the style or use `sha256` with a `cellar:` argument instead.
Please report this issue to the homebrew/core tap (not Homebrew/brew or Homebrew/core), or even better, submit a PR to fix it:
  /usr/local/Homebrew/Library/Taps/homebrew/homebrew-core/Formula/protobuf.rb:14 <br/>
<b>Solution: Go to https://github.com/protocolbuffers/protobuf/releases/ and scroll to assets and download the protobuf for your os.</b> 

<b>Error:</b> 
When running "protoc object_detection/protos/*.proto --python_out=."

zsh:1: command not found: protoc <br/>
<b>Solution:Find the path of the protoc, for me it is : /Users/{username}/Desktop/ObjectDetection/TFODCourse/Tensorflow/protoc/bin/protoc. And replace the "protoc" with this path</b> 
<pre> /Users/{username}/Desktop/ObjectDetection/TFODCourse/Tensorflow/protoc/bin/protoc object_detection/protos/*.proto --python_out=.</pre> 

Template
<b>Error:</b> <br/>
<b>Solution:</b> 
<pre></pre>

