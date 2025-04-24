# FUIRow

The `FUIRow` widget serves as a wrapper for the standard Flutter Column widget. The Flutter Column widget is configured with `mainAxisAlignment` set to `MainAxisAlignment.start` and `crossAxisAlignment` set to `CrossAxisAlignment.center`. In many scenarios within the Focus UI Kit, it is necessary to modify the `crossAxisAlignment` to`CrossAxisAlignment.start`.

Therefore, the `FUIRow` is a shorthand of:

```dart
Row(
    mainAxisAlignment = MainAxisAlignment.start,
    crossAxisAlignment = CrossAxisAlignment.start,
    children: [...],
);
```

### Widget Class Location

The `FUIRow` widget class could be found in:

```
focus_ui_kit/layout/fui_row.dart
```

### Usage

The usage of `FUIRow` is the same as Flutter's Row. This will align the widgets to the top left.

```dart
FUIRow(
    children: [
        SomeWidget1(),
        SomeWidget2(),
        ...
    ],
);
```

### Parameters

All other parameters of `FUIRow` corresponds with Flutter's `Row` widget.
