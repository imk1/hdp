CC = g++ -Wall
#CC = g++ -ansi -Wall -pedantic
#CFLAGS = -g -Wall -O3 -ffast-math -DHAVE_INLINE -DGSL_RANGE_CHECK_OFF
# CFLAGS = -g -Wall
LDFLAGS = -lgsl -lm -lgslcblas #-latlas

GSL_INCLUDE = /users/imk1/include
GSL_LIB = /users/imk1/lib

GSL_INCLUDE_MAC = $(GSL_INCLUDE) 
GSL_LIB_MAC = $(GSL_LIB)

LSOURCE = main.cpp utils.cpp stirln.cpp corpus.cpp state.cpp
LHEADER = utils.h stirln.h corpus.h state.h

mac: $(LSOURCE) $(HEADER)
	  $(CC) -I$(GSL_INCLUDE_MAC) -L$(GSL_LIB_MAC) $(LSOURCE) -o hdp $(LDFLAGS)

mac-d: $(LSOURCE) $(HEADER)
	  $(CC) -g -I$(GSL_INCLUDE_MAC) -L$(GSL_LIB_MAC) $(LSOURCE) -o hdp $(LDFLAGS)

linux: $(LSOURCE) $(HEADER)
	  $(CC) -I$(GSL_INCLUDE) -L$(GSL_LIB) $(LSOURCE) -o hdp $(LDFLAGS)

linux-d: $(LSOURCE) $(HEADER)
	  $(CC) -g -I$(GSL_INCLUDE) -L$(GSL_LIB) $(LSOURCE) -o hdp $(LDFLAGS)


clean:
	-rm hdp
