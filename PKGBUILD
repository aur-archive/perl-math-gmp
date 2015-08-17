# Maintainer: Janno T. <jaxnnxot@gmail.com>
_author=TURNSTEP
_perlmod=Math-GMP
pkgname=perl-math-gmp
pkgver=2.06
pkgrel=0
pkgdesc="High speed arbitrary size integer math "
arch=(any)
url="http://search.cpan.org/~$_author/$_perlmod-$pkgver/"
license=('GPL' 'PerlArtistic')
depends=('perl>=5.10.0', 'gmp')
options=(!emptydirs)
source=(http://cpan.perl.org/modules/by-authors/id/T/TU/$_author/$_perlmod-$pkgver.tar.gz)
md5sums=('0ead0cd7d7ec1076c6d5a5fbe81b91a3')

build() {
  cd "$srcdir/$_perlmod-$pkgver"

  # Install module in vendor directories.
  PERL_MM_USE_DEFAULT=1 perl Makefile.PL INSTALLDIRS=vendor
  make
}

package() {
  cd "$srcdir/$_perlmod-$pkgver"
  make install DESTDIR="$pkgdir/"
}

# vim:set ts=2 sw=2 et:
