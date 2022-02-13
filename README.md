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

**For Windows:**
First, the desired python version has to be installed. To do that, go to [Traversy Media] https://www.python.org/downloads/windows/ and chose the version of your choice.







First install via pip,
````
pip install virtualenv

````
Navigate to the desired folder where the virtual environment should be installed,
````
cd C:\Users\my_project

````
Within the desired folder install your new environment with a specific Python version of your choice,
````
virtualenv my_venv --python=python3.8.8 

````
Activate the new environment,
````
cd C:\Users\my_project\my_venv\Scripts\activate.bat
````
Check the installed version,
````
python --version
````
Deactivate the environment by typing, 
````
deactivate.bat
````
