# dicom_tools

PyQt4, sip and SimpleITK have to be installed

on mac you could install them with:

`brew install qt`

`brew install pyqt`

`brew install sip`

`brew install homebrew/science/simpleitk`

this package uses qt4, to install qt4 instead of qt5:
https://github.com/cartr/homebrew-qt4

on a debian linux:

`apt install python-pip python-qt4  python-sip`

on debian it is necessary to install also scikit-image and some other packages with apt:

`apt install python-skimage python-scipy python-matplotlib`

it could be necessary to upgrade pip before to install the package, as it could not find some dependencies:

`pip install --upgrade pip`

`apt install build-essential`

on CentOS 7 (or Scientific Linux):

`yum install centos-release-scl`

 `yum install python27`

`scl enable python27 bash`

`yum install python27-python-devel`

`yum install python27-pythyon-pip python27-python-six python27-numpy python27-scipy python27-python-tools`

Install Qt (I used `qt-unified-linux-x64-3.0.2-online.run`)

Install OpenGL headers, for QtGui and QtWidgets

`yum install freeglut-devel`

I manually compiled SIP but I'm not sure if it is enought to do so via pip (I used `sip-4.19.7`)

`python configure.py`

`make`

`make install`

Download PyQt source code (I tested PyQt5_gpl-5.10)

`python configure.py --qmake /path/to/Qt/5.10.0/gcc_64/bin/qmake`

`make`

`make install`

update pip and compile scikit

`pip install --upgrade pip`

`python -m pip install scikit-build`

finally, install the package with:

`python setup.py install`

on linux maybe you want to install it only for your user

`python setup.py install --user`

on debian it could be necessary to install ITK before SimpleITK

`apt install insighttoolkit4-python insighttoolkit4-examples libinsighttoolkit4-dev libinsighttoolkit4.10`

`pip uninstall SimpleITK`

`pip install SimpleITK`