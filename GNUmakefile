-:setup install plugin
setup:
##            --tags v0.13.1 --single-branch
	git clone --tags v0.13.1 --single-branch \
		https://github.com/asdf-vm/asdf.git $(HOME)/.asdf 2>/tmp/gnostr-deskop.log || ls $(HOME)/.asdf && cd $(HOME)/.asdf && git reset --hard && git pull -f origin --tag v0.13.1 && git checkout v0.13.1
.ONESHELL:install
install:
	. "$(HOME)/.asdf/asdf.sh" && . "$(HOME)/.asdf/completions/asdf.bash" && exec bash
plugin:
	$(shell which asdf) plugin add nodejs https://github.com/asdf-vm/asdf-nodejs.git && exec bash
