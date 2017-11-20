# react-native-image-cropping-android
Simple react-native image cropping library wrapper around [Android Image Cropper](https://github.com/ArthurHub/Android-Image-Cropper)

## install

```
npm install --save https://github.com/sarangan/react-native-image-cropping-android.git
```


Add the following to android/settings.gradle:

```
include ':react-native-image-cropping-android'
project(':react-native-image-cropping-android').projectDir = new File(settingsDir, '../node_modules/react-native-image-cropping-android/android')
```


Add the following to android/app/build.gradle:
```
...

dependencies {
    ...
    compile project(':react-native-image-cropping-android')
}
```


Add the following to android/app/src/main/java/**/MainApplication.java:

```
import sara.img.crop.ImageCroppingPackage;

public class MainApplication extends Application implements ReactApplication {

    @Override
    protected List<ReactPackage> getPackages() {
        return Arrays.<ReactPackage>asList(
            new MainReactPackage(),
            new ImageCroppingPackage()     // android-toast
        );
    }
}
```


add this to your react-native js

```
import ImageCropper from 'react-native-image-cropping-android';
ImageCropper.CropImage(url).then(uri =>{});

```
