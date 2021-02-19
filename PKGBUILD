pkgname=gorgzorg
_commit=23dd651
pkgver=0.3dev
pkgrel=1
pkgdesc="A simple CLI network file transfer tool"
arch=('x86_64')
url="https://github.com/aarnt/gorgzorg"
license=('GPLv2')
makedepends=('qt6-tools' 'qt6-base')
source=("https://github.com/aarnt/${pkgname}/tarball/main/${pkgname}-${pkgver}.tar.gz")
#source=("https://github.com/aarnt/${pkgname}/archive/v${pkgver}.tar.gz")
md5sums=('37cb6eda0cdd1aad4a1ab55fec7256c5')

build() {
	cd "aarnt-${pkgname}-${_commit}"
#	cd "${pkgname}-${pkgver}"
	#cmake -G "Unix Makefiles" -DCMAKE_BUILD_TYPE=Release -DCMAKE_INSTALL_PREFIX=/usr
	qmake-qt6
	make
}

package() {
	cd "aarnt-${pkgname}-${_commit}"
	#cd "${pkgname}-${pkgver}"
	install -Dm755 ${pkgname} "${pkgdir}/usr/bin/${pkgname}"
	install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
