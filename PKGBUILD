# Maintainer: Sander Boom <sanderboom@gmail.com>
# Contributor: jarosz

pkgname=php-codesniffer
_pkgname=PHP_CodeSniffer
pkgver=3.10.2
pkgrel=1
pkgdesc="PHP_CodeSniffer tokenizes PHP, JavaScript and CSS files to detect and fix violations of a defined set of coding standards."
arch=('any')
url="https://github.com/PHPCSStandards/PHP_CodeSniffer"
license=('BSD')
depends=('php')
source=("phpcs-${pkgver}.phar::https://github.com/PHPCSStandards/${_pkgname}/releases/download/${pkgver}/phpcs.phar"
        "phpcs-${pkgver}.phar.asc::https://github.com/PHPCSStandards/${_pkgname}/releases/download/${pkgver}/phpcs.phar.asc"
        "phpcbf-${pkgver}.phar::https://github.com/PHPCSStandards/${_pkgname}/releases/download/${pkgver}/phpcbf.phar"
        "phpcbf-${pkgver}.phar.asc::https://github.com/PHPCSStandards/${_pkgname}/releases/download/${pkgver}/phpcbf.phar.asc"
        "licence-${pkgver}.txt::https://raw.githubusercontent.com/PHPCSStandards/${_pkgname}/${pkgver}/licence.txt")
validpgpkeys=('689DAD778FF08760E046228BA978220305CD5C32')
sha256sums=('5f580b08328af20a4138a6dcefdbb4c3307e133d9dfbabdf925c08c7d87f18de'
            'SKIP'
            '7b4b1316ce388600c2a052b41b9badd2d906827f0a08a08873ca5d1063dd1038'
            'SKIP'
            '577aa0eb3360e7b45fe436138c40d49f952e6d496987406981b6f1eee69b26e9')

package() {
  install -Dm0755 "${srcdir}/phpcs-${pkgver}.phar" "${pkgdir}/usr/bin/phpcs"
  install -Dm0755 "${srcdir}/phpcbf-${pkgver}.phar" "${pkgdir}/usr/bin/phpcbf"

  install -d "${pkgdir}/usr/share/licenses"
  install -D -m 644 "${srcdir}/licence-${pkgver}.txt" "${pkgdir}/usr/share/licenses/${pkgname}/licence.txt"
}
