# Maintainer: Fotis 'NlightNFotis' Koutoulakis <fotis.koutoulakis@gmail.com>

pkgname=llvmpy-git
pkgver=0.9
pkgrel=1
pkgdesc="Python Bindings for LLVM"
url="http://www.llvmpy.org"
arch=('i686' 'x86_64')
license=('custom:BSD')
depends=('llvm>=3.1' 'python>=3.1')
makedepends=('gcc' 'g++' 'git')
conflicts=()
replaces=('llvm-py')
backup=()
source=(http://pypi.python.org/packages/source/l/llvmpy/llvmpy-0.9.tar.gz)
md5sums=('1ec34570663b33bf053f7a63d0ee67ef')


build() {
  cd $startdir/src
  git clone https://github.com/llvmpy/llvmpy.git
  cd llvmpy
  echo "Initiating Installation for Python 3."
  python setup.py install \
    --prefix=/usr \
    --root=$startdir/pkg \
    --llvm-config=`which llvm-config` \
    || return 1
}
