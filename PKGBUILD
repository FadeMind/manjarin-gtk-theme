# Maintainer: FadeMind <fademind@gmail.com>

 _commit=6956711e670cc563adba3b00abe1d33bbdcfdaa7
pkgname=manjarin-gtk-theme
pkgver=20180429
pkgrel=2
pkgdesc='Manjarin is a GTK-theme developed for the Manjaro-Gnome Edition'
arch=('any')
url='https://github.com/FadeMind/manjarin-gtk-theme'
license=('GPL')
depends=('gtk2' 'gtk3' 'gtk-engine-murrine' 'gtk-engines')
optdepends=('adapta-maia-theme: for adapta-nokto-maia shell theme'
			'papirus-maia-icon-theme: default icons theme for this theme') 
makedepends=('cmake')
source=("${pkgname}.zip::${url}/archive/${_commit}.zip")
sha256sums=('3f1478d4c7872164534b165559b04ccb4a7f3add9a8f1acd4096d695b411373a')

pkgver() {
	date +%Y%m%d
}

build() {
    mv ${srcdir}/${pkgname}-${_commit} ${srcdir}/${pkgname}
    mkdir -p ${srcdir}/build
    cd ${srcdir}/build
    cmake ../${pkgname}
    make
}

package() {
    make -C build DESTDIR="${pkgdir}" install
}
