# Expo ImagePicker URI Issue on Android

This repository demonstrates a bug in the Expo ImagePicker library on Android where the returned image URI is sometimes invalid.  The bug is intermittent and difficult to reproduce consistently. This repository contains code to reproduce the issue, along with a potential solution.

**Bug:** The `ImagePicker.launchImageLibraryAsync()` function returns an object with a `uri` property, but this URI is sometimes invalid, leading to errors when attempting to display or process the image. The issue is more prominent on specific Android devices.

**Solution:** The proposed solution involves checking the validity of the returned URI before attempting to use it. A robust approach is to make an additional verification step to ensure that the image can be accessed at the returned URI.