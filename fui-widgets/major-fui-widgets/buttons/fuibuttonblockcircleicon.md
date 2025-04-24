# FUIButtonBlockCircleIcon

<figure><img src="../../../.gitbook/assets/fuiblockbuttonicon.png" alt=""><figcaption></figcaption></figure>

The `FUIButtonBlockCircleIcon` is a fully colored circle icon button. This button is comparable to Flutter’s`ElevatedButton`, providing a more "Bootstrap"-liked aesthetic.

As its name implies, it is a full background-colored ‘block’ styled button (similar to `FUIButtonBlockTextIcon`), with the icon serving as the sole label.

## Widget Class Location

The `FUIButtonBlockCircleIcon` widget classes could be found in:

```
lib/focus_ui_kit/components/button/fui_button_block_circle_icon.dart
```

The `FUIButtonTheme` class is the theme class holds the default theme variables/values.

### Accessing the theme

To access the theme class object, do the following:

```dart
@override
Widget build(BuildContext context) {
    FUIButtonTheme buttonTheme = context.theme.fuiButton;
    
    // ...
}
```

## Usage

The `FUIButtonBlockCircleIcon` widget is developer-friendly and requires minimal configuration. It can be utilized by\
providing an icon and an `onPressed` callback, as demonstrated below:

```dart
FUIButtonBlockCircleIcon(
    icon: Icon(CupertinoIcons.arrow_right),
    onPressed: () {},
);
```

### Changing the size

Different sizes could be configured for the `FUIButtonBlockCircleIcon`, namely:

1. Large
2. Medium (default)
3. Small

This can be accomplished by configuring the `fuiButtonSize` parameter, which accepts values from the `FUIButtonSize`\
enumeration.

```dart
/// Large
FUIButtonBlockCircleIcon(
    icon: Icon(CupertinoIcons.arrow_right),
    fuiButtonSize: FUIButtonSize.large,
    onPressed: () {},
);

/// Medium (default)
FUIButtonBlockCircleIcon(
    icon: Icon(CupertinoIcons.arrow_right),
    fuiButtonSize: FUIButtonSize.medium,
    onPressed: () {},
);

/// Small
FUIButtonBlockCircleIcon(
    icon: Icon(CupertinoIcons.arrow_right),
    fuiButtonSize: FUIButtonSize.small,
    onPressed: () {},
);
```

### Changing the color scheme

<figure><img src="../../../.gitbook/assets/fuiblockbuttonicon02.png" alt=""><figcaption></figcaption></figure>

The `FUIButtonBlockCircleIcon` can be customized with a different color scheme by configuring the `fuiColorScheme` parameter. This parameter accepts values from the `FUIColorScheme` enum, allowing for flexibility in color selection.

```dart
FUIButtonBlockCircleIcon(
    fuiColorScheme: FUIColorScheme.success,
    icon: Icon(CupertinoIcons.arrow_right),
    onPressed: () {},
);
```

### Enabling / Disabling with Controller

<figure><img src="../../../.gitbook/assets/fuiblockbuttonicon03.gif" alt=""><figcaption></figcaption></figure>

The `FUIButtonBlockCircleIcon` enables the control of button functionality via a controller.

This can be achieved via the `FUIButtonController` controller.

```dart
/// Define the controller (usually in the initState function)
FUIButtonController btnCtrl = FUIButtonController();

/// Attached it with a FUIButtonBlockCircleIcon widget.
FUIButtonBlockCircleIcon(
    fuiButtonController: btnCtrl,
    icon: Icon(CupertinoIcons.check_mark),
    onPressed: () {},
);

/// Toggle enable
btnCtrl.trigger(FUIButtonEvent(
    enable: true,
));

/// Toggle disable
btnCtrl.trigger(FUIButtonEvent(
    enable: false,
));

/// Close the controller (do this in the dispose function)
btnCtrl.close();
```

## Major Parameters

| Parameters                               | Description                                               |
| ---------------------------------------- | --------------------------------------------------------- |
| Icon? icon                               | The icon for the button.                                  |
| FUIColorScheme fuiColorScheme            | The desired color scheme of the button.                   |
| FUIButtonSize fuiButtonSize              | The desired pre-configured size of the button             |
| FUIButtonController? fuiButtonController | The controller to toggle enable / disable for the button. |
| Color? backgroundColor                   | A custom background color for the button.                 |

## Other parameters

The other parameters corresponds to the ones available in `ElevatedButton`.
