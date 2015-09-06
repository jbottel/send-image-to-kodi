send-image-to-kodi
======================

send-image-to-kodi is a Google Chrome/Chromium extension which allows Kodi users to display an image from their browser on any Kodi instance. This is useful for environments when a user would like to share an image with a broader group onto a television screen where Kodi is being used, or for any similar reason.

In order to use send-image-to-kodi, a user should set ``xbmchost`` to the URL at which Kodi's JSON-RPC server is running. In most cases, this is the same URL as any other application submitting requests to Kodi would use. For example, if Kodi is running on the machine with IP address ``10.0.0.1``, xbmchost would be configured as ``xbmchost = http://10.0.0.1:8080/jsonrpc``. The ``xbmchost`` option is found within ``contextMenu.js``.

In order to use send-image-to-kodi, find any image in your browser and right-click to bring up the context menu. The default option is called "Show Image on Media Center". The title of the context menu option can be customized by setting the ``title`` variable to desired title. The ``title`` option is also found within ``contextMenu.js``.

Notes on Kodi screensaver option
--------------
Kodi does not traditiaionally ovverride a screensaver or dim screen when receiving an image request from the JSON-RPC server. To overcome this limitation, send-image-to-kodi sends a random directional remote request in order for Kodi to believe that the screen should "wake up". This works great for most purposes, but if a simple directional request will interrupt your use-case of Kodi, you should disable this function by eliminating the the two lines which mention ``requestDir`` in ``contextMenu.js``. 

How to Use
---
Until this extension is added to the Chrome marketplace, the best way to install this extension is to download the zip file and add it to Chrome. In recent versions of Chrome, you may have to enable 'Developer Mode' in order to use the extension.
