EXTRA_DIST = \
		requirements.txt \
		dev-requirements.txt \
		AlexaPi.service.in

# alexapi, alexaauth executable as python script

dist_bin_SCRIPTS = AlexaPi AlexaAuth AlexaCustomSkill gpio

servicedir = ${libdir}/systemd/system

service_DATA = AlexaPi.service AlexaCustomSkill.service

# rules for generating files after evaluating automake variables

edit = 	sed \
	-e 's|@bindir[@]|$(bindir)|g' \
	-e 's|@datadir[@]|$(datadir)|g' \
	-e 's|@pkgdatadir[@]|$(pkgdatadir)|g' \
	-e 's|@libdir[@]|$(libdir)|g' \
	-e 's|@libexecdir[@]|$(libexecdir)|g' \
	-e 's|@localstatedir[@]|$(localstatedir)|g' \
	-e 's|@prefix[@]|$(prefix)|g' \
	-e 's|@rundir[@]|$(localstatedir)/run|g' \
	-e 's|@sbindir[@]|$(sbindir)|g' \
	-e 's|@sharedstatedir[@]|$(sharedstatedir)|g' \
	-e 's|@sysconfdir[@]|$(sysconfdir)|g'


AlexaPi.service AlexaCustomSkill.service AlexaPi : Makefile
	rm -f $@ $@.tmp
	$(edit) '$(srcdir)/$@.in' >$@.tmp
	mv $@.tmp $@

# configuration file

pkgsysconfdir = ${sysconfdir}/AlexaPi

pkgsysconf_DATA = config.yaml
