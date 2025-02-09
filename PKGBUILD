# Maintainer: Sander Boom <sanderboom@gmail.com>
# Contributor: jarosz

pkgname=php-codesniffer
_pkgname=PHP_CodeSniffer
pkgver=3.11.3
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
sha256sums=('f043b299b6f3aa1a8b78cb47848cee28cdc524f31ceff6b24ff70eaf8bf39936'
            'SKIP'
            'a5c9a212e771b5f5f82e8213467ad35674e8a25cbf84ae88b6b8dd659a749f7c'
            'SKIP'
            '577aa0eb3360e7b45fe436138c40d49f952e6d496987406981b6f1eee69b26e9')

package() {
  install -Dm0755 "${srcdir}/phpcs-${pkgver}.phar" "${pkgdir}/usr/bin/phpcs"
  install -Dm0755 "${srcdir}/phpcbf-${pkgver}.phar" "${pkgdir}/usr/bin/phpcbf"

  install -d "${pkgdir}/usr/share/licenses"
  install -D -m 644 "${srcdir}/licence-${pkgver}.txt" "${pkgdir}/usr/share/licenses/${pkgname}/licence.txt"
}
