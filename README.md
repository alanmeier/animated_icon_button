# animated_icon_button

😊 Flutter package to create custom <strong>animated</strong> IconButton.</br>
😵 <strong>Includes all available icons.</strong> Based on native IconButton.

<img src="https://github.com/Frezyx/animated_icon_button/blob/master/example/rep_files/preview.gif?raw=true" width="270">

## Getting Started
Follow these steps to use this library

### Add dependency

```yaml
dependencies:
  animated_icon_button: ^0.3.0 #latest version
```

### Add import package

```dart
import 'package:animated_icon_button/animated_icon_button.dart';
```

### Easy to use
Simple example of use AnimatedIconButton<br>
Put this code in your project at an screen and learn how it works 😊

```dart
    AnimatedIconButton(
        size: 35,
        onPressed: () {
          print("button with color pressed");
        },
        duration: Duration(milliseconds: 200),
        endIcon: Icon(
            Icons.close,
                color: Colors.red,
            ),
        startIcon: Icon(
            Icons.add,
            color: Colors.purple,
        ),
    )
```

### Custom animation controller

In order to animate your icons in a custom way, like on text changed or when pressing a button, just use the ```animationController``` property as follows. </br>

```dart
    var animationController = AnimationController(
        vsync: this,
        duration: Duration(milliseconds: 200),
        reverseDuration: Duration(milliseconds: 200),
    );

    AnimatedIconButton(
        animationController: animationController,
        size: 35,
        onPressed: () {
          print("button with color pressed");
        },
        endIcon: Icon(
            Icons.close,
                color: Colors.red,
            ),
        startIcon: Icon(
            Icons.add,
            color: Colors.purple,
        ),
    )
```

Then, whenever you want, execute your ```animationController.forward()``` and ```animationController.reverse()``` methods to get your icons animated.

Don't forget to remove ```duration``` from your ```AnimatedIconButton``` when using this property.

### Attributes

<strong>size:</strong> The size of AnimatedIconButton <br>
<strong>startIcon:</strong> The icon of the AnimatedIconButton when button is not pressed.<br>
<strong>endIcon:</strong> The icon of the AnimatedIconButton when button is pressed. <br>
<strong>duration:</strong> Animation time of the AnimatedIconButton. <br>
<strong>startBackgroundColor:</strong> The background Color of the AnimatedIconButton when button is not pressed. <br>
<strong>endBackgroundColor:</strong> The background Color of the AnimatedIconButton when button is pressed. <br>
<strong>And all fields of the parent element:</strong> <a href="https://api.flutter.dev/flutter/material/IconButton-class.html">IconButton</a>
<br><br>

For help getting started with 😍 Flutter, view our 
[online documentation](https://flutter.dev/docs), which offers tutorials, 
samples, guidance on mobile development, and a full API reference.

