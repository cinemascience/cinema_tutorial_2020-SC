
# Cinema SuperComputing Tutorial 2020

This tutorial introduces core Cinema concepts and functionality.  As part of this tutorial, you will export a Cinema database from ParaView and run a Jupyter notebook workflow that takes in a Cinema database, updates it by calculating various image statistics and then views the new Cinema database in a browswer-based Cinema:Explorer viewer.  

To run this tutorial, you will need:

- The latest version of [ParaView:](https://www.paraview.org/download/)
- Python 3.7 or above
- pandas, numpy
- os, shutil
- cinemasci v1.1 or above
- openCV 4.4 or above
- skimage (scikit-image)
- notebook, jupyterlab


## A Note on Browser Security
To use Cinema:Explorer, you must allow local file access. Do this in the following way, but be sure to reset these options when you are done:

- **Firefox (preferred)**
    - type ```about:config``` in the navigaion bar
        - set ```privacy.file_unique_origin``` to **false**
        - set ```security.fileuri.strict_origin_policy``` to **false**
- **Safari**
    - Safari->Preferences->Advanced->Show Develop menu in menu bar
    - Safari->Develop->Disable Local File Restrictions (on)
- **Chrome**
    - open **chrome** with the option ```--disable-web-security```
    - Mac example:
        - ```open -na "Google Chrome" cinema_explorer.html --args --user-data-dir="YOUR_PATH_TO_REPO" --disable-web-security```


## Starting the server

```
    python -m cinemasci.server --port 8200 --viewer view --data data/sphere.cdb
```
