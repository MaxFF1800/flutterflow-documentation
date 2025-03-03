---
title: "Deployment/Build for mobile error: NoDecoderForImageFormatException"
custom_edit_url: null
showLastUpdateTime: false
hide_title: true
slug: "7038400-deployment-build-for-mobile-error-nodecoderforimageformatexception"
hide_table_of_contents: true
---

The issue is your icon file, the builder can not make the icon launcher file from your icon file selected.

It could be the file format, For example, if you selected an SVG file for your icon.

​

![](https://downloads.intercomcdn.com/i/o/681166860/5f83b15bdb937c7fafb247e3/image.png?expires=1741032900&signature=ad3c523cc5fe07a0dc667927b5afba6aecb56fcfb90c3282fe73d202a1718f22&req=cigmF894lYdfFb4f3HP0gI3R7SgFiZOegYRcUrIf0FuBxuOZIUfSlQI0ALiY%0AE4U%3D%0A)

Go to the Setting/App assets and change the icon and splash image

Make sure 

1- The size of the asset you selected is not too big 

2- Select a PNG/JPEG file icon, not SVG or something else

​

Try to use a 1024x1024 pixel size icon for the size at least.

Note: Because Flutterflow uses the same icon asset to generate the ios and android icons, it is important that the asset you selected meets the guide lines of the two devices.

For example, for ios better, you don't use PNG assets with transparent parts in it.

Useful links:

https://developer.android.com/distribute/google-play/resources/icon-design-specifications

https://developer.apple.com/design/human-interface-guidelines/foundations/app-icons/