# dropfiles_window
this plugin modify windows style to accep Drag&Drop a file and wheh Drop a file from this other window. this plugin does call a dart callback function.
flutter gets the file name from ths callback function.

## Supported Platforms
- [x] macOS
- [ ] Windows
- [ ] Linux

## Usage
refer /example/lib/main.dart for more details.
```dart
import 'package:dropfiles_window/dropfiles_window.dart';
.
.
.
if (Platform.isWindows == true) {
      // Platform messages may fail, so we use a try/catch PlatformException.
      try {
        DropfilesWindow.modifyWindowAcceptFiles((String strName) {
          // print("fileName=$strName");
          setState(() {
            _dropFileName = strName;
          });
        });
      } on PlatformException {
        _dropFileName = 'Failed to modifyDropFilesWindow.';
      }
    }
```
[Uinsg packages] https://flutter.dev/docs/development/packages-and-plugins/using-packages
