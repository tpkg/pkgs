#!/bin/sh

VER=2.8.1
PKGVER=1

rpm --quiet -q openssl-devel zlib-devel || sudo yum -y install openssl-devel zlib-devel
tpkg -q mysql || tpkg -i mysql
gem2tpkg mysql --version=$VER --package-version=$PKGVER --extra-deps=mysql,,, --native-deps=openssl,,,zlib,,, --build-options '--with-mysql-config=/opt/tpkg/mysql/bin/mysql_config --with-dldflags="-Wl,-rpath,/opt/tpkg/mysql/lib/mysql"'

