# Maintainer: Voobscout <voobscout+aur@gmail.com>
pkgname=xorg-xfs-fslsfonts
pkgver=1.0.5
pkgrel=1
pkgdesc="X Font Server - list fonts"
arch=('i686' 'x86_64')
license=('GPL2')
makedepends=('git' 'pkg-config' 'autoconf' 'automake' 'gettext' 'xproto' 'xtrans' 'wget')
depends=('libfs')
url="http://xorg.freedesktop.org/archive/individual/app"
provides=('xorg-xfs-fslsfonts')
optdepends=('xorg-xfs' 'xorg-xfstt')
source=("http://xorg.freedesktop.org/archive/individual/app/fslsfonts-$pkgver.tar.gz")
sha256sums=('27e58d2313835ce0f08cf47c59a43798b122f605a55f54b170db27b57a492007')
options=(!strip)

build() {
  cd ${srcdir}/fslsfonts-${pkgver}
  msg "Configuring fslsfonts..."
  ./configure --prefix=/usr
  msg "Compiling fslsfonts... "
  make
}

package() {
  msg "Installing fslsfonts"
  cd ${srcdir}/fslsfonts-${pkgver}
  make DESTDIR=${pkgdir} install
}

# vim:set ts=2 sw=2 et:
