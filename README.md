# auto-py-to-exe

## How to create a executable file for python?

## Getting Started [auto-py-to-exe · PyPI](https://pypi.org/project/auto-py-to-exe/)

##    Prerequisites
     **Python : 3.6-3.11

To have the interface displayed in the images, you will need chrome. If chrome is not installed or --no-chrome is supplied, the default browser will be used.

As of PyInstaller 4.0, Python 2.7 is no longer supported. Read "Python 2.7 Support" below for steps on how to use this tool with Python 2.7.

## Installation and Usage Installing Via PyPI

You can install this project using PyPI:

`$ pip install auto-py-to-exe`
 Then to run it, execute the following in the terminal:

 `$ auto-py-to-exe`

> If you have more than one version of Python installed, you can use python -m auto_py_to_exe instead of `auto-py-to-exe.`

# Installing Via GitHub

```

$ git clone https://github.com/brentvollebregt/auto-py-to-exe.git
$ cd auto-py-to-exe
$ python setup.py install
```

Then to run it, execute the following in the terminal:

## `$ auto-py-to-exe`

## Running Locally Via Github (no install) You can run this project locally by following these steps:

1. Clone/download the repo
  
2. Open cmd/terminal and cd into the project
  
3. Execute `python -m pip install -r requirements.txt`
  

Now to run the application, execute `python -m auto_py_to_exe`. A Chrome window in app mode will open with the project running inside.

> Make sure you are in the directory below auto_py_to_exe (you will be after step 3) when calling `python -m auto_py_to_exe` or you will need to reference the folder auto_py_to_exe absolutely/relatively to where you currently are.

## Using the Application

1. Select your script location (paste in or use a file explorer)
  
  Outline will become blue when file exists
  
2. Select other options and add things like an icon or other files
  
3. Click the big blue button at the bottom to convert
  
4. Find your converted files in /output when completed
  
5. Easy.
  

## Arguments

Usage: `auto-py-to-exe [-nc] [-c [CONFIG]] [-o [PATH]] [filename]`

| Argument | Type | Description |
| --- | --- | --- |
| filename | positional/optional | Pre-fill the "Script Location" field in the UI. |
| -nc, --no-chrome | optional | Open the UI using the default browser (which may be Chrome). Will not try to find Chrome. |
| -nu, --no-ui | optional | Don't try to open the UI in a browser and simply print out the address that the application can be accessed at. |
| -c [CONFIG], --config [CONFIG] | optional | Provide a configuration file (json) to pre-fill the UI. These can be generated in the settings tab. |
| -o [PATH], --output-dir [PATH] | optional | Set the default output directory. This can still be changed in the ui. |
| -bdo [FOLDER_PATH], --build-directory-override [FOLDER_PATH] | optional | Override the default build directory. Useful if you need to whitelist a folder to stop your antivirus from removing files. |
| -lang [LANGUAGE_CODE], --language [LANGUAGE_CODE] | optional | Hint the UI what language it should default to when opening. Language codes can be found in the table under "Translations" below. |

> If you are running this package locally, you will need to call python -m auto_py_to_exe instead of auto-py-to-exe

## JSON Configuration

Instead of inserting the same data into the UI over and over again, you can export the current state by going to the "Configuration" section within the settings tab and exporting the config to a JSON file. This can then be imported into the UI again to re-populate all fields.

This JSON config export action does not save the output directory automatically as moving hosts could mean different directory structures. If you want to have the output directory in the JSON config, add the directory under `nonPyinstallerOptions.outputDirectory` in the JSON file (will need to create a new key).
