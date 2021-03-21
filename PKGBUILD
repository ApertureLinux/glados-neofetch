# Maintainer: Zach Osman <zosman@aperturelinux.org>


pkgname=aperture-neofetch
pkgver=7.1.0
pkgrel=2
pkgdesc="A CLI system information tool written in BASH that supports displaying images."
arch=('any')
url="https://github.com/dylanaraps/neofetch"
license=('MIT')
depends=('bash')
makedepends=('git')
conflicts=('neofetch')
provides=('neofetch')
backup=('etc/neofetch/config.conf')
optdepends=(
  'catimg: Display Images'
  'chafa: Image to text support'
  'feh: Wallpaper Display'
  'imagemagick: Image cropping / Thumbnail creation / Take a screenshot'
  'jp2a: Display Images'
  'libcaca: Display Images'
  'nitrogen: Wallpaper Display'
  'w3m: Display Images'
  'xdotool: See https://github.com/dylanaraps/neofetch/wiki/Images-in-the-terminal'
  'xorg-xdpyinfo: Resolution detection (Single Monitor)'
  'xorg-xprop: Desktop Environment and Window Manager'
  'xorg-xrandr: Resolution detection (Multi Monitor + Refresh rates)'
  'xorg-xwininfo: See https://github.com/dylanaraps/neofetch/wiki/Images-in-the-terminal'
)
_commit="60d07dee6b76769d8c487a40639fb7b5a1a7bc85"
source=("git+https://github.com/ApertureLinux/aperture-neofetch#commit=${_commit}")
md5sums=('SKIP')

package() {
  cd "${pkgname}"
  make DESTDIR="$pkgdir" install
  install -Dm644 LICENSE.md "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE.md"
}