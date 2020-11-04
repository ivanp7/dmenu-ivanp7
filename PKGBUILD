# Maintainer:  ivanp7
# Contributor: ivanp7

_pkgname=dmenu
pkgname=$_pkgname-git
pkgver=5.0
pkgrel=1
pkgdesc="A generic menu for X"
url="http://tools.suckless.org/dmenu/"
arch=('i686' 'x86_64')
license=('MIT')
depends=('sh' 'libxinerama' 'libxft')
makedepends=('git')
provides=($_pkgname)
conflicts=($_pkgname)
source=('arg.h' 'config.h' 'config.mk' 'dmenu.1' 'dmenu.c'
    'dmenu_path' 'dmenu_run' 'drw.c' 'drw.h' 'LICENSE'
    'Makefile' 'stest.1' 'stest.c' 'util.c' 'util.h')
md5sums=('5bfb899b5a872212c492c4f110e9a119' 'SKIP'
    '9f65b5d073c1aa9c28ef69be0a88b0dc' 'SKIP' 'SKIP'
    '95ce4577f2a6640db4ee22520f83a69b' '02767b3eda4ab44b52e190ec3e01fec6' 
    'SKIP' 'SKIP' '3430d46fc42f3a732b887537239531df' 'ece1a69b52a7dc80af511306582e6eb5' 
    'SKIP' 'SKIP' 'SKIP' 'SKIP')

build(){
  make PREFIX=/usr DESTDIR="$pkgdir"
}

package() {
  make PREFIX=/usr DESTDIR="$pkgdir" install
  install -Dm644 LICENSE "$pkgdir"/usr/share/licenses/$pkgname/LICENSE
}

