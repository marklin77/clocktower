PKG         = file_crate
PKG_EXCLUDE = --exclude=.gitignore 
TAR_EXCLUDE = --exclude-vcs-ignores \
              --exclude-backups
root        = .

dir:
	mkdir -p $(root)/model $(root)/verif $(root)/rtl $(root)/common
	mkdir -p $(root)/verif/bench $(root)/verif/scripts
	touch README.md 
	touch model/README.md 
	touch verif/READEME.md 
	touch verif/bench/README.md 
	touch verif/scripts/README.md 
	touch rtl/README.md 
	touch common/README.md


tar:
	git ls-files | xargs tar $(TAR_EXCLUDE) $(PKG_EXCLUDE) -czvf $(PKG).tar.gz

zip:
	git ls-files | xargs zip $(PKG_EXCLUDE) $(PKG).zip
clean:
	git ls-files -o --directory | xargs rm -rf 
