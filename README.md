# Flutter Web Frame

Make the frame max width / size when on large devices such as Web or Desktop.

This is very suitable to be used to limit the size of content, if your application is not yet available a responsive version if it is run on multiple devices / platforms.

## Example Usage

   ```
   import 'package:flutter/foundation.dart';
import 'package:flutter/material.dart';
import 'package:flutter_web_frame/flutter_web_frame.dart';

void main() {
  runApp(MyAp());
}

class MyAp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return FlutterWebFrame(
      builder: (context) {
        return MaterialApp(
          home: Scaffold(
            appBar: AppBar(
              title: Text('Title '),
            ),
            body: Center(
              child: Text('Body Text'),
            ),
          ),
        );
      },
      maximumSize: Size(475.0, 812.0), // Maximum size
      enabled: kIsWeb, // default is enable, when disable content is full size
      backgroundColor: Colors.grey, // Background color/white space
    );
  }
}
   ```
