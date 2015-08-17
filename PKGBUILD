# Archtrack maintainer: Evan Teitelman <teitelmanevan at gmail dot com>
# Maintainer: Evan Teitelman <teitelmanevan at gmail dot com>
# Contributor: Michael P <ptchinster@archlinux.us>

pkgname='rifiuti'
pkgver=20040505_1
pkgrel=2
groups=(archtrack archtrack-forensics)
pkgdesc='Examine the contents of the INFO2 file from a MS Recycle Bin file (forensic purposes).'
arch=('i686' 'x86_64')
url="http://www.jonesdykstra.com/"
license=('GPL')
source=("http://sourceforge.net/projects/fast/files/Rifiuti/Rifiuti%20v${pkgver}/${pkgname}_${pkgver}.tar.gz/download"
         "includes.patch")
md5sums=('c39d6e560ff96136f80dfb73fc4390db'
         'SKIP')

prepare() {
	cd "$srcdir/${pkgname}_${pkgver}/src"
	patch -N < $srcdir/includes.patch
}

build() {
	cd "$srcdir/${pkgname}_${pkgver}/src"
	make install
	install -dm755 $pkgdir/usr/bin
	mv -v ../bin $pkgdir/usr
}
