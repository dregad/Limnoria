.. _plugin-Hashes:

Documentation for the Hashes plugin for Supybot
===============================================

Purpose
-------
Provides various hash- and encryption-related commands.

Usage
-----
Provides hash or encryption related commands

.. _commands-Hashes:

Commands
--------
.. _command-Hashes-algorithms:

algorithms <takes no arguments>
  Returns the list of available algorithms.

.. _command-Hashes-md5:

md5 <text>
  Returns the md5 hash of a given string.

.. _command-Hashes-mkhash:

mkhash <algorithm> <text>
  Returns TEXT after it has been hashed with ALGORITHM. See the 'algorithms' command in this plugin to return the algorithms available on this system.

.. _command-Hashes-sha:

sha <text>
  Returns the SHA1 hash of a given string.

.. _command-Hashes-sha256:

sha256 <text>
  Returns a SHA256 hash of the given string.

.. _command-Hashes-sha512:

sha512 <text>
  Returns a SHA512 hash of the given string.

Configuration
-------------
supybot.plugins.Hashes.public
  This config variable defaults to "True", is not network-specific, and is  not channel-specific.

  Determines whether this plugin is publicly visible.

