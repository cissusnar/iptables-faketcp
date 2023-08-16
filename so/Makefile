CFLAGS = -Wall -Wextra -Wl,-init=init
#-Wl,--verbose
LDFLAGS = -lxtables -DPIC -fPIC -shared -lm

%.so : %.c
	echo $(CC)
	$(CC) $(CFLAGS) $(LDFLAGS) $< -o $@

all: libipt_FAKETCP.so

clean:
	rm -f *.so

install:
	install -m 755 -t /lib/iptables/ *.so
