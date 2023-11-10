# Flutter Wrap widget

https://api.flutter.dev/flutter/widgets/Wrap-class.html

![image](https://github.com/luiscoco/flutter_wrap_widget/assets/32194879/61298e11-fc47-4952-ac09-5c11d487ff94)

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: MyWrapApp(),
    );
  }
}

class MyWrapApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Wrap Widget Sample'),
      ),
      body: Wrap(
        spacing: 8.0, // spacing between adjacent chips
        runSpacing: 4.0, // spacing between lines of chips
        children: [
          MyChip('Flutter'),
          MyChip('Dart'),
          MyChip('Widgets'),
          MyChip('Mobile'),
          MyChip('Development'),
          MyChip('UI'),
          MyChip('Layout'),
        ],
      ),
    );
  }
}

class MyChip extends StatelessWidget {
  final String label;

  MyChip(this.label);

  @override
  Widget build(BuildContext context) {
    return Chip(
      label: Text(label),
      backgroundColor: Colors.blue,
      labelStyle: TextStyle(color: Colors.white),
    );
  }
}
```
