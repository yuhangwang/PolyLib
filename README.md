# PolyLib
**A library of polyhedral functions**

This is an unofficial verbatim redistribution of the binary&source form of the PolyLib library (a prerequisite for compiling programs like CLooG), under the terms of GPL 3.0 license.

This redistribution is under the the same GPL 3.0.

Please visit the official website for more details: http://icps.u-strasbg.fr/polylib/

## Usage
The binary/ folder contains both a tar.gz file and a folder, which are equivalent. You can use either one.

## Compilation notes
### Compilation environment
* CentOS 6.6
* x86_64 architecture
* Compiler: gcc version 4.4.7 20120313 (Red Hat 4.4.7-11)

### Compilation steps
```bash
wget http://icps.u-strasbg.fr/polylib/polylib_src/polylib-5.22.5.tar.gz
tar xvf polylib-5.22.5.tar.gz
mkdir build_polylib-5.22.5
cd build_polylib-5.22.5
../polylib-5.22.5/configure --prefix=/home/steven/install/libpolylib/5.22.5 --with-libgmp=/home/steven/install/libgmp/4.3.2 --enable-int-lib --enable-longint-lib --enable-longlongint-lib
make -j10
make check -j10 | tee QualityVerification.txt
make install
```

### Quality verification
See the "QualityVerification.txt" for the output of "make check".