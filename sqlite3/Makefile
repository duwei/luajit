CC= gcc
CFLAGS= -O2 -Wall -DLUA_COMPAT_ALL -fPIC -DSQLITE_THREADSAFE=0

AR= ar rcu
RM= rm -f

LIB_O=sqlite3.o shell.o

all: $(LIB_O)
	$(AR) libsqlite3.a *.o

$(LIB_O): %.o: %.c
	$(CC) -c $(CFLAGS) $< -o $@

clean:
	$(RM) *.o
	$(RM) *.a

