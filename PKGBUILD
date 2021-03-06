pkgname=gorgzorg
pkgver=0.3.0
pkgrel=1
pkgdesc="A simple CLI network file transfer tool"
arch=('x86_64')
url="https://github.com/aarnt/gorgzorg"
license=('GPLv2')
makedepends=('qt6-tools' 'qt6-base')
source=("https://github.com/aarnt/${pkgname}/archive/v${pkgver}.tar.gz")
md5sums=('4a91f462a2220e923fe630862e276e5b')

build() {
	cd "${pkgname}-${pkgver}"
	qmake-qt6
	make
}

package() {
	cd "${pkgname}-${pkgver}"
	install -Dm755 ${pkgname} "${pkgdir}/usr/bin/${pkgname}"
	install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
