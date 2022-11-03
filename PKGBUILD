# Maintainer:  ivanp7
# Contributor: ivanp7

_pkgname=dmenu
pkgname=$_pkgname-ivanp7
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
md5sums=('5bfb899b5a872212c492c4f110e9a119'
         '077fa7408776ef1649d28c3251d77315'
         '5f8167b2aaeafa02104815509803c8a0'
         '10bbecbb14be4a69148f1c3a946af17d'
         'cf6a7692fb9b8a2bda4373dc80844921'
         '95ce4577f2a6640db4ee22520f83a69b'
         '02767b3eda4ab44b52e190ec3e01fec6'
         '952dc86e34617de02ddde41a2f256de0'
         'db0fc5f7f2a21e5cec73349ebdaa954a'
         '3430d46fc42f3a732b887537239531df'
         'ece1a69b52a7dc80af511306582e6eb5'
         '6d01e0cf823733696028e5f33b9fe593'
         '8942094f1a2f79c8fbcb6fd473b3f3c0'
         'e1d877b57636568ba579b1bc0ae42e8f'
         '007c065ca60e3f3c56bf153f2f769a90')

build(){
  make PREFIX=/usr DESTDIR="$pkgdir"
}

package() {
  make PREFIX=/usr DESTDIR="$pkgdir" install
  install -Dm644 LICENSE "$pkgdir"/usr/share/licenses/$pkgname/LICENSE
}

