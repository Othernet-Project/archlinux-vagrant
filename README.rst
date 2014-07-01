===========================
Arch Linux i686 vagrant box
===========================

This is a vagrant box based on Arch Linux i686. Installer
archlinux-2014.06.01-dual was used to create the image. For most part, this box
is bare-bones, with just a few additional packages and no stack-specific
packages.

Versions
========

 - v20140630_ 405 MiB (md5: 940dcbd30b18dae99c8992a97f638b65)

Each file can be checked against the CHECKSUMS file in this repository.

Installation
============

To add the Arch Linux minimal base box, run::

    vagrant box add archlinux-i686 URL

where ``URL`` is the download URL in the Versions_ section.

Additional packages
===================

Apart from the base system, the following additional packages are installed:

 - net-tools
 - openssh
 - sudo
 - base-devel
 - virtualbox-guest-modules

Configuration
=============

Following configuration changes have been made:

 - ``vagrant`` user added
 - ``vagrant`` user added to ``wheel`` group
 - enabled ``wheel`` group to use sudo without password
 - added DHCP network configuration for all interfaces
 - loaded ``vboxguest`` and ``vboxsf`` modules on boot
 - added Vagrant's insecure public key to ``vagrant`` user's
   ``authorized_keys``
 - enabled sshd service


.. _v20140630: https://dl.dropboxusercontent.com/s/09iq7rmvs268t64/archlinux-i686-20140630.box
