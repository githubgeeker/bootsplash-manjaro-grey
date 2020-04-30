pkgbase=bootsplash-themes
pkgname=('bootsplash-theme-manjaro-grey')
pkgver=1
pkgrel=1
url="https://lists.freedesktop.org/archives/dri-devel/2017-December/160242.html"
arch=('x86_64')
license=('GPL')

depends=()
builddepends=('imagemagick')
options=('!libtool' '!emptydirs')

source=('bootsplash-packer'
	'bootsplash-manjaro-grey.sh'
	'bootsplash-manjaro-grey.initcpio_install'
	'spinner.gif'
	'logo.png')

sha256sums=('SKIP'
            'SKIP'
            'SKIP'
            'SKIP'
            'SKIP')

build() {
  cd "$srcdir"
  sh ./bootsplash-manjaro-grey.sh
}

package_bootsplash-theme-manjaro-grey() {
  pkgdesc="Bootsplash Theme with Grey"
  cd "$srcdir"

  install -Dm644 "$srcdir/bootsplash-manjaro-grey" "$pkgdir/usr/lib/firmware/bootsplash-themes/manjaro-grey/bootsplash"
  install -Dm644 "$srcdir/bootsplash-manjaro-grey.initcpio_install" "$pkgdir/usr/lib/initcpio/install/bootsplash-manjaro-grey"
} 
