## MEPViewer
A pyqtgraph application for viewing and interpreting EMG data

### System Prerequisites
#### Windows
* A Terminal: you can use `cmd.exe` but I recommend [Git for Windows](https://msysgit.github.io/)
* [Python 2.7.x](https://www.python.org)
  * Install python into the default option `C:\Python27` if you can.  Then, edit your PATH environment variable to include `C:\Python27` (instructions [here](https://www.microsoft.com/resources/documentation/windows/xp/all/proddocs/en-us/sysdm_advancd_environmnt_addchange_variable.mspx?mfr=true)).
* [Pip](https://pypi.python.org/pypi/pip) for python package management
  * Pip is included in the standard python installation on windows.  Simply add the `C:\Python27\Scripts` directory to your `PATH` variable (separate directories using a semicolon), and pip should be accessible from the command line.

#### Mac OS X
* [Python 2.7.x](https://www.python.org)
* [Pip](https://pypi.python.org/pypi/pip) for python package management
  * First, try this: open a terminal and run the command `sudo easy_install pip`.  If this doesn't work,
  * Download [get-pip.py](https://raw.githubusercontent.com/pypa/pip/master/contrib/get-pip.py) and run the command `sudo python /path/to/get-pip.py` in your terminal.

=

### Python prerequisites
=
#### Windows
Many of these packages have been archived by Christopher Gohlke in order to be easy to install.  For several of these requirements, I'll link to his [Unofficial Windows Binaries page](http://www.lfd.uci.edu/~gohlke/pythonlibs/).  Simply find the package you want, select the correct version based on your architecture (32- or 64-bit) and python version (use "27" or "26" depending on the version of Python you downloaded).  For example:

| Your Python Version  | Your system architecture | You should download |
| -------------------- | ------------------------ | ------------------- |
| 2.6.x  | 32-bit  | numpy‑1.9.2+mkl‑cp26‑none‑win32.whl|
|        | 64-bit  | numpy‑1.9.2+mkl‑cp26‑none‑win_amd64.whl|
| 2.7.x  | 32-bit  | numpy-1.9.2+mkl-cp27-none-win32.whl|
|        | 64-bit  | numpy‑1.9.2+mkl‑cp27‑none‑win_amd64.whl|

A wheel is a ZIP-format archive with a specially formatted filename and the .whl extension. More info on python wheels [here](https://pypi.python.org/pypi/wheel).  Once you download the correct wheel file, use pip in the terminal to install it:
```bash
pip install C:\Users\chris\Downloads\numpy‑1.9.2+mkl‑cp27‑none‑win_amd64.whl
```

* [NumPy](http://www.numpy.org/) for numerical computing
  * [Gohlke's NumPy+MKL packages](http://www.lfd.uci.edu/~gohlke/pythonlibs/#numpy)
  * Alternatively, try the most recent supported version [ 1.9.2 available on the sourceforge page](http://sourceforge.net/projects/numpy/files/NumPy/1.9.2/) (not much advantage since Gohlke has archived 1.9.2).
* [neo](https://pythonhosted.org/neo/) for reading electrophysiology data in Python
  * Run the command `pip install neo` in your terminal.
* [PyQt4](http://www.riverbankcomputing.com/software/pyqt/download)
  * [Gohlke's PyQt4 packages](http://www.lfd.uci.edu/~gohlke/pythonlibs/#pyqt4)
* [PyQtGraph](http://www.pyqtgraph.org/)
  * On Gohlke's download page under "Misc".  Search for the file `pyqtgraph‑0.9.10‑py2.py3‑none‑any.whl`
  * Alternatively, the [PyQtGraph homepage](http://www.pyqtgraph.org/) has windows installers.
 
=
#### Mac OS X
* [NumPy](http://www.numpy.org/) for numerical computing
  * Run `sudo pip install numpy` in your terminal.
* [neo](https://pythonhosted.org/neo/) for reading electrophysiology data in Python
  * Run `sudo pip install neo` in your terminal.

[ImportError: cannot import name _thread](http://stackoverflow.com/questions/27630114/matplotlib-issue-on-os-x-importerror-cannot-import-name-thread) -- Sometimes the matplotlib install fails on newer versions of OSX. The fix mentioned in the link is:
```bash
sudo pip uninstall python-dateutil
sudo pip install python-dateutil==2.2
```

### Download the MEPViewer
If you have [git](https://git-scm.com/) available in your command line or terminal, execute:
```bash
git clone git://github.com/chrismullins/MEPViewer.git
```
or simply download and extract the tarball from this page.
