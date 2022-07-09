# Maintainer: iyamnabeen <iym.nabeen@gmail.com>
pkgname=metis-base
_destname1="/etc"
_destname2="/usr"
_licensedir="/usr/share/metis/licenses/"
pkgver=1.0
pkgrel=0
pkgdesc="base Configuration files for @metis-os"
arch=('x86_64')
url="https://github.com/metis-os/$pkgname"
license=('GPL-3.0')
makedepends=('git')
conflicts=("metis-base")
backup=('etc/pacman.d/gnupg/gpg.conf' 'etc/X11/xorg.conf.d/30-touchpad.conf')
provides=("${pkgname}")
options=( !strip !emptydirs )
source=(${pkgname}::"git+https://github.com/metis-os/${pkgname}")
sha256sums=('SKIP')

package() {
  install -dm755 "$pkgdir/$_licensedir/$pkgname"
  install -m644 "$srcdir/$pkgname/LICENSE" "$pkgdir/$_licensedir/$pkgname"

  install -dm755 "$pkgdir/$_destname1"
  cp -r ${srcdir}/${pkgname}/${_destname1} ${pkgdir}

  install -dm755 "$pkgdir$_destname2"
  cp -r ${srcdir}/${pkgname}/${_destname2} ${pkgdir}
}
