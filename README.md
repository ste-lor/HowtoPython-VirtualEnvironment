# HowtoPython-VirtualEnvironment
Some open source programs are not always immediately compatible with the latest Python version. Thus, it is suitable to create virtual environments and decouple your main Python and work within the virtual env. This avoids that the different Python versions influence each other.

<br />

**For Linux:**
````
comming soon
````

<br />
<br />
<br />

**For Windows:**<br />
First, the desired Python version has to be installed. To do that, go to [PythonVersionsWindows](https://www.python.org/downloads/windows/) and download the version of your choice.
<br />
<br />
It is convenient to store all local versions in a single folder. One possibility is shown below. There are currently two different Python versions stored in the file "C:\Python".
````
C:\Python\Python3.8.8
C:\Python\Python3.9.10
````
<br />
<br />
Once the desired Python version is installed, continue with the following steps.
Install via pip,

````
pip install virtualenv
````
Next, navigate to the desired folder where the virtual environment should be installed,
````
cd C:\Users\my_project
````
Within the desired folder install your new environment for the specific Python version,
````
virtualenv my_venv --python=python3.8.8 

````
Activate the new environment,
````
cd C:\Users\my_project\my_venv\Scripts\activate
````
Check the installed version,
````
python --version
````
Deactivate the environment by typing, 
````
deactivate
````
