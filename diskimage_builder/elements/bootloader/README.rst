==========
bootloader
==========

Installs ``grub[2]`` on boot partition on the system.

Arguments
=========

* ``DIB_GRUB_TIMEOUT`` sets the ``grub`` menu timeout.  It defaults to
  5 seconds.  Set this to 0 (no timeout) for fast boot times.

* ``DIB_GRUB_TIMEOUT_STYLE`` sets the visibility of the ``grub`` menu.
  It defaults to ``hidden`` (or ``countdown`` as an alias). Set this to
  ``menu`` to display the menu and then wait for the timeout set by
  ``DIB_GRUB_TIMEOUT`` to expire before booting the default entry.

* ``DIB_BOOTLOADER_DEFAULT_CMDLINE`` sets parameters that are appended
  to the ``GRUB_CMDLINE_LINUX_DEFAULT`` values in ``grub.cfg``
  configuration. It defaults to ``nofb nomodeset gfxpayload=text``.

* ``DIB_BOOTLOADER_SERIAL_CONSOLE`` sets the serial device to be
  used as a console. It defaults to ``hvc0`` for PowerPC, 
  ``ttyAMA0,115200`` for ARM64, otherwise ``ttyS0,115200``.

* ``DIB_BOOTLOADER_VIRTUAL_TERMINAL`` sets the virtual terminal be
  used as a console. It defaults to ``tty0``. When explicitly set
  to an empty string then no virtual terminal console kernel argument
  is added.
