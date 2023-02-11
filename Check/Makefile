vpath %.h include  #vpath 指定搜索路径
vpath %.c sub
vpath %.c unit_test

LIBS += -lcheck -lm -lpthread -lrt -lsubunit
objects = sub.o test_sub.o


test: test_main.c $(objects)
	cc $(CFLAGS) -I include $^ -o test $(LIBS)

all: $(objects)
$(objects): %.o: %.c
	cc $(CFLAGS) -c -I include $< -o $@ $(LIBS)

.PHONY: clean
clean:
	rm *.o test