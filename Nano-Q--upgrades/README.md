# Some improvements to Nano-Q:

These files holds some changes that make Nano-Q a bit faster or more predictable.

1. I changed getSomeHam() to cython code.
  - This increased the speed by 50%
2. I added a -t option, so that Nano-Q does not launch all subprocess at once.
  - threadsInt is a new variable that is set to three threads at default
  - doSomeSubprocess() now has threadsInt=3 option to controll the number of threads
  - It looks like a good jump value would be 100 to 500 reads. A jump of 10 causes subprocess
    to complete and relaunch a new suprocess to quickly, thus reducing the efficancy.

## How to use:

1. pip3 install Cython
  - Installs cython so can build cython code
3. Copy these files to your Nano-Q directory
4. delete scribbles.py from you Nano-Q directory (this gets replaced by scribbles.pxy)
5. Run: python setup.py build_ext --inplace
