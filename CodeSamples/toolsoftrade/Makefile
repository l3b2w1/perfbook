# This program is free software; you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation; either version 2 of the License, or
# (at your option) any later version.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with this program; if not, you can access it online at
# http://www.gnu.org/licenses/gpl-2.0.html.
#
# Copyright (c) 2009 Paul E. McKenney, IBM Corporation.

include ../Makefile.arch

PROGS =	forkjoin \
	forkjoinperf \
	forkjoinvar \
	lock \
	mytrue \
	pcreate \
	rwlockscale

all: $(PROGS)

forkjoin: forkjoin.c ../api.h
	cc $(GCC_ARGS) -o forkjoin forkjoin.c

forkjoinperf: forkjoinperf.c
	cc $(GCC_ARGS) -o forkjoinperf forkjoinperf.c

forkjoinvar: forkjoinvar.c ../api.h
	cc $(GCC_ARGS) -o forkjoinvar forkjoinvar.c

lock: lock.c ../api.h
	cc $(GCC_ARGS) -o lock lock.c -lpthread

mytrue: mytrue.c
	cc $(GCC_ARGS) -o mytrue mytrue.c

pcreate: pcreate.c ../api.h
	cc $(GCC_ARGS) -o pcreate pcreate.c -lpthread

rwlockscale: rwlockscale.c ../api.h
	cc $(GCC_ARGS) -o rwlockscale rwlockscale.c -lpthread

clean:
	rm -f $(PROGS) *.o
