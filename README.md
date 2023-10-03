# prusa-connect-api

This is just a public repo with some question and a download of https://connect.prusa3d.com/docs/cameras/openapi.yaml

The OpenAPI spec is publically available.

I'd like to build an Android app or a flutter app eventually that is more effecient as a camera for the prusa connect hardware. Such software would:
* require wake locks
* dim the screen
* turn the screen off if not in use to save battery
* possiby also cross post to SLACK for redundancy
* start on boot/reboot
* have more control over the camera/zoom into the picture
* do some mild camera picture adjustments
  * contrast
  * crop
  * saturation
  * ...
* change the resolution
