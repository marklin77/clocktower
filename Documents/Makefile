PKG         = file_crate
PKG_EXCLUDE = --exclude=Makefile \
              --exclude=.gitignore 
TAR_EXCLUDE = --exclude-vcs-ignores \
              --exclude-backups
root        = .

dir:
	mkdir -p $(root)/model $(root)/verif $(root)/rtl $(root)/common

tar:
	git ls-files | xargs tar $(TAR_EXCLUDE) $(PKG_EXCLUDE) -czvf $(PKG).tar.gz

zip:
	git ls-files | xargs zip $(PKG_EXCLUDE) $(PKG).zip
clean:
	git ls-files -o --directory | xargs rm -rf 
