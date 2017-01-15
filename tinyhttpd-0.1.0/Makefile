uname_S:=$(shell sh -c 'uname -s 2>/dev/null || echo not' )
CANLSOCK=-lsocket
#complie Linux
ifeq  ($(uname_S),Linux)
		CANLSOCK = 
endif
all: httpd
httpd: httpd.c
	gcc -W -Wall $(CANLSOCK) -lpthread -o tinyhttpd httpd.c
clean:
	rm tinyhttpd
