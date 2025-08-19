pkgname=crush
pkgrel=1
pkgdesc="The glamourous AI coding agent for your favourite terminal"
arch=('x86_64' 'arm64')
url="https://github.com/klarkc/crush"
license=('MIT')
provides=("${pkgname}")
conflicts=("${pkgname}")
vcs=('git')

pkgver=v0.6.3.7.g3a66612a

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
