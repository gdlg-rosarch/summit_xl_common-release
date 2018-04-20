# Script generated with Bloom
pkgdesc="ROS - The summit_xl_localization package"
url='http://ros.org/wiki/summit_xl_localization'

pkgname='ros-kinetic-summit-xl-localization'
pkgver='1.1.2_1'
pkgrel=1
arch=('any')
license=('BSD'
)

makedepends=('ros-kinetic-catkin'
'ros-kinetic-geographic-msgs'
'ros-kinetic-geometry-msgs'
'ros-kinetic-mavros-msgs'
'ros-kinetic-message-filters'
'ros-kinetic-nav-msgs'
'ros-kinetic-robot-localization'
'ros-kinetic-robotnik-msgs'
'ros-kinetic-rosbag'
'ros-kinetic-roscpp'
'ros-kinetic-rostest'
'ros-kinetic-sensor-msgs'
'ros-kinetic-std-msgs'
'ros-kinetic-std-srvs'
'ros-kinetic-tf'
'ros-kinetic-tf2'
'ros-kinetic-tf2-geometry-msgs'
'ros-kinetic-tf2-ros'
)

depends=('ros-kinetic-geographic-msgs'
'ros-kinetic-geometry-msgs'
'ros-kinetic-mavros-msgs'
'ros-kinetic-message-filters'
'ros-kinetic-message-runtime'
'ros-kinetic-nav-msgs'
'ros-kinetic-robot-localization'
'ros-kinetic-robotnik-msgs'
'ros-kinetic-roscpp'
'ros-kinetic-sensor-msgs'
'ros-kinetic-std-msgs'
'ros-kinetic-std-srvs'
'ros-kinetic-tf'
'ros-kinetic-tf2'
'ros-kinetic-tf2-geometry-msgs'
'ros-kinetic-tf2-ros'
)

conflicts=()
replaces=()

_dir=summit_xl_localization
source=()
md5sums=()

prepare() {
    cp -R $startdir/summit_xl_localization $srcdir/summit_xl_localization
}

build() {
  # Use ROS environment variables
  source /usr/share/ros-build-tools/clear-ros-env.sh
  [ -f /opt/ros/kinetic/setup.bash ] && source /opt/ros/kinetic/setup.bash

  # Create build directory
  [ -d ${srcdir}/build ] || mkdir ${srcdir}/build
  cd ${srcdir}/build

  # Fix Python2/Python3 conflicts
  /usr/share/ros-build-tools/fix-python-scripts.sh -v 2 ${srcdir}/${_dir}

  # Build project
  cmake ${srcdir}/${_dir} \
        -DCMAKE_BUILD_TYPE=Release \
        -DCATKIN_BUILD_BINARY_PACKAGE=ON \
        -DCMAKE_INSTALL_PREFIX=/opt/ros/kinetic \
        -DPYTHON_EXECUTABLE=/usr/bin/python2 \
        -DPYTHON_INCLUDE_DIR=/usr/include/python2.7 \
        -DPYTHON_LIBRARY=/usr/lib/libpython2.7.so \
        -DPYTHON_BASENAME=-python2.7 \
        -DSETUPTOOLS_DEB_LAYOUT=OFF
  make
}

package() {
  cd "${srcdir}/build"
  make DESTDIR="${pkgdir}/" install
}

