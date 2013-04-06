Affirm
======

Affirm is an Android application that intermittently reminds you of your self-affirmations, goals, resolutions, or whatever else you choose to add.
These affirmations, when enabled, work from the background so the device can continue normal use.

##Technical Overview##

Affirmations are triggered by a scheduled Intent to a BroadcastReceiver; this minimizes resource use by only loading what is necessary to show the message, and then closing. Unless the user is editing the preferences, there are no Activities or Services running.
Affirm provides a lot of end-user options with minimal overhead by delivering messages via Toast with customized duration, font color, positioning, and more in the works.

##Contributions##

Contributors and supporters are welcome. I will gratefully acccept translations, pull requests, and gifts/donations via paypal.

<div style="margin:0 1.75em;padding-top:1.75em;text-align:center;max-width:40%;clear:right;" class="right"><p>If you like Affirm, please support my ad-free development projects with a donation via paypal!</p>
<form action="https://www.paypal.com/cgi-bin/webscr" method="post" style="width:100%;">
<input type="hidden" name="cmd" value="_s-xclick" style="margin:0;">
<input type="hidden" name="encrypted" value="-----BEGIN PKCS7-----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-----END PKCS7-----">
<input type="image" src="https://www.paypalobjects.com/en_US/i/btn/btn_donate_SM.gif" border="0" name="submit" alt="PayPal - The safer, easier way to pay online!"><img alt="" border="0" src="https://www.paypalobjects.com/en_US/i/scr/pixel.gif" width="1" height="1">
</form>&nbsp;</div>


###Fine Print###

Copyright © 2010-2012, Shane Ian Robinson. All Rights Reserved.
