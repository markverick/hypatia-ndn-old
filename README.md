You can install ndnSIM anywhere in your system

```
mkdir ndnSIM
cd ndnSIM
git clone https://github.com/named-data-ndnSIM/ns-3-dev.git ns-3
git clone https://github.com/named-data-ndnSIM/pybindgen.git pybindgen
git clone --recursive https://github.com/named-data-ndnSIM/ndnSIM.git ns-3/src/ndnSIM

# Build and install NS-3 and ndnSIM
cd ns-3
./waf configure -d optimized
./waf

sudo ./waf install
```

You need to specify the path to your ns-3/ndnSIM installation
Default path after running `sudo ./waf install` will be `/usr/local/lib/pkgconfig`

```
export PKG_CONFIG_PATH=/usr/local/lib/pkgconfig
export LD_LIBRARY_PATH=/usr/local/lib:$LD_LIBRARY_PATH

cd ns-3-sim
./waf configure
./waf --run <scenerio>
```