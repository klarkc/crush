pkgname=crush
pkgrel=1
pkgdesc="The glamourous AI coding agent for your favourite terminal"
arch=('x86_64' 'arm64')
url="https://github.com/klarkc/crush"
license=('MIT')
provides=("${pkgname}")
conflicts=("${pkgname}")
vcs=('git')

pkgver=v0.7.1.12.gf838b5b0

pkgver() {
  git describe --long --tags | sed 's/\([^-]*-\)-g/\1r/' | sed 's/-/./g'
}

source=("$pkgname::git+$url.git")
sha256sums=('SKIP')

build() {
  # Change directory into the cloned repo
  cd "$pkgname"
  go build -o crush .
}

package() {
  # Install the binary from within the cloned repo directory
  install -Dm755 "$pkgname/crush" "${pkgdir}/usr/bin/crush"
}
