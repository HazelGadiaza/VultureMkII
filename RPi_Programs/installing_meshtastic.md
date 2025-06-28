# Installing Meshtastic
Follow this guide: [Installing Python CLI](https://meshtastic.org/docs/software/python/cli/installation/)

<br>

## Common Errors encountered

### 1. Cannot install serial driver CH9102 yet
Because Meshtastic devices haven't arrived yet (as of June 25, 2025).

### 2. Error installing Pytap2
After running `pip3 install --upgrade pytap2`, an error message `error:externally-managed-environment` appeared.
To install Pytap2, a python3 virtual environment must be created. A guide to creating a virtual environment is also detailed in the installation guide page but an error was also encountered.


### 3. Cannot install `python-virtualenvwrapper` to create a Python virtual environment. Use `venv` as alternative
Error message was: `sudo: pacman: command not found` <br>
So an alternative approach is to use **venv** to create a python virtual environment following [this guide from linuxconfig.org](https://linuxconfig.org/creating-and-managing-python-virtual-environments-with-virtualenv-on-ubuntu-debian)

CREATING A VIRTUAL ENVIRONMENT
- install virtualenv and venv
  ```
  sudo apt update
  sudo apt install python3-virtualenv
  sudo apt install python3-venv
  ``` 
-  Create a new virtual environment
   ```
   python3 -m venv meshtastic-client
   ```
- Activate the virtual environment
  ```
  source meshtastic-client/bin/activate
  ```
- Once activated, your terminal prompt will show the name of the activated environment. Meaning, any Python commands you run will now use the environment’s Python interpreter and configuration.
- After creating a python virtual environment, install the Pytap2 and Meshtastic
  ```
  pip3 install --upgrade pytap2
  pip3 install --upgrade "meshtastic[cli]"
  ```
- To deactivate, just run `deactivate`
