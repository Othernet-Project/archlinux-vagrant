=====================================
Arch Linux minimal Vagrant base boxes
=====================================

This repositories contain truly minimal Arch Linux base boxes for Vagrant.
Currently, only VirtualBox images are provided, and only for the i686
architecture (32-bit).

Versions
========

- archlinux-i686-v20140630_ 405 MiB (md5: 940dcbd30b18dae99c8992a97f638b65)

Each file can be checked against the CHECKSUMS file in this repository.

Installation
============

To add the Arch Linux minimal base box, run::

    vagrant box add archlinux-ARCH URL

where ``ARCH`` is the architecture (i686 or x86-64) and ``URL`` is the download 
URL in the Versions_ section.

Provisioning
============

None of the boxes provide anything apart from built-in shell provider (no
Puppet, no Chef, etc).

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


.. _archlinux-i686-v20140630: https://dl.dropboxusercontent.com/s/09iq7rmvs268t64/archlinux-i686-20140630.box
