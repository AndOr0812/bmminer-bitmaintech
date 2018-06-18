environment setup:
need 2 PATH: toolchain base path and other open source lib binary and include files base path.

for example:
XILINX_BASE_PATH=/home/XILINX/gcc-linaro-arm-linux-gnueabihf-4.7-2012.11-20121123_linux
XILINX_OTHER_LIB_BASE_PATH=/home/XILINX/bin
export XILINX_OTHER_LIB_BASE_PATH
export XILINX_BASE_PATH

OBS: 
 If compiling on a armhf device : 
 1. apt-get update
 2. apt-get install build-essential git autoconf automake pkg-config libtool libcurl4-openssl-dev libncurses5-dev 
 3. apt-get install libusb-1.0-0-dev libudev-dev uthash-dev libjansson-dev  zlib1g-dev zlib1g  libc6-dev  dpkg-dev                 
4. cd /home
5. mkdir develop
6. cd develop

 XILINX_BASE_PATH=/usr
 XILINX_OTHER_LIB_BASE_PATH=/usr     (this will only look for libz.a and nothing else -so if libz.a is found in /usr/libs then ok, if found somewhere else then copy it to /usr/libs)
 
 export XILINX_OTHER_LIB_BASE_PATH
 export XILINX_BASE_PATH


SEE ALSO : https://bitcointalk.org/index.php?topic=4030824.0



How to compile:
1. set miner type value
./setminertype S9
option: S9   R4   T9   T9+

2. compile the code
make

