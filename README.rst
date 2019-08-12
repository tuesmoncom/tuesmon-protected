===============
tuesmon-protected
===============

tuesmon-protected is a service that implements token validation.

This project is a part of the system. The complete system is integrated by:

- nginx with specific configuration.

- tuesmon-protected service to validate tokens (this!)

- tuesmon-contrib-protected plugin, an alternative storage system for tuesmon-back.

Configuration
=============

The server has 2 configuration options:

- `SECRET_KEY`. This is the shared secret used by the signer.

- `MAX_AGE` (optional). This is the expiration time in seconds.

Options could be set using environment variables or in a `.env` file.

Vendoring
=========

How to update vendored libraries.

.. code::

   pip install -t _vendor -r _vendor/vendor.txt --no-compile --no-deps
   rm -rf _vendor/*.dist-info/

