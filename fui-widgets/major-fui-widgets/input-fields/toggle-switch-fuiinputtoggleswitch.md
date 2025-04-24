# Toggle Switch - FUIInputToggleSwitch

<figure><img src="../../../.gitbook/assets/fuiinputtoggle01.gif" alt=""><figcaption></figcaption></figure>

The `FUIInputToggleSwitch` is a user-friendly on/off switch component available within the UI kit.

### Widget Class Location

The `FUIInputToggleSwitch` widget classes could be found in:

```
lib/focus_ui_kit/components/input/fui_input_toggle_switch.dart
```

### Widget Theme Location

The `FUIInputToggleSwitch` class is the theme class holds the default theme variables/values.

#### Accessing the theme

To access the theme class object, do the following:

```dart
@override
Widget build(BuildContext context) {
    FUIInputTheme fuiInputTheme = context.theme.fuiInput;
    
    // ...
}
```

### Usage

<figure><img src="../../../.gitbook/assets/fuiinputtoggle02.gif" alt=""><figcaption></figcaption></figure>

Below are illustrative examples of the UI Kit’s toggle switch in various common usage scenarios:

```dart
//Default (without label) 
FUIInputToggleSwitch(
  initialValue: true,
  onChanged: (val) {},
);

// Show on/off
FUIInputToggleSwitch(
  initialValue: true,
  showOnOff: true,
  onChanged: (val) {},
),

// Custom active / inactive label
FUIInputToggleSwitch(
  initialValue: true,
  activeText: Text('Yes'),
  inactiveText: Text('No'),
  onChanged: (val) {},
);
```

#### Customizable active / inactive

<figure><img src="../../../.gitbook/assets/fuiinputtoggle03.gif" alt=""><figcaption></figcaption></figure>

The toggle switch’s active/inactive (true/false) UI display could be customized, as follows:

```dart
FUIThemeCommonColors fuiColors = context.theme.fuiColors;

FUIInputToggleSwitch(
  initialValue: true,
  
  activeText: Text('Yes', style: TextStyle(color: fuiColors.shade5)),
  activeColor: fuiColors.namedBanana,
  activeIcon: Icon(CupertinoIcons.check_mark, color: fuiColors.shade0),
  activeToggleColor: fuiColors.namedBlack,

  inactiveText: Text('No', style: TextStyle(color: fuiColors.shade0)),
  inactiveColor: fuiColors.namedCobalt,
  inactiveIcon: Icon(CupertinoIcons.xmark, color: fuiColors.shade0),
  inactiveToggleColor: fuiColors.namedBlack,
  onChanged: (val) {
    print('val: $val');
  },
);
```

#### Other configurations

<figure><img src="../../../.gitbook/assets/fuiinputtoggle04.gif" alt=""><figcaption></figcaption></figure>

Certain aspects of the `FUIInputToggleSwitch` can be controlled programmatically using the `FUIInputFieldToggleController`.

```dart
/// Define and setup the controller (likely in the initState function)
FUIInputFieldToggleController tCtrl = FUIInputFieldToggleController();

/// Assign it on a toggle switch widget
FUIInputToggleSwitch(
  initialValue: true,
  showOnOff: true,
  fuiInputFieldToggleController: tCtrl,
  onChanged: (val) {},
);

/// Close the controller (likely in the dispose function)
tCtrl.close();
```

**Enable / disable the toggle `FUIInputToggleSwitch`**

```dart
/// Enable
tCtrl.trigger(FUIInputFieldToggleEvent(
  enabled: true,
));

/// Disable
tCtrl.trigger(FUIInputFieldToggleEvent(
  enabled: false,
));
```

**Configure readonly on `FUIInputToggleSwitch`**

```dart
/// Read Only
tCtrl.trigger(FUIInputFieldToggleEvent(
  readOnly: true,
));

/// Read Only (off)
tCtrl.trigger(FUIInputFieldToggleEvent(
  readOnly: false,
));
```

**Value assignment on `FUIInputToggleSwitch`**

```dart
/// Set to 'true'
tCtrl.trigger(FUIInputFieldToggleEvent(
  value: true,
));

/// Set to 'false'
tCtrl.trigger(FUIInputFieldToggleEvent(
  value: false,
));
```

### Parameters

| Parameters                                                   | Description                                                      |
| ------------------------------------------------------------ | ---------------------------------------------------------------- |
| FUIInputFieldToggleController? fuiInputFieldToggleController | The controller for the `FUIInputToggleSwitch`.                   |
| bool initialValue                                            | The initial value for the toggle switch.                         |
| ValueChanged\<bool> onChanged                                | The call back function on any value change.                      |
| FUIInputSize fuiInputSize                                    | Configure the display size of the toggle switch.                 |
| FUIColorScheme fuiColorScheme                                | The color scheme for the `FUIInputToggleSwitch`.                 |
| bool showOnOff                                               | Shows On/Off as label (The default doesn't have a label).        |
| Widget? activeText                                           | Custom active label text.                                        |
| Widget? inactiveText                                         | Custom inactive label text.                                      |
| Color? activeColor                                           | Custom active color.                                             |
| Color? inactiveColor                                         | Custom inactive color.                                           |
| Color? toggleColor                                           | Custom toggle color.                                             |
| Color? activeToggleColor                                     | Custom active toggle color (background).                         |
| Color? inactiveToggleColor                                   | Custom active toggle color (background).                         |
| BoxBorder? switchBorder                                      | Custom switch border.                                            |
| BoxBorder? activeSwitchBorder                                | Custom active switch border.                                     |
| BoxBorder? inactiveSwitchBorder                              | Custom inactive switch border.                                   |
| BoxBorder? toggleBorder                                      | Custom toggle switch border.                                     |
| BoxBorder? activeToggleBorder                                | Custom active toggle switch border.                              |
| BoxBorder? inactiveToggleBorder                              | Custom inactive toggle switch border.                            |
| Widget? activeIcon                                           | Custom icon when the toggle is on 'active' state.                |
| Widget? inactiveIcon                                         | Custom icon when the toggle is on 'inactive' state.              |
| Duration? toggleAniDuration                                  | Custom animation duration of the toggle while switching.         |
| Curve? toggleAniCurve                                        | Custom animation curve of the toggle while switching.            |
| bool readOnly                                                | Set the `FUIInputToggleSwitch` to be `readonly`.                 |
| bool enabled                                                 | Enable/disable the `FUIInputToggleSwitch`.                       |
| Duration? enableOpacityAniDuration                           | Custom animation duration of the toggle opacity while switching. |
| Curve? enableOpacityAniCurve                                 | Custom animation curve of the toggle opacity while switching.    |
