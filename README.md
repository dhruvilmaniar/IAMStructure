# Object Detection Module

**Notes:**
* This exe is produced under development mode, not release mode.
* High End GPU is **required** to run all the modules efficiently.

The ObjectDetection.exe file will perform :
- Human Detection & Coordinates Extraction
- Vehicle Detection & Coordinates Extraction
- Vehicle Color Detection
- Bad Image Classification
- Unpaved Roads Extraction
- Paved Roads Extraction

# Installation

I've added an windows based installer with the exe. Opening the file sent in the mail will start the installer.
**Choose the installation location. Keep the antivirus off.**

Look for the following files in the folder after installation:


| File | Use |
| ------ | ------ |
| ObjectDetection.exe | The application |
| OUTPUT_DATA | Output Folder for processed Images |
| Data | Database for Detected Objects |

In case of Images, input can be anywhere from the computer.

# File Structure

**Output File structure:**

>   Output Data folder for sortie # xxxxx
    .\OUTPUT_DATA\Sortiexxxxx\

>   Result of Object detection for the Vehicles, Humans and all other detection         module:
    .\OUTPUT_DATA\Sortiexxxxx\Processed_Images

>   KML, CSV for detected Lat-long :
    .\OUTPUT_DATA\Sortiexxxxx\Result_Data\Detection_Data_CSV.csv
    .\OUTPUT_DATA\Sortiexxxxx\Result_Data\Detection_Data_KML.kml
    
>   Result of Roads Detection (Segmentation):
    .\OUTPUT_DATA\Sortiexxxxx\Roads\
    
>   Temp folder:
    .\OUTPUT_DATA\Sortiexxxxx\TMP\
    
    
**Input Structure:**

There can be 3 types of Inputs possible:
*   Live Video Feed : Put the rtsp link of the video in the GUI
*   Video Feed      : Put the Video **File** path from the local machine
*   Images Folder : Put the **Folder** path from the local machine 

In case of video input, an Temp folder will be created automatically.

**Database Structure:**

References for Change Detection are stored in the database. (Only useful for the IAM module.)


**Telemetry:**

Currently, the application extracts the telemetry data from image exif.

A seperate telemetry file input is also possible.

After processing, the application saves the data back in image exif, along with detected data in csv and kml files.


# Usage:

*Ignore the command prompt window for the entire process.

1)  Start ObjectDetection.exe. The GUI will pop up, with 3 options of input as descibed.
2.  Choose the option and provide the paths / links for the input. Press start button.
3.  The system may freeze for a moment. After some time, the detection module should start.
4.  After the process is completed - i.e. all the images have been processed, the GUI will show the option to open the output folder.


# Todos

*   Solve GUI not responding during heavy backend processes.
*   Test Updated Telemetry module
*   Add vehicle type classifier (Dataset needed.)
