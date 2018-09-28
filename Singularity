Bootstrap: docker
From: ubuntu:16.04
IncludeCmd: yes

%labels
Author Jason Chow
Version v0.01

%apprun blender
exec /opt/blender "$@"

%post
apt-get update
apt-get install -y curl \
  tar \
  bzip2 \
  libglu1 \
  libxi6 \
  libxrender1

mkdir /opt/blender
curl -ssL https://mirror.clarkson.edu/blender/release/Blender2.79/blender-2.79b-linux-glibc219-x86_64.tar.bz2 | \
  tar -jxv --strip-components=1 -C /opt/blender
