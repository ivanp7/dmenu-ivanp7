# Maintainer:  ivanp7
# Contributor: ivanp7

_pkgname=dmenu
pkgname=$_pkgname-ivanp7
pkgver=5.2
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
md5sums=('5bfb899b5a872212c492c4f110e9a119'
         'a628f7b33f8940d72ce14b8878d27b8d'
         '6a540451c962cf927c7062f0c9f7c0fc'
         '4b0f2702c67346247b253788abb19804'
         '37798461a788d9a28bf9087728c7c8b3'
         '95ce4577f2a6640db4ee22520f83a69b'
         '877996fb91600d9e307b1412c1a399f4'
         '316c001c977900ec104f2b1249dd1573'
         '352d9dafdcbee8ef4fa8265c4fb681c7'
         'e1c893def7d16c74c65692c5e3c62fc3'
         'ece1a69b52a7dc80af511306582e6eb5'
         '6d01e0cf823733696028e5f33b9fe593'
         '5833554449b3bf384172191218074274'
         '962655608098fe6ac52cc796e7c42fd0'
         '007c065ca60e3f3c56bf153f2f769a90')

build(){
  make PREFIX=/usr DESTDIR="$pkgdir"
}

package() {
  make PREFIX=/usr DESTDIR="$pkgdir" install
  install -Dm644 LICENSE "$pkgdir"/usr/share/licenses/$pkgname/LICENSE
}

