# HowtoPython-VirtualEnvironment
Some open source programs are not always immediately compatible with the latest Python version. Thus, it is suitable to create virtual environments and decouple your main Python and work within the virtual environment. This avoids that the different Python versions influence each other.<br />

The following description is a brief summary of [How to Install Multiple Python Versions]( https://k0nze.dev/posts/install-pyenv-venv-vscode/) from [k0nze](https://k0nze.dev/).

<br />

**For Linux:**<br />
First, 

````
comming soon
````



<br />
<br />
<br />



**For Windows:**<br />
First, the desired Python version has to be installed. To do that, go to [PythonVersionsWindows](https://www.python.org/downloads/windows/) and download the version of your choice. <br />
It is convenient to store all local versions in a single folder. One possibility is shown below. There are currently two different Python versions stored in the file `C:\Python\`:
````
C:\Python\Python3.8.8
C:\Python\Python3.9.10
````

Once the desired Python version is installed, continue with the following steps.<br />
1. Install via `pip`,
````
pip install virtualenv
````

2. Next, navigate with the terminal to the desired folder where the virtual environment should be installed. For instance,
````
cd C:\Users\my_project
````

3. Within the desired folder install your new environment for the specific Python version by typing,
````
virtualenv my_venv --python=python3.8.8 
````

4. Activate the new environment,
````
cd C:\Users\my_project\my_venv\Scripts\activate
````

5. Check installed version,
````
python --version
````

6. Deactivate the environment by typing, 
````
deactivate
````
