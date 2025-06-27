# Working inside a Python Virtual Environment
> [!IMPORTANT]
> For Vulture Raspberry Pi's, ALL Python programs must run in a dedicated Virtual Environment. Similarly, Python Packages must also be installed in the same Virtual Environment. This is best practice for running Python programs in RPi.

## Creating Python Virtual Environments
- install virtualenv and venv
  ```
  sudo apt update
  sudo apt install python3-virtualenv
  sudo apt install python3-venv
  ``` 
-  Create a new virtual environment
   ```
   python3 -m venv vulture-venv
   ```

## Naming Convention for Virtual Environment
- For the Vulture Swarm, the venv can follow the name **vulture-venv** for the sake of uniformity across all the RPis of the swarm.

## Activating and Deactivating
```
  source vulture-venv/bin/activate
```
- To deactivate, just run `deactivate`

