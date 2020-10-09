## CinemaViewer Jupyter notebook component

A Jupyter notebook with components to run a simple viewer for one or more Cinema databases.  Designed for the use case of fully populated cinema databases of common format images. 

# Requirements

- python 3
- jupyter

# Usage

## Starting Jupyter Notebook

Run Jupyter and select the **cinema_module.ipynb** file

```
$ jupyter notebook
```

## Loading a Cinema Database

Looking at the python code, you load the `cinemasci` module, then create a cinema viewer.

```
import cinemasci

# create a viewer object
viewer = cinemasci.pynb.CinemaViewer()
# load one or more cinema databases
viewer.load("data/sphere.cdb data/sphere_01.cdb")
```

Optionally, set layout properties of the viewer.

```
# set a horizontal orientation (defualt is vertical)
viewer.setLayoutToHorizontal()
# set the height of the viewer
viewer.setHeight(250)
```

## UI manipulation

Manipulate UI-based controls.

```
# list UI controller names
viewer.getUINames()
# list all UI controller names with current value
viewer.getUIValues()
# list all possible values for a UI controller
viewer.getUIOptions('image size')
# return the current value for a UI controller
viewer.getUIValue('image size')
# set the value for any UI controller
viewer.setUIValues({'image size': 200})
# hide the controller of UI parameter 
viewer.hideUIControl('image size')
# show the controller of UI Parameter 
viewer.showUIControl('image size')
```

Manipulate Parameter-based controls.

```
# list data parameter names
viewer.getParameterNames()
# list data parameter names with current value
viewer.getParameterValues()
# list all possible values for a data parameter
viewer.getParameterOptions('phi')
# return the current value for a data parameter
viewer.getParameterValue('phi')
# set the value for any data parameter controller
viewer.setParameterValues({'theta': 72, 'phi': -108})
# hide the controller of data parameter
viewer.hideParameterControl('time')
# show the controller of data parameter
viewer.showParameterControl('time')
```


Contact `cinema-info@lanl.gov` for more information.
