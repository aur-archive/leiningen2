# Maintainer: pisuka <tekmon@gmail.com>
pkgname=leiningen2
pkgver=2.0.0preview3
pkgrel=1
pkgdesc="Leiningen is for automating Clojure projects without setting your hair on fire."
arch=(any)
url="https://github.com/technomancy/leiningen"
license=(EPL)
groups=()
depends=(java-environment)
makedepends=()
optdepends=()
provides=()
conflicts=(leiningen2-git)
replaces=()
backup=()
options=()
install=
source=(https://raw.github.com/technomancy/leiningen/2.0.0-preview3/bin/lein
		https://raw.github.com/technomancy/leiningen/2.0.0-preview3/bash_completion.bash)
md5sums=(64773622efddf8d60349dc7d552c4cd3 ec205c6f4ee2d4890365ec5f4dfafdea)

package() {
	mkdir -p "${pkgdir}"/usr/bin/ "${pkgdir}"/usr/share/bash-completion/completions/
	install -m 755 -D "${srcdir}"/lein "${pkgdir}"/usr/bin/lein2
	install -D "${srcdir}"/bash_completion.bash "${pkgdir}"/usr/share/bash-completion/completions/lein2
	sed -i 's/lein/lein2/g' "${pkgdir}"/usr/share/bash-completion/completions/lein2
}

# vim:set ts=2 sw=2 et:
