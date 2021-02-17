pkgname=gorgzorg
pkgver=0.2.0
pkgrel=1
pkgdesc="A simple CLI network file transfer tool"
arch=('x86_64')
url="https://github.com/aarnt/gorgzorg"
license=('GPLv2')
makedepends=('qt5-tools' 'cmake')
source=("https://github.com/aarnt/${pkgname}/archive/v${pkgver}.tar.gz")
md5sums=('39707e3a59304a95d1cfb376fb354301')

build() {
	cd "${pkgname}-${pkgver}"
	cmake -G "Unix Makefiles" -DCMAKE_BUILD_TYPE=Release -DCMAKE_INSTALL_PREFIX=/usr
	make
}

package() {
 cd "${pkgname}-${pkgver}"
 install -Dm755 ${pkgname} "${pkgdir}/usr/bin/${pkgname}"
 install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
