# Maintainer: Arch Haskell Team <arch-haskell@haskell.org>
_hkgname=detrospector
pkgname=detrospector
pkgver=0.1
pkgrel=2
pkgdesc="Markov chain text generator"
url="http://hackage.haskell.org/package/${_hkgname}"
license=('custom:BSD3')
arch=('i686' 'x86_64')
makedepends=('ghc' 'haskell-binary>=0.5' 'haskell-bytestring=0.9.1.7' 'haskell-cmdargs>=0.6' 'haskell-containers=0.3.0.0' 'haskell-hashable>=1.0' 'haskell-hashmap>=1.1' 'haskell-mwc-random>=0.8' 'haskell-text>=0.8' 'haskell-zlib=0.5.2.0')
depends=('gmp')
options=('strip')
source=(http://hackage.haskell.org/packages/archive/${_hkgname}/${pkgver}/${_hkgname}-${pkgver}.tar.gz)
build() {
    cd ${srcdir}/${_hkgname}-${pkgver}
    runhaskell Setup configure --prefix=/usr --docdir=/usr/share/doc/${pkgname} -O
    runhaskell Setup build
}
package() {
    cd ${srcdir}/${_hkgname}-${pkgver}
    runhaskell Setup copy --destdir=${pkgdir}
    install -D -m644 LICENSE ${pkgdir}/usr/share/licenses/${pkgname}/LICENSE
    rm -f ${pkgdir}/usr/share/doc/${pkgname}/LICENSE
}
md5sums=('a97d85224b6bb47b55aea30ef736b1b6')
