##Requirements:
* Craftcoin
* Python
* Twisted
* python-argparse (for Python <=2.6)
* litecoin_scrypt (included)

##Update - Important!
* Those updating to v13.1 from an older version will need to setup a new as it is not compatible with the old version.
* The P2Pool communication port has changed to 23630.


##Setup:
####Linux:
If Python version <= 2.6 : `sudo apt-get install python-argparse`

    sudo apt-get install python-zope.interface python-twisted python-twisted-web
    cd litecoin_scrypt
    sudo python setup.py install

####Windows:
* Install [MinGW](http://www.mingw.org/wiki/Getting_Started)
* Install [Python 2.7](http://www.python.org/getit/)
* Install [Twisted](http://twistedmatrix.com/trac/wiki/Downloads)
* Install [Zope.Interface](http://pypi.python.org/pypi/zope.interface/3.8.0)
* Install [python win32 api](http://sourceforge.net/projects/pywin32/files/pywin32/Build%20218)
* Install [python win32 api wmi wrapper](https://pypi.python.org/pypi/WMI/#downloads)
* Unzip the files into C:\Python27\Lib\site-packages
* In MinGW bash:

    cd litecoin_scrypt
    C:\Python27\python.exe setup.py build --compile=mingw32 install

If you run into an error with unrecognized command line option '-mno-cygwin', see [this](http://stackoverflow.com/questions/6034390/compiling-with-cython-and-mingw-produces-gcc-error-unrecognized-command-line-o)

####Mac:

You're on your own, pal.


##Running P2Pool:
To use P2Pool for Craftcoin, you must be running your own local craftcoind. For standard
configurations, using P2Pool should be as simple as:

    python run_p2pool.py --net craftcoin

Then run your miner program, connecting to 127.0.0.1 on port 8830 with any
username and password.

If you are behind a NAT, you should enable TCP port forwarding on your
router. Forward port 23630 to the host running P2Pool.

Run for additional options.

    python run_p2pool.py --help


###Credits and Donations:
* [forrestv](https://github.com/forrestv) (Original P2Pool): 1HNeqi3pJRNvXybNX4FKzZgYJsdTSqJTbk
* [testzcrypto](https://github.com/testzcrypto) (Conversion to Craftcoin): QKTCHBMHajXsrdDVGW33wtuHA7wfvswLnJ
* [CartmanSPC](https://bitcointalk.org/index.php?action=profile;u=101393) (Conversion to Craftcoin): QBFBJs6KBX2GZogVdti6Ui6Zyx81gYPuVE

###Official wiki:
https://en.bitcoin.it/wiki/P2Pool

###Alternate web front end:
https://github.com/hardcpp/P2PoolExtendedFrontEnd
