# Tested on FreeBSD, Ubuntu 10.04 and Cygwin
CC=g++
CFLAGS=-c -Wall -std=c++17 -pedantic
CPPFLAGS=-I/usr/local/opt/openssl/include
#LDFLAGS=-lcrypto -lssl
LDFLAGS=-L/usr/local/opt/openssl/lib
all: test_client

test_client: test_client.o openssl_hostname_validation.o
	$(CC) test_client.o openssl_hostname_validation.o -o test_client $(LDFLAGS)

clean:
	rm -rf *.o test_client
