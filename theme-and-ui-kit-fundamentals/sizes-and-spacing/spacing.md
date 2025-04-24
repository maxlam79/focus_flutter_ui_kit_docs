# Spacing

In certain scenarios, widgets may require spacing between them. This can be achieved by utilizing the `FUISpacer` class.

### FUISpacer

The **FUISpacer** class, defined in `focus_ui_kit/layout/fui_spacer.dart`, provides pre-defined vertical and horizontal space values, enabling the creation of space that is handy when arranging widgets within `Column` or `Row`.

#### Vertical Spacing

```dart
Column(
  children: [
    FUIButtonBlockTextIcon(fuiButtonSize: FUIButtonSize.large, text: Text('Large Button'), onPressed: () {}),
    FUISpacer.vSpace20,     // Vertical space of 20.
    FUIButtonBlockTextIcon(fuiButtonSize: FUIButtonSize.medium, text: Text('Medium Button'), onPressed: () {}),
    FUISpacer.vSpace10,     // Vertical space of 10.
    FUIButtonBlockTextIcon(fuiButtonSize: FUIButtonSize.small, text: Text('Small Button'), onPressed: () {}),
  ],
);
```

These buttons are spaced with `FUISpacer.vSpace20`, at height of 20 in between.

#### Horizontal Spacing

```dart
Row(
  children: [
    FUIButtonBlockTextIcon(fuiButtonSize: FUIButtonSize.large, text: Text('Large Button'), onPressed: () {}),
    FUISpacer.hSpace20,     // Horizontal space of 20.
    FUIButtonBlockTextIcon(fuiButtonSize: FUIButtonSize.medium, text: Text('Medium Button'), onPressed: () {}),
    FUISpacer.hSpace10,     // Horizontal space of 10.
    FUIButtonBlockTextIcon(fuiButtonSize: FUIButtonSize.small, text: Text('Small Button'), onPressed: () {}),
  ],
);
```

These buttons are spaced with `FUISpacer.hSpace20`, at width of 20 in between.

You can utilize either `FUISpacer.hSpaceXX` for horizontal spacing or `FUISpacer.vSpaceXX` for vertical spacing.
