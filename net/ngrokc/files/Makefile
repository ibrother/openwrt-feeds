CFLAGS+= -Wall -fexceptions -DOPENSSL=1 -DOPENSSLDL=1
CXXFLAGS+= -Wall -fexceptions -DOPENSSL=1 -DOPENSSLDL=1

OLIBS=sendmsg.o openssldl.o cJSON.o nonblocking.o sslbio.o ngrok.o main.o

all:: ngrokc $(OLIBS)

ngrokc: $(OLIBS)
	$(CXX) -s $(OLIBS) -o ngrokc

sendmsg.o: sendmsg.h
openssldl.o: openssldl.h
cJSON.o: cJSON.h
nonblocking.o: nonblocking.h
sslbio.o: sslbio.h
ngrok.o: ngrok.h
main.o: sendmsg.h openssldl.h sslbio.h ngrok.h cJSON.h bytestool.h nonblocking.h

clean:
	rm -f $(OLIBS) ngrokc
