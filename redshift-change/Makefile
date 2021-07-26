PREFIX ?= /usr/local
install:
	cp redshift-change $(DESTDIR)$(PREFIX)/bin/
	echo 25000 > $${HOME}/.local/redshift-temp
	echo 0 >> $${HOME}/.local/redshift-temp
	sed -i "1s/^/sed -i '\$s\/1\/0\/' .local\/redshift-temp\n/" $${HOME}/.xinitrc
uninstall:
	rm $(DESTDIR)$(PREFIX)/bin/redshift-change
	rm $${HOME}/.local/redshift-temp
	sed -i "/sed -i '\$s\/1\/0\/' .local\/redshift-temp/d" $${HOME}/.xinitrc
