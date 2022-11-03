# HowtoPython-VirtualEnvironment
Some open source programs are not always immediately compatible with the latest Python version. Thus, it is suitable to create virtual environments and decouple your main Python and work within the virtual environment. This avoids that the different Python versions influence each other.<br />

The following description is a brief summary of [How to Install Multiple Python Versions]( https://k0nze.dev/posts/install-pyenv-venv-vscode/) from [k0nze](https://k0nze.dev/).

<br />

**For Linux:**<br />
For linux we will use the tool `pyenv`, which allows to create virtual environments very easily. However, for the installation of `pyenv` some actions must be considered first. `pyenv` is stored under `/home/user/.pyenv`.<br /> <br />

**1. Installation of `pyenv` - has only to be done once** <br />

1.1) Type into your terminal,
````
sudo apt install -y make build-essential libssl-dev zlib1g-dev \
libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev \
libncursesw5-dev xz-utils tk-dev libffi-dev liblzma-dev python3-openssl \
git
````

1.2) Under `/home/user/` clone the following repository from GitHub:
````
git clone https://github.com/pyenv/pyenv.git ~/.pyenv
````
  
1.3) Add `.pyenv` to `$Path`, 
````
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
echo 'eval "$(pyenv init --path)"' >> ~/.bashrc
````
  
1.4) Close your current terminal and open a new one, type `pyenv` and check if it works, 
````
pyenv
````
<br />

**2. Using `pyenv` and setting up virtual environments** <br />

2.1) Check possible Python versions which can be installed,
````
pyenv install -l
````

2.2) Install a desired Python version (installed in `home/user/.pyenv` => is installed locally, exactly what is wanted). For instance,
````
pyenv install 3.9.10
````

2.3) Check if installation worked,
````
pyenv versions
````

2.4) Check currently active version (should be the one of your `*system`), 
````
pyenv version
````

2.5) Create a new folder in `/home/user/`, in which all the future virtual environments will be saved,
````
mkdir venvs
````

2.6) Set in this folder a local Python version (which should be active also in the virtual env): pyenv local 3.8.8

````
pyenv install 3.9.10
````
12) Create virtual environment: python -m venv venv388

````
pyenv install 3.9.10
````

14) Activate virtual env: source venv388/bin/activate
15) Deactivate env: deactivate
16) Create a second virtual env, fist change the local Python version to the desired one: pyenv local 3.9.10
17) python -m venv venv3910
18) Activate the env: source venv3910/bin/activate
19) deactivate2.1)



<br />
<br />
<br />



**For Windows:**<br />
*Note:* There is the possibility of using `pyenv` for Windows. The installation procedure can be found here [How to Install Multiple Python Versions](https://k0nze.dev/posts/install-pyenv-venv-vscode/). However, in the following description `virtualenv` is used. <br />

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
