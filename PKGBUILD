pkgname=pacaur
pkgver=0.9.6
pkgrel=1
pkgdesc="A simple cower wrapper to fetch PKGBUILDS from aur & abs"
arch=('any')
url="https://github.com/Spyhawk/pacaur"
license=('GPL')
depends=('cower' 'sudo')
optdepends=('pacman-color: matches output if color is used')
backup=('etc/pacaur.conf')
source=($pkgname $pkgname.conf)
md5sums=('66f974333c01940396aaf03150a80874'
         'cf83d1c7e6a9be698217282645feff24')
build() {
  mkdir -p "$pkgdir/etc/"
  install -D -m644 ./$pkgname.conf $pkgdir/etc/$pkgname.conf || return 1
  install -D -m755 ./$pkgname $pkgdir/usr/bin/$pkgname || return 1
}
