IDIR=./
CC=gcc
CFLAGS=-Wall -I$(IDIR)
OMP=-fopenmp

ODIR=build
SDIR=./

LIBS=-lm

_DEPS = bh_sim.h quadtree.h monitor.h cycletimer.h
DEPS = $(patsubst %,$(IDIR)/%,$(_DEPS))

_OBJ = bh_sim.o quadtree.o monitor.o cycletimer.o
OBJ = $(patsubst %,$(ODIR)/%,$(_OBJ))

BINS = barneshut

$(ODIR)/%.o: $(SDIR)/%.c $(DEPS) | build_dir
	$(CC) $(OMP) -c -o $@ $< $(CFLAGS) $(LIBS)

default: all
all: clean barneshut

barneshut: $(OBJ)
	$(CC) $(OMP) -o $@ $^ $(CFLAGS) $(LIBS)

.PHONY: build_dir
build_dir:
	mkdir -p $(ODIR)

.PHONY: clean
clean:
	rm -f -r $(ODIR) *~ $(BINS) $(IDIR)/*~ *.txt