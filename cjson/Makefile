CC= gcc
CFLAGS= -O3 -Wall -pedantic -DNDEBUG  -I../src/ -fPIC -DENABLE_CJSON_GLOBAL=1

AR= ar rcu
RM= rm -f

LIB_O= dtoa.o  g_fmt.o  lua_cjson.o  strbuf.o

all: $(LIB_O)
	$(AR) libcjson.a *.o

$(LIB_O): %.o: %.c
	$(CC) -c $(CFLAGS) $< -o $@

clean:
	$(RM) *.o
	$(RM) *.a

