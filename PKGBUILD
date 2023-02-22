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
provides=($_pkgname)
conflicts=($_pkgname)
source=('arg.h' 'config.h' 'config.mk' 'dmenu.1' 'dmenu.c'
    'dmenu_path' 'dmenu_run' 'drw.c' 'drw.h' 'LICENSE'
    'Makefile' 'stest.1' 'stest.c' 'util.c' 'util.h')
sha256sums=('9ed2b2e3396fdebc8ecab2cdbb09db115cca015f63ec0443b8ccc56340b6b03c'
            '16220492633c462256209cd71fbfbfbe22ca9dfe91eaffa4fde98b60af2c08ca'
            'e4af309d9cb5dbf947ffe09b33ffe01b68da24a1a158aefb857c88f89e7aed45'
            'e915c98bf9de44149cc8a50b64461da2a6a587a25251c2cd27f030ae1eab3553'
            '6d2509bdf3a08853ac5faaaa7766e92136e280fda61656d8112b802e71185502'
            'a3f19e648e20eb80532dfe87e9bd9feeaa92df838e6ecc061f274c9da579d617'
            'cd20492b57189ecc3353e7b46748ed931e02f0b5ceb7b867b22a69a29e9d0f0c'
            '8c9f81b98f447440cf59dd3eefda99eec4e7733266ad0c072612163ccff4e1df'
            '7ed1cf72bfcb0f5444f338293aef74c455ce4ed5463f171a48358f64d7835d49'
            '9f8e922fcfc18ffcc4975dd0b1bee38302bd4e0c538251dfef6d77cd7ed59c89'
            '77d5b98576b4b3aa788699c6528e76c45ded168b7c1dc10f8543906c6e2179b6'
            '00d3389ef8858a565cf3fb3445620b90eb67d1a9b31434f4d54b05ed6c5abefb'
            'ba76404e61abbd734e315999ffe4e883419c4c69ff17a5d4d88a5cd11dd4b055'
            '1c093b9969daaf3e1a001b924c6c2da3770993916b444dfe65fe39aa0090aa1a'
            '1196a7b6efbf4cb3f5c435fffd72e7647f977483845d5c78c1c48d9ab8b96819')

build() {
  make PREFIX=/usr DESTDIR="$pkgdir"
}

package() {
  make PREFIX=/usr DESTDIR="$pkgdir" install
  install -Dm644 LICENSE "$pkgdir"/usr/share/licenses/$pkgname/LICENSE
}

