Affirm
======

Affirm is an Android application that intermittently reminds you of your self-affirmations, goals, resolutions, or whatever else you choose to add.
These affirmations, when enabled, work from the background so the device can continue normal use.

##Technical Overview##

The messages are triggered by a scheduled Intent to a BroadcastReceiver; this minimizes resource use by only loading what is necessary to show the message, and then closing. Unless the user is editing the preferences, there are no Activities or Services running.
Affirm provides a lot of end-user options with minimal overhead by delivering messages via Toast with customized duration, font color, positioning, and more in the works.

