-:setup install
setup:
	git clone https://github.com/asdf-vm/asdf.git $(HOME)/.asdf --branch v0.13.1 || ls $(HOME)/.asdf && cd $(HOME)/.asdf && git reset --hard && git pull -f origin v0.13.1:v0.13.1 && git checkout v0.13.1
.ONESHELL:install
install:
	. "$(HOME)/.asdf/asdf.sh" && . "$(HOME)/.asdf/completions/asdf.bash" && exec bash
