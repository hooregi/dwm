# Maintainer: Hooregi <hooregi@halo.fm>
pkgname=dwm-hooregi-git
pkgver=6.3.r1147.617788f
pkgrel=1
epoch=
pkgdesc="Hooregi's build of suckless' dynamic window manager (dwm)"
arch=(x86_64)
url="https://gitlab.com/Hooregi/dwm.git"
license=('MIT')
groups=()
depends=('libxft' 'libx11' 'libxinerama' 'freetype2')
makedepends=('git' 'make')
checkdepends=()
optdepends=('dwmblocks-hooregi-git' 'dmenu-hooregi-git' 'st-hooregi-git')
provides=('dwm')
conflicts=('dwm')
replaces=()
backup=()
options=()
source=("git+$url")
noextract=()
md5sums=('SKIP')
validpgpkeys=()

pkgver() {
	cd "${_pkgname}"
  printf "6.3.r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

build() {
	cd dwm
  make X11INC=/usr/include/X11 X11LIB=/usr/lib/X11 FREETYPEINC=/usr/include/freetype2
}

package() {
  cd dwm
  mkdir -p ${pkgdir}/opt/${pkgname}
  cp -rf * ${pkgdir}/opt/${pkgname}
  make PREFIX=/usr DESTDIR="${pkgdir}" install
  install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
  install -Dm644 README "${pkgdir}/usr/share/doc/${pkgname}/README"
  install -Dm644 "${srcdir}/dwm/dwm.desktop" "$pkgdir/usr/share/xsessions/dwm.desktop"
}
