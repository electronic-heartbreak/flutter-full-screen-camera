# full_screen_camera

This project contains a simple solution to make the camera fullscreen, or atleast, take up all the available space without losing aspect ratio or having 'zooming-in' issues. The following code is the most important:

```dart
return SizedBox(
    width: size.width,
    height: size.height,
    child: FittedBox(
    fit: BoxFit.cover,
    child: SizedBox(
        width: 100, // the actual width is not important here
        child: CameraPreview(_controller),
    ),
    ),
);
```
