pkgname=faba-icons
_pkgname=faba-icon-theme
pkgver=1.0.0
pkgrel=1
pkgdesc="This is the base icon set for Faba. It is designed with simplicity and compliance to Tango desktop standards in mind. "
arch=('any')
url="https://github.com/snwh/faba-icon-theme"
license=('GPL3')
depends=()
makedepends=('git')
optdepends=()
provides=('faba-icons')
conflicts=('faba-icons')
source=('git+https://github.com/snwh/faba-icon-theme.git')
md5sums=('SKIP')

pkgver() {
  cd $srcdir/$_pkgname
  echo $(git rev-list --count HEAD).$(git rev-parse --short HEAD)
}

package() {

  # create theme dirs
  install -d -m 755 "$pkgdir"/usr/share/icons/Faba

  # install theme
  cd $srcdir/faba-icon-theme/Faba
  cp -r . "$pkgdir"/usr/share/icons/Faba/
}
