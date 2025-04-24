# FUIButtonLinkIcon

<figure><img src="../../../.gitbook/assets/fuibuttonlinkicon01.png" alt=""><figcaption></figcaption></figure>

The `FUIButtonLinkIcon` is a clickable icon button.

> Please note that the icon line color is the `secondary` color, not the `primary` color.

### Widget Class Location

The `FUIButtonLinkIcon` widget classes could be found in:

```
lib/focus_ui_kit/components/button/fui_button_link_icon.dart
```

The `FUIButtonTheme` class is the theme class holds the default theme variables/values.

#### Accessing the theme

To access the theme class object, do the following:

```dart
@override
Widget build(BuildContext context) {
    FUIButtonTheme buttonTheme = context.theme.fuiButton;
    
    // ...
}
```

### Usage

The `FUIButtonLinkIcon` widget is user-friendly and requires only an icon and the `onPressed` callback to be\
implemented. For instance:

```dart
FUIButtonLinkIcon(
    icon: Icon(CupertinoIcons.arrow_right),
    onPressed: () {},
);
```

#### Changing the size

Different sizes could be configured for the `FUIButtonOutlinedCircleIcon`, namely:

1. Large
2. Medium (default)
3. Small

This can be accomplished by configuring the `fuiButtonSize` parameter, which accepts values from the `FUIButtonSize`\
enumeration.

```dart
/// Large
FUIButtonLinkIcon(
    icon: Icon(CupertinoIcons.arrow_right),
    fuiButtonSize: FUIButtonSize.large,
    onPressed: () {},
);

/// Medium (default)
FUIButtonLinkIcon(
    icon: Icon(CupertinoIcons.arrow_right),
    fuiButtonSize: FUIButtonSize.medium,
    onPressed: () {},
);

/// Small
FUIButtonLinkIcon(
    icon: Icon(CupertinoIcons.arrow_right),
    fuiButtonSize: FUIButtonSize.small,
    onPressed: () {},
);
```

#### Changing the color scheme

<figure><img src="../../../.gitbook/assets/fuibuttonlinkicon02.png" alt=""><figcaption></figcaption></figure>

The `FUIButtonLinkIcon` can be customized with a different color scheme by configuring the `fuiColorScheme` parameter. This parameter accepts values from the `FUIColorScheme` enum, allowing for flexibility in color selection.

```dart
FUIButtonLinkIcon(
    fuiColorScheme: FUIColorScheme.success,
    icon: Icon(CupertinoIcons.arrow_right),
    onPressed: () {},
);
```

#### Enabling / Disabling with Controller

The `FUIButtonLinkIcon` enables the control of button functionality through a controller.

This functionality can be implemented using the `FUIButtonController` controller.

```dart
/// Define the controller (usually in the initState function)
FUIButtonController btnCtrl = FUIButtonController();

/// Attached it with a FUIButtonOutlinedCircleIcon widget.
FUIButtonLinkIcon(
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

### Major Parameters

| Parameters                               | Description                                               |
| ---------------------------------------- | --------------------------------------------------------- |
| Icon icon                                | The icon for the button.                                  |
| FUIColorScheme fuiColorScheme            | The desired color scheme of the button.                   |
| FUIButtonSize fuiButtonSize              | The desired pre-configured size of the button             |
| FUIButtonController? fuiButtonController | The controller to toggle enable / disable for the button. |

### Other parameters

The other parameters corresponds to the ones available in `IconButton`.
