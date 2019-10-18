# ATTENTION
I don't have any time to maintain this plugin anymore. As long as no one wants to maintain it I don't see the possiblity to fix all the stuff mentioned in the issues, sorry. I recommend to not use this plugin anymore.

# Image Resizer for Cordova #
By: Protonet GmbH

Authors: Joschka Schulz

## Adding the Plugin ##
Use the Cordova CLI and type in the following command:
```

// This plugin uses the cordova-plugin-camera
cordova plugin add cordova-plugin-camera

// This plugin
cordova plugin add https://github.com/protonet/cordova-plugin-image-resizer.git
```
## Sample Code

At the moment the plugin is available on iOS

### resize

    window.ImageResizer.resize(options, success, failed);
    
### Options

  - **uri**(String): The Uri for the image on the device to get scaled (can be file:// path).
  - **fileName**(String): A custom name for the file. Default name is a timestamp.
  - **quality**(Number): Quality given as Number for the quality of the new image - defaults to 85
  - **width**(Number): The width of the new image,
  - **height**(Number): The height of the new image
  - **base64**(Boolean): Whether or not to return a base64 encoded image string instead of the path to the resized image (you must set false).

### iOS Example
```
    var options = {
          uri: uri,
          fileName: "image.jpg",
          quality: 90,
          width: 1280,
          height: 1280,
          base64: false
    };

    window.ImageResizer.resize(options,
      function(image) {
         // success: image is the new resized image
      }, function() {
        // failed: grumpy cat likes this function
      });
```
