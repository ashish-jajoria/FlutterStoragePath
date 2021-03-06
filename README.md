![Publish](https://github.com/ashish-jajoria/FlutterStoragePath/workflows/Publish/badge.svg?branch=master&event=push)

# StoragePath

A flutter plugin to get all images, audios, videos and files location path in json format based on [StoragePath](https://github.com/follow2vivek/StoragePath).

> Only for Android.
> If you like this plugin, buy me a cup of coffee.
> [PayPal](https://paypal.me/ashishjajoria)

```dart
dependencies:
 flutter_storage_path: ^0.0.2
```


```dart
import 'package:storage_path/storage_path.dart';
```
Sample Code
```dart 
 try {
      imagePath = await StoragePath.imagesPath; //contains images path and folder name in json format
    } on PlatformException {
      imagesPath = 'Failed to get path';
    }
```
AND

```dart
videoPath = await StoragePath.videoPath; //this will return videos path
audioPath = await StoragePath.audioPath; //this will return audios path
filePath = await StoragePath.filePath; //this will return files path
```

Image Json Sample
 ```json 

[
  {
    "files": [
      "path/screenshot/abc.png",
      "path/screenshot/pqr.png"
    ],
    "folderName": "screenshot"
  }
]
  ```
File Json Sample
```json
[
  {
    "files": [
      {
        "mimeType": "application/pdf",
        "size": "34113",
        "title": "C001-SP-2719^201902",
        "path": "/storage/emulated/0/Download/abc.pdf"
      }
    ],
    "folderName": "Download"
  }
]
```
Audio Json Sample
```json
[
  {
    "files": [
      {
        "album": "ABC",
        "artist": "PQR",
        "path": "/storage/emulated/0/Download/todo.mp3",
        "dateAdded": "1515060080",
        "displayName": "todo.mp3",
        "duration": "235986",
        "size": "9506989"
      }
    ],
    "folderName": "Download"
  }
]
```
Video Json Sample
```json
[
  {
    "files": [
      {
        "path": "/storage/emulated/0/DCIM/Camera/VID_20190304_112455.mp4",
        "dateAdded": "1551678904",
        "displayName": "VID_20190304_112455.mp4",
        "duration": "7147",
        "size": "12787914"
      }
    ],
    "folderName": "Camera"
  }
]
```
## Special Thanks to
- [Vivek Sharma](https://github.com/follow2vivek) for base [StoragePath](https://github.com/follow2vivek/StoragePath) repository

## Thank you for contribution
- [Aman Gupta](https://github.com/thealteria)
