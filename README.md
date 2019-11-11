# dedisp
This repositry is derived from Ben Barsdell's original GPU De-dedispersion library (code.google.com/p/dedisp)

Installation Instructions:

  1.  git clone https://github.com/ajameson/dedisp.git
  2.  Update Makefile.inc with your CUDA path, Install Dir and GPU architecture. e.g.
      * CUDA_PATH ?= /usr/local/cuda-8.0.61
      * INSTALL_DIR = $(HOME)/opt/dedisp
      * GPU_ARCH = sm_60
  3.  make && make install
  
  This will build a shared object library named libdedisp.so which is a prerequisite for Heimdall. The dedisp header files will be installed into INSTALL_DIR/include and the library into INSTALL_DIR/lib.
  
  This fork just adds the mkdir commands to the makefile, since the original make fails if the directory does not already exist.
  If trying to use this library with any other astronomy tool, for example, heimdall-astro, add the /lib/ subdirectory of the installation path to LD_LIBRARY_PATH. 
