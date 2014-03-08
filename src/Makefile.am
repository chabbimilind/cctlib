#include ../Makefile.inc
all:  libcctlib.a libcctlib_tree_based.a

libcctlib.a: cctlib.cpp
	$(CXX) -DUSE_SHADOW_FOR_DATA_CENTRIC  $(CFLAGS) $(CCTLIB_INCLUDES) -o cctlib.o cctlib.cpp
	$(AR) -cvq libcctlib.a cctlib.o

libcctlib_tree_based.a: cctlib.cpp
	$(CXX) -DUSE_TREE_BASED_FOR_DATA_CENTRIC  $(CFLAGS) $(CCTLIB_INCLUDES) -o cctlib_tree_based.o cctlib.cpp
	$(AR) -cvq libcctlib_tree_based.a cctlib_tree_based.o

clean:
	rm -f *.o *.a
