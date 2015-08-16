# Maintainer: Kristian Ronnberg <kristian DOT ronnberg AT gmail DOT com>
# Contributor: Kevin Peters <65bones AT gmail DOT com>
# Contributor: Ali H. Caliskan <ali.h.caliskan AT gmail DOT com>

pkgname=jstock
pkgver=1.0.7.6
pkgrel=1
pkgdesc="A stock market software that helps you make smart investment decision"
arch=('any')
url="http://jstock.org/"
license=('GPL2')
depends=('jre7-openjdk')
source=("https://github.com/yccheok/jstock/releases/download/release_1-0-7-6/jstock-1.0.7.6-bin.zip"
        "${pkgname}.desktop"
        "${pkgname}.png"
        "${pkgname}.sh")
md5sums=('37d3b57a3eb8450ce6dba6e82a26d43c'
         '7a68e77a1dccdd89db242d799c9f2d8e'
         'c2483790417a4ca80b7a65006f696679'
         'c025a2cf0c187bb4b5fbb5114f15ac4a')

package() {
  cd "${srcdir}/${pkgname}"

  # Install program files
  mkdir -p "${pkgdir}/usr/share/${pkgname}"
  cp -r * "${pkgdir}/usr/share/${pkgname}"

  # Install a launcher
  install -Dm755 ../${pkgname}.sh "${pkgdir}/usr/bin/${pkgname}"

  # Install a desktop entry
  install -Dm644 ../${pkgname}.png "${pkgdir}/usr/share/pixmaps/${pkgname}.png"
  install -Dm644 ../${pkgname}.desktop "${pkgdir}/usr/share/applications/${pkgname}.desktop"
}
