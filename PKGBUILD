# Generated by gem2arch (https://github.com/anatol/gem2arch)
# Maintainer: Anatol Pomozov <anatol.pomozov@gmail.com>
# Contributor: Nathan Phillip Brink <binki@gentoo.org>

_gemname=paperclip
pkgname=ruby-$_gemname
pkgver=4.2.0
pkgrel=1
pkgdesc='File attachments as attributes for ActiveRecord'
arch=(any)
url='https://github.com/thoughtbot/paperclip'
license=(MIT)
depends=(imagemagick ruby ruby-activemodel ruby-activesupport ruby-cocaine ruby-mime-types)
options=(!emptydirs)
source=(https://rubygems.org/downloads/$_gemname-$pkgver.gem)
noextract=($_gemname-$pkgver.gem)
sha1sums=('e9566407b652273faf4a8ea48615108c4a24a8e1')

package() {
  local _gemdir="$(ruby -e'puts Gem.default_dir')"
  gem install --ignore-dependencies --no-user-install -i "$pkgdir/$_gemdir" -n "$pkgdir/usr/bin" $_gemname-$pkgver.gem
  rm "$pkgdir/$_gemdir/cache/$_gemname-$pkgver.gem"
  install -D -m644 "$pkgdir/$_gemdir/gems/$_gemname-$pkgver/LICENSE" "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
