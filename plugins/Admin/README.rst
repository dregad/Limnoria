.. _plugin-Admin:

Documentation for the Admin plugin for Supybot
==============================================

Purpose
-------
These are commands useful for administrating the bot; they all require their
caller to have the 'admin' capability.  This plugin is loaded by default.

Usage
-----
This plugin provides access to administrative commands, such as
adding capabilities, managing ignore lists, and joining channels.
This is a core Supybot plugin that should not be removed!

.. _commands-Admin:

Commands
--------
.. _command-Admin-acmd:

acmd <command> [<arg> ...]
  Perform <command> (with associated <arg>s on all channels on current network.

.. _command-Admin-capability.add:

capability add <name|hostmask> <capability>
  Gives the user specified by <name> (or the user to whom <hostmask> currently maps) the specified capability <capability>

.. _command-Admin-capability.remove:

capability remove <name|hostmask> <capability>
  Takes from the user specified by <name> (or the user to whom <hostmask> currently maps) the specified capability <capability>

.. _command-Admin-channels:

channels takes no arguments
  Returns the channels the bot is on.

.. _command-Admin-clearq:

clearq takes no arguments
  Clears the current send queue for this network.

.. _command-Admin-ignore.add:

ignore add <hostmask|nick> [<expires>]
  This will set a persistent ignore on <hostmask> or the hostmask currently associated with <nick>. <expires> is an optional argument specifying when (in "seconds from now") the ignore will expire; if it isn't given, the ignore will never automatically expire.

.. _command-Admin-ignore.list:

ignore list takes no arguments
  Lists the hostmasks that the bot is ignoring.

.. _command-Admin-ignore.remove:

ignore remove <hostmask|nick>
  This will remove the persistent ignore on <hostmask> or the hostmask currently associated with <nick>.

.. _command-Admin-join:

join <channel> [<key>]
  Tell the bot to join the given channel. If <key> is given, it is used when attempting to join the channel.

.. _command-Admin-nick:

nick [<nick>] [<network>]
  Changes the bot's nick to <nick>. If no nick is given, returns the bot's current nick.

Configuration
-------------
supybot.plugins.Admin.public
  This config variable defaults to "True", is not network-specific, and is  not channel-specific.

  Determines whether this plugin is publicly visible.

