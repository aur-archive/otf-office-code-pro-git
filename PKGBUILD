# Maintainer: Sial <NAME at cpan dot org>

_gitname='Office-Code-Pro'
pkgname='otf-office-code-pro-git'
pkgver=1.004
pkgrel=2
pkgdesc='Pre-patched and adjusted version for usage with the new Powerline plugin'
arch=('any')
url="https://github.com/nathco/${_gitname}/tree/master/Fonts/OTF"
license=('custom:OFL')
depends=('fontconfig' 'xorg-font-utils')
makedepends=('git')
install=${pkgname}.install
source=("git+https://github.com/nathco/${_gitname}")
md5sums=('SKIP')

pkgver() {
	cd "${srcdir}/${_gitname}"
 cat README.md | grep '^\*\*Version' | head -1 | sed -n 's/^.* \(.*[0-9]\).*$/\1/p'
}

package() {
	cd "${srcdir}/${_gitname}/Fonts/Office Code Pro/OTF"
	install -d "${pkgdir}/usr/share/fonts/OTF"
	install -m644 *.otf "${pkgdir}/usr/share/fonts/OTF/"

    cd "${srcdir}/${_gitname}/Fonts/Office Code Pro D/OTF"
    install -d "${pkgdir}/usr/share/fonts/OTF"
    install -m644 *.otf "${pkgdir}/usr/share/fonts/OTF/"

    cd "${srcdir}/${_gitname}"
    install -Dm644 ./LICENSE.txt "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE.txt"
}
