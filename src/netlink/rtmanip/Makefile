include $(GOROOT)/src/Make.inc

TARG=netlink/rtmanip

DEPS=../


GOFILES=\
	links.go\


include $(GOROOT)/src/Make.pkg


tester: tester.go _obj/nl3.a route/_obj/nl3/route.a
	$(GC) -o $@.6 $<
	$(LD) -L_obj -Lroute/_obj -o $@ $@.6

modules:
	$(MAKE) -C route
	$(MAKE) -C link 
	$(MAKE) -C addr

modules_install:
	$(MAKE) -C route install
	$(MAKE) -C link  install
	$(MAKE) -C addr  install
