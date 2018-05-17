# Qt

For Qt-based applications we have the `org.kde.Sdk` that will offer us most Qt
modules and KDE Frameworks for our applications to use.

For example, the following JSON makes building a random Qt application really
straight-forward.

.. code-block:: json

    {
      "id": "org.kde.blinken",
      "runtime": "org.kde.Platform",
      "runtime-version": "5.9",
      "sdk": "org.kde.Sdk",
      "command": "blinken",
      "finish-args": ["--share=ipc", "--socket=x11", "--socket=wayland", "--device=dri" ],

      "modules": [
        {
          "name": "blinken",
          "builddir": true,
          "buildsystem": "cmake-ninja",
          "sources": [
            {
              "type": "git",
              "url": "git://anongit.kde.org/blinken.git"
            }
          ]
        }
      ]
    }
