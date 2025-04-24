# FUIColumn

The `FUIColumn` widget serves as a wrapper for the standard Flutter `Column` widget. The Flutter `Column` widget is configured with `mainAxisAlignment` set to `MainAxisAlignment.start` and `crossAxisAlignment` set to`CrossAxisAlignment.center`. However, in this UI kits, we require the `crossAxisAlignment` to be set to`CrossAxisAlignment.start`.

Therefore, the `FUIColumn` is a shorthand of:

```dart
Column(
    mainAxisAlignment = MainAxisAlignment.start,
    crossAxisAlignment = CrossAxisAlignment.start,
    children: [...],
);
```

### Widget Class Location

The `FUIColumn` widget class could be found in:

```dart
focus_ui_kit/layout/fui_column.dart
```

### Usage

The usage of `FUIColumn` is equivalent to Flutter’s `Column` widget. This widget will automatically align its child\
widgets to the top-left corner of the container.

```dart
FUIColumn(
    children: [
        SomeWidget1(),
        SomeWidget2(),
        ...
    ],
);
```

### Parameters

All other parameters of `FUIColumn` corresponds with Flutter's `Column` widget.
