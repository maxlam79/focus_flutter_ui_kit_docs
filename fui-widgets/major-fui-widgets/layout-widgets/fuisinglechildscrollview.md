# FUISingleChildScrollView

For scrolling functionality, if a widget exceeds the screen size or layout boundaries, the `FUISingleChildScrollView` is a recommended containing widget. Similar to Flutter’s `SingleChildScrollView` widget, the `FUISingleChildScrollView` offers the same scrolling functionality with a themed scroll bar consistent with the UI Kit's aesthetics.

### Widget Class Location

The `FUISingleChildScrollView` widget class could be found in:

```
focus_ui_kit/layout/fui_scrollview.dart
```

### Usage

```dart
@override
Widget build(BuildContext context) {
    return FUISingleChildScrollView(
      fuiColorScheme: FUIColorScheme.primary, /// Change the color scheme here (default is primary).
      child: SizedBox(
        height: 1000,
        child: Center(
          child: Regular(Text('Centered Text')),
        ),
      ),
    );
}
```

### Major Parameters

| Parameters                    | Description                                                                                                                                                                              |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| FUIColorScheme fuiColorScheme | <p>Allows you the select the desired color scheme for the scroll view. This affects the color of the scroll bar.<br>The default color scheme is <code>FUIColorScheme.primary</code>.</p> |
| Color? scrollbarColor         | Setting a custom color for the scroll bar. This will override the color suggested by fuiColorScheme.                                                                                     |

### Other Parameters

The other parameters correspond to Flutter's `SingleChildScrollView`.
