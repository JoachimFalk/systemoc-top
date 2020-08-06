
To build:

./autoreconf.sh
mkdir obj
cd obj/
../configure -C
make

# Now run test cases to check your build
make check
