# Contributor: Arch Haskell Team <arch-haskell@haskell.org>
# Package generated by cabal2arch 0.3.4
pkgname=haskell-data-trie-general
pkgrel=1
pkgver=0.4
pkgdesc="An experiment with generalised tries."
url="http://hackage.haskell.org/cgi-bin/hackage-scripts/package/Data-Trie-General"
license=('custom:BSD3')
arch=('i686' 'x86_64')
makedepends=('ghc')
source=(http://hackage.haskell.org/packages/archive/Data-Trie-General/0.4/Data-Trie-General-0.4.tar.gz)
install=haskell-data-trie-general.install
md5sums=('a75c1339f8a93f8b6119e8149092cad7')
build() {
    cd $startdir/src/Data-Trie-General-0.4
    runhaskell Setup configure --prefix=/usr || return 1
    runhaskell Setup build                   || return 1
    runhaskell Setup register   --gen-script || return 1
    runhaskell Setup unregister --gen-script || return 1
    install -D -m744 register.sh   $startdir/pkg/usr/share/haskell/$pkgname/register.sh
    install    -m744 unregister.sh $startdir/pkg/usr/share/haskell/$pkgname/unregister.sh
    runhaskell Setup copy --destdir=$startdir/pkg || return 1
    install -D -m644 LICENSE $startdir/pkg/usr/share/licenses/$pkgname/LICENSE || return 1
}
