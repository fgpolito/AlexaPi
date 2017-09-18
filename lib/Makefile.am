ALEXAPI_SRCS =	capture.py \
		config.py \
		constants.py \
		exceptions.py \
		__init__.py \
		tunein.py

EXTRA_DIST = config.py.in

alexapidir = $(pythondir)/alexapi
alexapi_PYTHON = ${ALEXAPI_SRCS};

SUBDIRS = device_platforms playback_handlers triggers

edit = 	sed \
	-e 's|@bindir[@]|$(bindir)|g' \
	-e 's|@datadir[@]|$(datadir)|g' \
	-e 's|@libdir[@]|$(libdir)|g' \
	-e 's|@libexecdir[@]|$(libexecdir)|g' \
	-e 's|@localstatedir[@]|$(localstatedir)|g' \
	-e 's|@prefix[@]|$(prefix)|g' \
	-e 's|@rundir[@]|$(localstatedir)/run|g' \
	-e 's|@sbindir[@]|$(sbindir)|g' \
	-e 's|@sharedstatedir[@]|$(sharedstatedir)|g' \
	-e 's|@sysconfdir[@]|$(sysconfdir)|g'


config.py : Makefile
	rm -f $@ $@.tmp
	$(edit) '$(srcdir)/$@.in' >$@.tmp
	mv $@.tmp $@
