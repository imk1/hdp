CC = g++ -Wall
#CFLAGS = -g -Wall -O3 -ffast-math -DHAVE_INLINE -DGSL_RANGE_CHECK_OFF
# CFLAGS = -g -Wall
LDFLAGS = -lgsl -lm -lgslcblas

GSL_INCLUDE = /users/imk1/include
GSL_LIB = /users/imk1/lib

LSOURCE =  utils.cpp corpus.cpp state.cpp hdp.cpp main.cpp
LHEADER =  utils.h corpus.h hdp.h state.h

hdp: $(LSOURCE) $(HEADER)
	$(CC)  -I$(GSL_INCLUDE) -L$(GSL_LIB) $(LSOURCE) -o $@ $(LDFLAGS)

clean:
	rm -f *.o hdp
