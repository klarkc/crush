pkgname=crush
pkgrel=1
pkgdesc="The glamourous AI coding agent for your favourite terminal"
arch=('x86_64' 'arm64')
url="https://github.com/klarkc/crush"
license=('MIT')
provides=("${pkgname}")
conflicts=("${pkgname}")
vcs=('git')

pkgver=v0.1.0.gb03a42df

pkgver() {
  git describe --long --tags | sed 's/\([^-]*-\)-g/\1r/' | sed 's/-/./g'
}

source=()

prepare() {
  rsync -a ../ ./
}

build() {
  go build -o crush .
}

package() {
  install -Dm755 crush "${pkgdir}/usr/bin/crush"
}
