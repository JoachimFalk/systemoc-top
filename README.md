# To fetch git submodules

- git submodule update --init --recursive

# To build

- ./autoreconf.sh
- mkdir obj
- cd obj/
- ../configure -C
- make

# Now run test cases to check your build
- make check
