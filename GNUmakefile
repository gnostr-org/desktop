V=1
export V
.ONESHELL:
-:setup install
setup:
	git clone --tags v0.13.1 --single-branch \
		https://github.com/asdf-vm/asdf.git $(HOME)/.asdf 2>/tmp/gnostr-deskop.log || \
		cd $(HOME)/.asdf && git reset --hard && git pull -f origin --tag v0.13.1 && git checkout v0.13.1
plugin:
	$(shell which asdf) plugin add nodejs https://github.com/asdf-vm/asdf-nodejs.git
install:plugin install-yarn
	. $(HOME)/.asdf/asdf.sh && . $(HOME)/.asdf/completions/asdf.bash
install-yarn:install
## rm -f node_modules/@eslint/eslintrc/node_modules/ignore/LICENSE-MIT
## yarn upgrade -f  @types
	. $(HOME)/.nvm/nvm.sh && \
		nvm exec $(shell which yarn) install -f || \
		$(MAKE) install-pnpm || $(MAKE) install-npm
install-pnpm:install
	. $(HOME)/.nvm/nvm.sh && \
		nvm exec $(shell which pnpm) install -f
install-npm:install
	. $(HOME)/.nvm/nvm.sh && \
		nvm exec $(shell which npm) install -f
