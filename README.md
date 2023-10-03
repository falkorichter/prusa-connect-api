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

## Other quick wins/ideas:
* build a command line tool to upload pictures from a raspberry pi
* octoprint plugin for camera integration

# sample upload request (tested)

```
curl --location --request PUT 'https://webcam.connect.prusa3d.com/c/snapshot' \
--header 'token: <your token from https://connect.prusa3d.com/printer/<your-printer>/cameras>' \
--header 'fingerprint: <your token from reverse engineered from another web cam app' \
--header 'Content-Type: image/jpeg' \
--data '@z96u9g9q3/sample_upload.jpg'                             
```

## Questions:
* What is max file size?
* Which file formats are allowed? Is JPEG-2000 possible?
* Where is is the ´fingerprint´ from? See https://github.com/falkorichter/prusa-connect-api/issues/2
* Is the `https://webcam.connect.prusa3d.com/c/info`

# outreach

I reached out to Josef Prusa on Mastodon:
* https://berlin.social/@volkersfreunde/111172878224039056
* https://berlin.social/@volkersfreunde/111172913258846704
* also reached out to https://www.facebook.com/pitlik / https://twitter.com/Pitlik who seems to be on the same topic in the forum (https://forum.prusa3d.com/forum/bugs-errors/prusaconnect-camera-api-issue-with-fingerprint/)
