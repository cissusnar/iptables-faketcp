CFLAGS = -Wall -Wextra -Wl,-init=init
#-Wl,--verbose
LDFLAGS = -lxtables -DPIC -fPIC -shared -lm
XTABLES_SO_DIR	?= $(shell pkg-config xtables --variable xtlibdir)

%.so : %.c
	$(CC) $(CFLAGS) $(LDFLAGS) $< -o $@

all: libipt_FAKETCP.so

clean:
	rm -f *.so

install:
	install -m 755 -t "${XTABLES_SO_DIR}/" *.so
