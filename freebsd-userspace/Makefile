include ../config.inc

include $(RTEMS_MAKEFILE_PATH)/Makefile.inc
include $(RTEMS_CUSTOM)
include $(PROJECT_ROOT)/make/leaf.cfg

CFLAGS += -Iinclude 
CFLAGS += -Irtems/include 
CFLAGS += -Ilib/libc/include 
CFLAGS += -Ilib/libc/resolv 
CFLAGS += -Ilib/netgraph
CFLAGS += -Ilib/libmemstat
CFLAGS += -Ilib/libutil
CFLAGS += -Ilib/libkvm
CFLAGS += -Isys
CFLAGS += -Ilocal 
# XXX hack to find rpc
CFLAGS += -I../services/librpc/include 
# nsparser needs this
CFLAGS += -Ilib/libc/net

CFLAGS += -I$(INSTALL_BASE)/include

#Only needed for route
# CFLAGS += -D__BSD_VISIBLE=1
#Only Needed for db files
CFLAGS += -D__DBINTERFACE_PRIVATE

CFLAGS += -g 
CFLAGS += -w 
CFLAGS += -std=gnu99
CFLAGS += -MT $@ -MD -MP -MF $(basename $@).d

C_FILES =
C_FILES += lib/libc/inet/inet_addr.c
C_FILES += lib/libc/inet/inet_cidr_ntop.c
C_FILES += lib/libc/inet/inet_cidr_pton.c
C_FILES += lib/libc/inet/inet_lnaof.c
C_FILES += lib/libc/inet/inet_makeaddr.c
C_FILES += lib/libc/inet/inet_net_pton.c
C_FILES += lib/libc/inet/inet_ntop.c
C_FILES += lib/libc/inet/inet_neta.c
C_FILES += lib/libc/inet/inet_net_ntop.c
C_FILES += lib/libc/inet/inet_netof.c
C_FILES += lib/libc/inet/inet_network.c
C_FILES += lib/libc/inet/inet_ntoa.c
C_FILES += lib/libc/inet/inet_pton.c
C_FILES += lib/libc/inet/nsap_addr.c

C_FILES += lib/libc/net/base64.c
C_FILES += lib/libc/net/ether_addr.c
C_FILES += lib/libc/net/getaddrinfo.c
C_FILES += lib/libc/net/gethostbydns.c
C_FILES += lib/libc/net/gethostbyht.c
C_FILES += lib/libc/net/gethostbynis.c
C_FILES += lib/libc/net/gethostnamadr.c
C_FILES += lib/libc/net/getifaddrs.c
C_FILES += lib/libc/net/getifmaddrs.c
C_FILES += lib/libc/net/getnameinfo.c
C_FILES += lib/libc/net/getnetbydns.c
C_FILES += lib/libc/net/getnetbyht.c
C_FILES += lib/libc/net/getnetbynis.c
C_FILES += lib/libc/net/getnetnamadr.c
C_FILES += lib/libc/net/getproto.c
C_FILES += lib/libc/net/getprotoent.c
C_FILES += lib/libc/net/getprotoname.c
C_FILES += lib/libc/net/getservent.c
C_FILES += lib/libc/net/nsdispatch.c
C_FILES += lib/libc/net/gai_strerror.c
# The following two /net files are generated
C_FILES += lib/libc/net/nslexer.c
C_FILES += lib/libc/net/nsparser.c
C_FILES += lib/libc/gen/err.c
C_FILES += lib/libc/gen/gethostname.c
C_FILES += lib/libc/nameser/ns_name.c
C_FILES += lib/libc/nameser/ns_netint.c
C_FILES += lib/libc/nameser/ns_parse.c
C_FILES += lib/libc/nameser/ns_print.c
C_FILES += lib/libc/nameser/ns_samedomain.c
C_FILES += lib/libc/nameser/ns_ttl.c
C_FILES += lib/libc/net/if_indextoname.c
C_FILES += lib/libc/net/if_nameindex.c
C_FILES += lib/libc/net/if_nametoindex.c
C_FILES += lib/libc/net/linkaddr.c
ifneq ($(DISABLE_IPV6),yes)
C_FILES += lib/libc/net/map_v4v6.c
endif
# This file is not IPV6 specific
C_FILES += lib/libc/net/name6.c
C_FILES += lib/libc/net/rcmd.c
C_FILES += lib/libc/net/recv.c
# C_FILES += lib/libc/net/send.c
C_FILES += lib/libc/resolv/herror.c
C_FILES += lib/libc/resolv/h_errno.c
C_FILES += lib/libc/resolv/res_comp.c
C_FILES += lib/libc/resolv/res_data.c
C_FILES += lib/libc/resolv/res_debug.c
C_FILES += lib/libc/resolv/res_findzonecut.c
C_FILES += lib/libc/resolv/res_init.c
C_FILES += lib/libc/resolv/res_mkquery.c
C_FILES += lib/libc/resolv/res_mkupdate.c
C_FILES += lib/libc/resolv/res_query.c
C_FILES += lib/libc/resolv/res_send.c
C_FILES += lib/libc/resolv/res_state.c
C_FILES += lib/libc/resolv/res_update.c
C_FILES += lib/libc/resolv/mtctxres.c
C_FILES += lib/libc/string/strsep.c
C_FILES += lib/libc/stdlib/strtonum.c

C_FILES += lib/libc/isc/ev_streams.c
C_FILES += lib/libc/isc/ev_timers.c

C_FILES += lib/libc/stdio/fgetln.c

C_FILES += lib/libc/db/db/db.c
C_FILES += lib/libc/db/btree/bt_close.c   
C_FILES += lib/libc/db/btree/bt_get.c       
C_FILES += lib/libc/db/btree/bt_put.c     
C_FILES += lib/libc/db/btree/bt_utils.c
C_FILES += lib/libc/db/btree/bt_conv.c    
C_FILES += lib/libc/db/btree/bt_open.c      
C_FILES += lib/libc/db/btree/bt_search.c
C_FILES += lib/libc/db/btree/bt_debug.c   
C_FILES += lib/libc/db/btree/bt_overflow.c  
C_FILES += lib/libc/db/btree/bt_seq.c
C_FILES += lib/libc/db/btree/bt_delete.c  
C_FILES += lib/libc/db/btree/bt_page.c      
C_FILES += lib/libc/db/btree/bt_split.c
C_FILES += lib/libc/db/recno/rec_close.c   
C_FILES += lib/libc/db/recno/rec_get.c   
C_FILES += lib/libc/db/recno/rec_put.c     
C_FILES += lib/libc/db/recno/rec_seq.c
C_FILES += lib/libc/db/recno/rec_delete.c  
C_FILES += lib/libc/db/recno/rec_open.c  
C_FILES += lib/libc/db/recno/rec_search.c  
C_FILES += lib/libc/db/recno/rec_utils.c

C_FILES += lib/libc/db/mpool/mpool.c

# libmemstat
C_FILES += lib/libmemstat/memstat_all.c
C_FILES += lib/libmemstat/memstat.c
C_FILES += lib/libmemstat/memstat_malloc.c
C_FILES += lib/libmemstat/memstat_uma.c

# libutil
C_FILES += lib/libutil/expand_number.c
C_FILES += lib/libutil/humanize_number.c
C_FILES += lib/libutil/trimdomain.c

# libipsec files
C_FILES += lib/libipsec/pfkey_dump.c
# Has a main and may or may not be needed
# C_FILES += lib/libipsec/test-policy.c
C_FILES += lib/libipsec/pfkey.c
C_FILES += lib/libipsec/ipsec_strerror.c
C_FILES += lib/libipsec/ipsec_get_policylen.c
C_FILES += lib/libipsec/ipsec_dump_policy.c
# The following two /net files are generated
C_FILES += lib/libipsec/policy_token.c
C_FILES += lib/libipsec/policy_parse.c

C_FILES += lib/libc_r/uthread/uthread_select.c
C_FILES += lib/libc_r/uthread/uthread_kern.c

# RTEMS Specific Files
# C_FILES += rtems/rtems-net-setup.c
C_FILES += rtems/syslog.c
C_FILES += rtems/rtems-kvm.c
C_FILES += rtems/rtems-kvm-symbols.c
C_FILES += rtems/rtems-syslog-initialize.c
C_FILES += rtems/rtems-getprogname.c
C_FILES += rtems/rtems-uthread_main_np.c
C_FILES += rtems/rtems-uthread_kevent.c
C_FILES += rtems/rtems-uthread_kqueue.c
C_FILES += rtems/rtems-shell.c
C_FILES += rtems/rtems-syspoll.c
C_FILES += rtems/rtems-uthread_init.c
C_FILES += rtems/rtems-get_curthread.c

# ping command sources
C_FILES += commands/sbin/ping/ping.c
ifneq ($(DISABLE_IPV6),yes)
C_FILES += commands/sbin/ping6/ping6.c
endif

# route command sources
C_FILES += commands/sbin/route/route.c

# dhclient command sources
C_FILES += commands/sbin/dhclient/alloc.c
C_FILES += commands/sbin/dhclient/bpf.c
C_FILES += commands/sbin/dhclient/clparse.c
C_FILES += commands/sbin/dhclient/conflex.c
C_FILES += commands/sbin/dhclient/convert.c
C_FILES += commands/sbin/dhclient/dhclient.c
C_FILES += commands/sbin/dhclient/dispatch.c
C_FILES += commands/sbin/dhclient/errwarn.c
C_FILES += commands/sbin/dhclient/hash.c
C_FILES += commands/sbin/dhclient/inet.c
C_FILES += commands/sbin/dhclient/options.c
C_FILES += commands/sbin/dhclient/packet.c
C_FILES += commands/sbin/dhclient/parse.c
C_FILES += commands/sbin/dhclient/privsep.c
C_FILES += commands/sbin/dhclient/tables.c
C_FILES += commands/sbin/dhclient/tree.c

# ifconfig command sources
# UNUSED IFCONFIG_C_FILES += commands/sbin/ifconfig/af_atalk.c
IFCONFIG_C_FILES += commands/sbin/ifconfig/af_inet.c
IFCONFIG_C_FILES += commands/sbin/ifconfig/af_link.c
IFCONFIG_C_FILES += commands/sbin/ifconfig/ifbridge.c
IFCONFIG_C_FILES += commands/sbin/ifconfig/ifclone.c
IFCONFIG_C_FILES += commands/sbin/ifconfig/ifgif.c
IFCONFIG_C_FILES += commands/sbin/ifconfig/ifgroup.c
IFCONFIG_C_FILES += commands/sbin/ifconfig/iflagg.c
IFCONFIG_C_FILES += commands/sbin/ifconfig/ifmedia.c
IFCONFIG_C_FILES += commands/sbin/ifconfig/ifvlan.c
ifneq ($(DISABLE_IPV6),yes)
IFCONFIG_C_FILES += commands/sbin/ifconfig/af_inet6.c
IFCONFIG_C_FILES += commands/sbin/ifconfig/af_nd6.c
endif
IFCONFIG_C_FILES += commands/sbin/ifconfig/ifcarp.c
IFCONFIG_C_FILES += commands/sbin/ifconfig/ifconfig.c
IFCONFIG_C_FILES += commands/sbin/ifconfig/ifgre.c
# UNUSED IFCONFIG_C_FILES += commands/sbin/ifconfig/ifieee80211.c
# UNUSED IFCONFIG_C_FILES += commands/sbin/ifconfig/ifmac.c
IFCONFIG_C_FILES += commands/sbin/ifconfig/ifpfsync.c

# The following two files were left out to avoid
# porting issues.  regdomain uses an xml parser
# that is not part of the standard release and
# af_ipx uses thread0 which we are trying to avoid
# pulling in.
#
# C_FILES += commands/sbin/ifconfig/regdomain.c
# C_FILES += commands/sbin/ifconfig/af_ipx.c

# netstat command sources
# no need to support AppleTalk yet
# NETSTAT_C_FILES += commands/usr.bin/netstat/atalk.c
NETSTAT_C_FILES += commands/usr.bin/netstat/bpf.c
NETSTAT_C_FILES += commands/usr.bin/netstat/if.c
ifneq ($(DISABLE_IPV6),yes)
NETSTAT_C_FILES += commands/usr.bin/netstat/inet6.c
endif
NETSTAT_C_FILES += commands/usr.bin/netstat/inet.c
NETSTAT_C_FILES += commands/usr.bin/netstat/ipsec.c
# no need to support IPX yet
# NETSTAT_C_FILES += commands/usr.bin/netstat/ipx.c
NETSTAT_C_FILES += commands/usr.bin/netstat/main.c
# XXX does not compile yet
NETSTAT_C_FILES += commands/usr.bin/netstat/mbuf.c
ifneq ($(DISABLE_IPV6),yes)
NETSTAT_C_FILES += commands/usr.bin/netstat/mroute6.c
endif
NETSTAT_C_FILES += commands/usr.bin/netstat/mroute.c
# Disable netgraph support - this is a long thread to pull
# NETSTAT_C_FILES += commands/usr.bin/netstat/netgraph.c
NETSTAT_C_FILES += commands/usr.bin/netstat/pfkey.c
# Actually just route.c in FreeBSD
NETSTAT_C_FILES += commands/usr.bin/netstat/netstat_route.c
NETSTAT_C_FILES += commands/usr.bin/netstat/sctp.c
NETSTAT_C_FILES += commands/usr.bin/netstat/unix.c

C_O_FILES = $(C_FILES:%.c=%.o)
C_D_FILES = $(C_FILES:%.c=%.d)

IFCONFIG_C_O_FILES = $(IFCONFIG_C_FILES:%.c=%.o)
IFCONFIG_C_D_FILES = $(IFCONFIG_C_FILES:%.c=%.d)

NETSTAT_C_O_FILES = $(NETSTAT_C_FILES:%.c=%.o)
NETSTAT_C_D_FILES = $(NETSTAT_C_FILES:%.c=%.d)

LIB = libbsdc.a
IFCONFIG = commands/sbin/ifconfig/ifconfig.rel
NETSTAT = commands/usr.bin/netstat/netstat.rel

COMMAND_RELS = $(NETSTAT) $(IFCONFIG)

GEN_FILES = rtems/rtems-kvm-symbols.c
GEN_FILES += include/rpc/rpcb_prot.h
GEN_FILES += commands/sbin/route/keywords.h
# lib/libc/net
GEN_FILES += lib/libc/net/nslexer.c
GEN_FILES += lib/libc/net/nsparser.c
CLEAN_FILES = lib/libc/net/nsparser.i
CLEAN_FILES += lib/libc/net/y.tab.h

# lib/libipsec
GEN_FILES += lib/libipsec/policy_token.c
GEN_FILES += lib/libipsec/policy_parse.c
CLEAN_FILES += lib/libipsec/policy_parse.i
CLEAN_FILES += lib/libipsec/y.tab.h

all: $(LIB) 

$(LIB): $(GEN_FILES) $(C_O_FILES) $(COMMAND_RELS)
	$(AR) rcu $@ $^

$(IFCONFIG): $(IFCONFIG_C_O_FILES)
	$(LD) -r -o $@ $^

$(NETSTAT): $(NETSTAT_C_O_FILES)
	$(LD) -r -o $@ $^

rtems/rtems-kvm-symbols.c: rtems/generate_kvm_symbols
	./rtems/generate_kvm_symbols >rtems/rtems-kvm-symbols.c

include/rpc/rpcb_prot.h: include/rpc/rpcb_prot.x
	rm -f include/rpc/rpcb_prot.h
	rpcgen -h -o include/rpc/rpcb_prot.h include/rpc/rpcb_prot.x

commands/sbin/route/keywords.h: commands/sbin/route/keywords
	sed -e '/^#/d' -e '/^$$/d' commands/sbin/route//keywords > _keywords.tmp
	LC_ALL=C tr 'a-z' 'A-Z' < _keywords.tmp | paste _keywords.tmp - | \
	    awk '{ \
		if (NF > 1) \
			printf "#define\tK_%s\t%d\n\t{\"%s\", K_%s},\n", \
			    $$2, NR, $$1, $$2 }' \
	    > commands/sbin/route/keywords.h
	rm -f _keywords.tmp

# lib/libc/net Yacc and lex files
lib/libc/net/nslexer.c: lib/libc/net/nslexer.l
	make -C lib/libc/net nslexer.c

lib/libc/net/nsparser.c: lib/libc/net/nsparser.y
	make -C lib/libc/net nsparser.c

# libipsec Yacc and lex files
lib/libipsec/policy_token.c: lib/libipsec/policy_token.l
	make -C lib/libipsec policy_token.c

lib/libipsec/policy_parse.c: lib/libipsec/policy_parse.y
	make -C lib/libipsec policy_parse.c

install: $(LIB)
	install -d $(INSTALL_BASE)/include
	cd include; for i in `find . -name '*.h'` ; do \
	  install -c -m 644 -D "$$i" "$(INSTALL_BASE)/include/$$i" ; done
	cd rtems/include; for i in `find . -name '*.h'` ; do \
	  install -c -m 644 -D "$$i" "$(INSTALL_BASE)/include/$$i" ; done
	cd local; for i in `find . -name '*.h'` ; do \
	  install -c -m 644 -D "$$i" "$(INSTALL_BASE)/include/$$i" ; done
	cd sys; for i in `find . -name '*.h'` ; do \
	  install -c -m 644 -D "$$i" "$(INSTALL_BASE)/include/$$i" ; done
	install -c -m 644 $(LIB) $(INSTALL_BASE)

clean:
	rm -f $(LIB) $(GEN_FILES) $(CLEAN_FILES)
	rm -f $(C_O_FILES) $(IFCONFIG_C_O_FILES) $(NETSTAT_C_O_FILES)
	rm -f $(C_D_FILES) $(IFCONFIG_C_D_FILES) $(NETSTAT_C_D_FILES)

-include $(C_D_FILES)

doc: 

