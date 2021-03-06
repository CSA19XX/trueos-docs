**Preface** 

Written by users of the |trueos| operating system.

Copyright © 2005 - 2016 The |trueos| Project.

Welcome to |trueos|! This Handbook covers the installation and use of
|trueos|. This Handbook is a work in progress and relies on the
contributions of many individuals. To assist with the Handbook, refer to
the documentation
`README <https://github.com/trueos/trueos-docs/blob/master/trueos-handbook/README.md>`_.
If using IRC Freenode, join the #trueos channel and converse with many
other |trueos| users.

The |trueos| Users Handbook is freely available for sharing and
redistribution under the terms of the
`Creative Commons Attribution License <https://creativecommons.org/licenses/by/4.0/>`_.
This means you have permission to copy, distribute, translate, and
adapt the work as long as you attribute the |trueos| Project as the
original source of the Handbook.

|trueos| and the |trueos| logo are registered trademarks of
`iXsystems <https://www.ixsystems.com/>`_. To use the |trueos| logo in
your own works, please ask for permission first from
marketing@ixsystems.com.

AMD is a trademark of Advanced Micro Devices, Inc.

Apache is a trademark of The Apache Software Foundation.

|appcafe| is a registered trademark of
`iXsystems <https://www.ixsystems.com/>`_.

Asus® and Eee PC® are registered trademarks of ASUSTeK® Computer Inc.

Facebook® is a registered trademark of Facebook Inc.

Flash® is a registered trademark of Adobe Systems Incorporated in the
United States and/or other countries.

FreeBSD® is a registered trademark of the
`FreeBSD Foundation <https://www.freebsdfoundation.org/>`_.

|freenas| is a registered trademark of
`iXsystems <https://www.ixsystems.com/>`_.

Intel, the Intel logo, Pentium Inside, and Pentium are trademarks of
Intel Corporation in the U.S. and/or other countries.

Java™ is a trademark of Oracle America and/or its affiliates in the
United States and other countries.

LinkedIn® is a registered trademark of LinkedIn Corporation.

Linux® is a registered trademark of Linus Torvalds.

Mac and Mac OS are trademarks of Apple Inc., registered in the U.S. and
other countries.

NVIDIA® is a trademark and/or registered trademark of NVIDIA Corporation
in the U.S. and other countries.

ThinkPad® is a registered trademark of Lenovo.

Twitter is a trademark of Twitter, Inc. in the United States and other
countries.

UNIX® is a registered trademark of The Open Group.

VirtualBox® is a registered trademark of Oracle.

VMWare® is a registered trademark of VMWare, Inc.

Windows® is a registered trademark of Microsoft Corporation in the
United States and other countries.

**Typographic Conventions** 

The |trueos| User Guide uses several typographic conventions, seen here
in :numref:`Table %s <typ conv>`:

.. _typ conv:

.. table:: : Text Formatting Examples

   +----------------------------------------------------------------+-------------------------------------------------+
   | Item                                                           | Visual Example                                  |
   +================================================================+=================================================+
   | Graphical elements: buttons, icons, fields, columns, and boxes | Click the :guilabel:`Import CA` button.         |
   +----------------------------------------------------------------+-------------------------------------------------+
   | Menu selections                                                | Select :menuselection:`System --> Information`. |
   +----------------------------------------------------------------+-------------------------------------------------+
   | Commands                                                       | Use the :command:`scp` command.                 |
   +----------------------------------------------------------------+-------------------------------------------------+
   | File names and volume and dataset names                        | Locate the :file:`/etc/rc.conf` file.           |
   +----------------------------------------------------------------+-------------------------------------------------+
   | Keyboard keys                                                  | Press the :kbd:`Enter` key.                     |
   +----------------------------------------------------------------+-------------------------------------------------+
   | Important points                                               | **This is important.**                          |
   +----------------------------------------------------------------+-------------------------------------------------+
   | Values entered into fields, or device names                    | Enter *127.0.0.1* in the address field.         |
   +----------------------------------------------------------------+-------------------------------------------------+

Introduction
************

Welcome to |trueos|!

`TrueOS® <http://www.pcbsd.org/>`_ (formerly known as |pcbsd|) began in
2005 when Kris Moore presented the first beta version of a FreeBSD
operating system pre-configured for desktop use. Since then, |trueos|
has matured into a polished, feature-rich, free-of-charge, open source
operating system that meets the desktop or server needs of the beginner
to the advanced user alike.

|trueos| is essentially a customized installation of FreeBSD, not a
forked derivative. Since the underlying FreeBSD system has been kept
intact, you have a fully functional FreeBSD system under the hood.
|trueos| provides an easy-to-use installer which can be used to install
a desktop or a server version of FreeBSD. Other differences from FreeBSD
include: 

* |trueos| pre-configures the BSD-licensed, |lumina| desktop
  environment during a desktop installation. Additional desktop
  environments can be installed and will appear in the login menu,
  allowing the user to select  which environment to log into.

* The |trueos| installer supports configuring ZFS and encryption during
  installation.

* |trueos| provides both a graphical and command line software management
  system.

* |trueos| provides many graphical utilities for configuring and managing
  the system. These utilities have both a command line equivalent and
  a REST and WebSocket API so that they can also be used to manage
  multiple systems.

* |trueos| comes pre-configured with a number of automatic scripts to
  perform tasks such as connecting digital cameras or USB memory sticks.

* The |trueos| boot menu supports boot environments, or snapshots of the
  operating system, and the |trueos| Update Manager automatically adds a
  new boot environment to the boot menu before updating the operating
  system or software. This means that if an update fails, the system can
  reboot into the previous version of the operating system, before the
  update occurred.

While it began as an independent project, since October 2006 |trueos| is
financially backed and supported by the enterprise-class hardware
solutions provider `iXsystems <https://www.ixsystems.com/>`_.

.. index:: features
.. _Goals and Features:

Goals and Features
==================

|trueos| provides the following features: 

* **Easy installation:** To install either a graphical desktop or
  command-line server, simply insert the installation media, reboot the
  system to start the installer, and answer a few questions in the
  installation menus.

* **Automatically configured hardware:** Video, sound, network, and
  other devices are configured automatically during installation.

* **Intuitive desktop interface:** |trueos| installs the |lumina|
  desktop, but additional desktop environments can be installed to
  support day-to-day computing needs.

* **Easy software management:** With :ref:`AppCafe®`, installing,
  upgrading, and uninstalling software is safe and easy.

* **Lots of software available:** :ref:`AppCafe®` can be used to install
  software ported to FreeBSD (currently over 26,100 applications).

* **Easy to update:** |trueos| provides a built-in :ref:`Update Manager`
  which provides notifications of available updates. This utility makes
  it easy to apply operating system security fixes, bug fixes, and
  system enhancements, as well as upgrade to newer versions of the
  operating system or installed software.

* **Virus-free:** |trueos| is unaffected by viruses, spyware, or other
  malware.

* **No defragmentation:** |trueos| hard drives do not need to be
  defragmented and are formatted with OpenZFS, a self-healing filesystem.

* **Laptop support:** Provides power saving, swap space encryption, and
  automatic switching between wired and wifi network connections.

* **Secure environment:** |trueos| provides a pre-configured firewall
  and a built-in host-based Intrusion Detection System.

* **Easy system administration:** |trueos| provides many graphical tools
  for performing system administration tasks.

* **Localization:** |trueos| supports a variety of native languages and
  locales.

* **Vibrant community:** |trueos| has a friendly and helpful community.

.. index:: What's New
.. _What's New:

What's New
==========

The following features or enhancements were introduced for |trueos|:

* Based on FreeBSD-CURRENT.

* The GRUB bootloader has been replaced by the FreeBSD bootloader which
  now provides both GELI and boot environment support. The
  :guilabel:`Use GRUB bootloader` checkbox has been added to the
  :guilabel:`Customize Disk Selection` screens for users of dual-boot
  systems who prefer to use the GRUB boot loader.

* A |trueos| installation installs the |lumina| Desktop. Additional
  window managers can be installed using :ref:`AppCafe®`.

* The :ref:`SysAdm™ Client` and server has replaced Control Panel.
  Most of the utilities that were in the Control Panel have been
  rewritten to use the |sysadm| middleware. Under the hood, |sysadm|
  provides REST and WebSocket APIs for securely managing local and
  remote FreeBSD and |trueos| systems.
  
* Many utilities have been converted to the |sysadm| API and are
  available in the :ref:`SysAdm™ client`: :ref:`AppCafe®`,
  :ref:`Update Manager`, :ref:`Boot Environment Manager`,
  :ref:`Life Preserver`, :ref:`Firewall Manager`, :ref:`User Manager`,
  :ref:`Network Manager`, and :ref:`Mount Tray`.
  
* The functionality provided by the *About* utility has been
  incorporated into :ref:`Lumina Information`.
  
* The functionality provided by *Service Manager*
  (:command:`pc-servicemanager`) has been integrated into
  :ref:`Task Manager`.

* The Active Directory & LDAP utility (:command:`pc-adsldap`) has been
  deprecated.

* Login Manager (:command:`pc-dmconf`) has been replaced by
  :command:`pcdm-config`).

* System Manager (:command:`pc-sysmanager`) has been deprecated.

* :command:`freebsd-update` has been retired in favor of using
  :command:`pkg` for system updates.

* The binary for :ref:`Disk Manager` (:command:`pc-zmanager`) has been
  renamed to :command:`pc-diskmanager` and the graphical version has
  been moved to the :guilabel:`Browse Applications` menu.

* The option to use the SCFB display driver has been added to the
  installer. This driver is suitable for newer UEFI laptops as it
  automatically detects native resolution and is a good solution for
  newer Intel drivers that have not been ported yet to FreeBSD. Before
  selecting this driver, check the BIOS and ensure the CSM module is
  disabled. This driver does not support a dual-head configuration, such
  as an external port for presentations, or suspend and resume.

* :guilabel:`Customize` has been removed from the
  :ref:`System Selection Screen` in order to reduce the size of the
  installation media. Additional software can be installed
  post-installation using :ref:`AppCafe®`.

* The :guilabel:`Boot to console (Disable X)` option has been added to
  the graphical boot menu.

* These new utilites are available in the :ref:`SysAdm™ Client`:
  :ref:`Manage SSL Keys` and :ref:`Task Manager`.

* The graphical and command line versions of PBI Manager and Warden have
  been removed.

* **pc-thinclient** has been removed as it is deprecated.

.. index:: Linux
.. _TrueOS® for Linux Users:

TrueOS® for Linux Users
=======================

|trueos| is based on FreeBSD, meaning it is not a Linux distribution.
If you have used Linux before, you will find some features you are used
to have different names on a BSD system and some commands are different.
This section covers some of these differences.

.. index:: filesystems
.. _Filesystems:

BSD and Linux use different filesystems during installation. Many Linux
distros use EXT2, EXT3, EXT4, or ReiserFS, while |trueos| uses OpenZFS.
This means if you wish to dual-boot with Linux or access data on an
external drive formatted with another filesystem, you will want to
research if the data will be accessible to both operating systems.

:numref:`Table %s <filesys support>` summarizes the various filesystems
commonly used by desktop systems. |trueos| will automatically mount
several filesystems: *FAT16*, *FAT32*, *EXT2*, *EXT3*
(without journaling), *EXT4* (read-only), *NTFS5*, *NTFS6*, and *XFS*.
See the section on :ref:`Files and File Sharing` for a comparison of
some graphical file manager utilities.

.. _filesys support:

.. table:: : Filesystem Support on |trueos|

   +------------+-----------+----------------------------+--------------------------------------------------------+
   | Filesystem | Native to | Type of non-native support | **Usage notes**                                        |
   +============+===========+============================+========================================================+
   | Btrfs      | Linux     | none                       |                                                        |
   +------------+-----------+----------------------------+--------------------------------------------------------+
   | exFAT      | Windows   | none                       | requires a license from Microsoft                      |
   +------------+-----------+----------------------------+--------------------------------------------------------+
   | EXT2       | Linux     | r/w support loaded         |                                                        |
   |            |           | by default                 |                                                        |
   +------------+-----------+----------------------------+--------------------------------------------------------+
   | EXT3       | Linux     | r/w support loaded         | since EXT3 journaling is not supported, you will not   |
   |            |           | by default                 | be able to mount a filesystem requiring a journal      |
   |            |           |                            | replay unless you :command:`fsck` it using an          |
   |            |           |                            | external utility such as                               |
   |            |           |                            | `e2fsprogs <http://e2fsprogs.sourceforge.net>`_        |
   +------------+-----------+----------------------------+--------------------------------------------------------+
   | EXT4       | Linux     | r/o support loaded         | EXT3 journaling, extended attributes, and inodes       |
   |            |           | by default                 | greater than 128 bytes are not supported; EXT3         |
   |            |           |                            | filesystems converted to EXT4 may have better          |
   |            |           |                            | performance                                            |
   +------------+-----------+----------------------------+--------------------------------------------------------+
   | FAT16      | Windows   | r/w support loaded         |                                                        |
   |            |           | by default                 |                                                        |
   +------------+-----------+----------------------------+--------------------------------------------------------+
   | FAT32      | Windows   | r/w support loaded         |                                                        |
   |            |           | by default                 |                                                        |
   +------------+-----------+----------------------------+--------------------------------------------------------+
   | HFS+       | Mac OS X  | none                       | older Mac versions might work with                     |
   |            |           |                            | `hfsexplorer <http://www.catacombae.org/hfsexplorer>`_ |
   +------------+-----------+----------------------------+--------------------------------------------------------+
   | JFS        | Linux     | none                       |                                                        |
   +------------+-----------+----------------------------+--------------------------------------------------------+
   | NTFS5      | Windows   | full r/w support loaded    |                                                        |
   |            |           | by default                 |                                                        |
   +------------+-----------+----------------------------+--------------------------------------------------------+
   | NTFS6      | Windows   | r/w support loaded         |                                                        |
   |            |           | by default                 |                                                        |
   +------------+-----------+----------------------------+--------------------------------------------------------+
   | ReiserFS   | Linux     | r/o support is loaded      |                                                        |
   |            |           | by default                 |                                                        |
   +------------+-----------+----------------------------+--------------------------------------------------------+
   | UFS2       | FreeBSD   | check if a Linux distro    | changed to r/o support in Mac Lion                     |
   |            |           | provides ufsutils;         |                                                        |
   |            |           | r/w support on Mac;        |                                                        |
   |            |           | UFS Explorer can be        |                                                        |
   |            |           | used on Windows            |                                                        |
   +------------+-----------+----------------------------+--------------------------------------------------------+
   | ZFS        | |trueos|, |                            |                                                        |
   |            | FreeBSD   |                            |                                                        |
   +------------+-----------+----------------------------+--------------------------------------------------------+

.. index:: devices

Linux and BSD use different naming conventions for devices. For example:

* In Linux, Ethernet interfaces begin with :file:`eth`. With BSD,
  interface names indicate the name of the driver. For example, an
  Ethernet interface may be listed as :file:`re0`, indicating it uses
  the Realtek :file:`re` driver. The advantage of this convention is
  you can read the **man 4** page for the driver (e.g. type
  :command:`man 4 re`) to see which models and features are provided by
  the driver.

* BSD disk names differ from Linux. IDE drives begin with :file:`ad` and
  SCSI and USB drives begin with :file:`da`.

Some of the features used by BSD have similar counterparts to Linux, but
the name of the feature is different. :numref:`Table %s <feature names>`
provides some common examples:

.. _feature names:

.. table:: : BSD and Linux Feature Names

   +------------------------------+---------------------+--------------------------------+
   | TrueOS                       | Linux               | **Description**                |
   +==============================+=====================+================================+
   | IPFW                         | iptables            | default firewall               |
   +------------------------------+---------------------+--------------------------------+
   | :file:`/etc/rc.d/` for       | :file:`rc0.d/`,     | in |trueos|, the directories   |
   | operating system and         | :file:`rc1.d/`,     | containing the startup scripts |
   | :file:`/usr/local/etc/rc.d/` | etc.                | do not link to runlevels as    |
   | for applications             |                     | there are no runlevels; system |
   |                              |                     | startup scripts are separated  |
   |                              |                     | from third-party application   |
   |                              |                     | scripts                        |
   +------------------------------+---------------------+--------------------------------+
   | :file:`/etc/ttys` and        | :command:`telinit`, | terminals are configured in    |
   | :file:`/etc/rc.conf`         | :file:`init.d/`     | *ttys* and *rc.conf* indicates |
   |                              |                     | which services will start at   |
   |                              |                     | boot time                      |
   +------------------------------+---------------------+--------------------------------+

Users comfortable with the command line may find some of the common
Linux commands have different names on BSD.
:numref:`Table %s <common commands>` lists some common commands and
what they are used for.

.. _common commands:

.. table:: : Common BSD and Linux Commands

   +-----------------------------------+-----------------------------+
   | Command                           | **Used to:**                |
   +===================================+=============================+
   | :command:`dmesg`                  | discover what hardware was  |
   |                                   | detected by the kernel      |
   +-----------------------------------+-----------------------------+
   | :command:`sysctl dev`             | display configured devices  |
   +-----------------------------------+-----------------------------+
   | :command:`pciconf -l -cv`         | show PCI devices            |
   +-----------------------------------+-----------------------------+
   | :command:`dmesg | grep usb`       | show USB devices            |
   +-----------------------------------+-----------------------------+
   | :command:`kldstat`                | list all modules loaded in  |
   |                                   | the kernel                  |
   +-----------------------------------+-----------------------------+
   | :command:`kldload <module>`       | load a kernel module for    |
   |                                   | the current session         |
   +-----------------------------------+-----------------------------+
   | :command:`pkg install <pkgname>`  | install software from the   |
   |                                   | command line                |
   +-----------------------------------+-----------------------------+
   | :command:`sysctl hw.realmem`      | display hardware memory     |
   +-----------------------------------+-----------------------------+
   | :command:`sysctl hw.model`        | display CPU model           |
   +-----------------------------------+-----------------------------+
   | :command:`sysctl hw.machine_arch` | display CPU Architecture    |
   +-----------------------------------+-----------------------------+
   | :command:`sysctl hw.ncpu`         | display number of CPUs      |
   +-----------------------------------+-----------------------------+
   | :command:`uname -vm`              | get release version         |
   |                                   | information                 |
   +-----------------------------------+-----------------------------+
   | :command:`gpart show`             | show device partition       |
   |                                   | information                 |
   +-----------------------------------+-----------------------------+
   | :command:`fuser`                  | list IDs of all processes   |
   |                                   | with one or more files open |
   +-----------------------------------+-----------------------------+

There are many articles and videos which provide additional information
about some of the differences between BSD and Linux:

* `Comparing BSD and Linux <http://www.freebsd.org/doc/en/articles/explaining-bsd/comparing-bsd-and-linux.html>`_

* `FreeBSD Quickstart Guide for Linux® Users <http://www.freebsd.org/doc/en/articles/linux-users/index.html>`_

* `BSD vs Linux <http://www.over-yonder.net/~fullermd/rants/bsd4linux/01>`_

* `Why Choose FreeBSD? <http://www.freebsd.org/advocacy/whyusefreebsd.html>`_

* `Interview: BSD for Human Beings <http://www.unixmen.com/bsd-for-human-beings-interview/>`_

* `Video: BSD 4 Linux Users <https://www.youtube.com/watch?v=xk6ouxX51NI>`_

* `Why you should use a BSD style license for your Open Source Project <http://www.freebsd.org/doc/en/articles/bsdl-gpl/article.html>`_

* `A Sysadmin's Unixersal Translator (ROSETTA STONE) <http://bhami.com/rosetta.html>`_