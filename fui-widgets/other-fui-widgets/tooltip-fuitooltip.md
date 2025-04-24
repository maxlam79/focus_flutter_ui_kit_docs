# Tooltip - FUITooltip

<figure><img src="../../.gitbook/assets/fuitooltip01.gif" alt=""><figcaption></figcaption></figure>

The `FUITooltip` widget provides a means to display tooltips on mouse hover for virtually any widget.

> The `FUITooltip` leverages the `just_the_tooltip` package from [https://pub.dev/packages/just\_the\_tooltip](https://pub.dev/packages/just_the_tooltip). Please refer to this for more info.

### Widget Class Location

The `FUITooltip` widget class could be found in:

```dart
lib/focus_ui_kit/components/tooltip/fui_tooltip.dart
```

The `FUITooltipTheme` class is the theme class holds the default theme variables/values.

#### Accessing the theme

To access the theme class object, do the following:

```dart
@override
Widget build(BuildContext context) {
    FUITooltipTheme ttTheme =  context.theme.fuiTooltip;
    
    // ...
}
```

### Usage

Utilizing the `FUITooltip` feature is straightforward. Simply enclose the widget within another widget, and the tooltip will be displayed accordingly.

```dart
FUITooltip(
  tooltip: Text('This is a tooltip'),
  child: FUIButtonBlockTextIcon(text: Text('Press Me'), onPressed: () {}),
);
```

#### Position the tooltip

The tooltip’s position can be customized by specifying the `preferredDirection` parameter. This parameter accepts values from the `AxisDirection` enum.

```dart
/// Position tooltip - UP
FUITooltip(
  preferredDirection: AxisDirection.up,
  tooltip: Text('This is a tooltip'),
  child: FUIButtonBlockTextIcon(text: Text('Press Me'), onPressed: () {}),
);

/// Position tooltip - DOWN
FUITooltip(
  preferredDirection: AxisDirection.down,
  tooltip: Text('This is a tooltip'),
  child: FUIButtonBlockTextIcon(text: Text('Press Me'), onPressed: () {}),
);

/// Position tooltip - LEFT
FUITooltip(
  preferredDirection: AxisDirection.left,
  tooltip: Text('This is a tooltip'),
  child: FUIButtonBlockTextIcon(text: Text('Press Me'), onPressed: () {}),
);

/// Position tooltip - RIGHT
FUITooltip(
  preferredDirection: AxisDirection.right,
  tooltip: Text('This is a tooltip'),
  child: FUIButtonBlockTextIcon(text: Text('Press Me'), onPressed: () {}),
);
```

### Other Parameters

The other parameters correspond to the [just\_the\_tooltip](https://pub.dev/packages/just_the_tooltip) package.\
Please refer to this package for more info.
