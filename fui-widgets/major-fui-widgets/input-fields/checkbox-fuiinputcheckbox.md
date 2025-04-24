# Checkbox - FUIInputCheckbox

<figure><img src="../../../.gitbook/assets/fuiinputcheckbox01.gif" alt=""><figcaption></figcaption></figure>

The `FUIInputCheckbox` is a variation of the toggle-like widget found in the UI Kit.

### Widget Class Location

The `FUIInputCheckbox` widget classes could be found in:

```
lib/focus_ui_kit/components/input/fui_input_checkbox.dart
```

### Widget Theme Location

The `FUIInputCheckbox` class is the theme class holds the default theme variables/values.

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

Using the `FUIInputCheckbox` is simple, just this will do:

```dart
FUIInputCheckbox(
  initialValue: true,
  onChanged: (val) {
    print('val: $val');
  },
);
```

#### Tristate

<figure><img src="../../../.gitbook/assets/fuiinputcheckbox02.gif" alt=""><figcaption></figcaption></figure>

In the context of the checkbox, the value can be either `true`, `false`, or `null`, this is called a `tristate`. However, if the `tristate` option is disabled, the values can only be `true` or `false`.

> Note: if `tristate` is NOT enabled, setting the `initialValue` to `null` will have the value set as `false`.

```dart
FUIInputCheckbox(
  initialValue: true,
  tristate: true,
  onChanged: (val) {
  
    // val can be true, false or null.
    print('val: $val');
  },
);
```

#### Using a controller

<figure><img src="../../../.gitbook/assets/fuiinputcheckbox03.gif" alt=""><figcaption></figcaption></figure>

The `FUIInputCheckbox` shares the same controller class as the `FUIInputToggleSwitch`, which is the`FUIInputFieldToggleController`.

```dart
/// Define and setup the controller (likely in the initState function)
FUIInputFieldToggleController tCtrl = FUIInputFieldToggleController();

/// Assign it on a toggle switch widget
FUIInputCheckbox(
  initialValue: true,
  fuiInputFieldToggleController: tCtrl,
  onChanged: (val) {},
);

/// Close the controller (likely in the dispose function)
tCtrl.close();
```

**Enable / disable the toggle `FUIInputCheckbox`**

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

**Configure readonly on `FUIInputCheckbox`**

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

**Value assignment on `FUIInputCheckbox`**

```dart
/// Set to 'true'
tCtrl.trigger(FUIInputFieldToggleEvent(
  value: true,
));

/// Set to 'false'
tCtrl.trigger(FUIInputFieldToggleEvent(
  value: false,
));

/// Set to 'null'
tCtrl.trigger(FUIInputFieldToggleEvent(
  value: null,
));
```

### Parameters

| Parameters                                                   | Description                                                                                           |
| ------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------- |
| FUIInputFieldToggleController? fuiInputFieldToggleController | The controller for the `FUIInputCheckbox`.                                                            |
| bool? initialValue                                           | The initial value of the checkbox - either `true`, `false` or `null` (only when tristate is enabled). |
| FUIInputSize fuiInputSize                                    | Configure the display size of the checkbox.                                                           |
| FUIColorScheme fuiColorScheme                                | The color scheme for the `FUIInputCheckbox`.                                                          |
| bool tristate                                                | Enable/disable tristate.                                                                              |
| Color? activeColor                                           | Configure the active/checked background color (overrides color scheme).                               |
| Color? checkColor                                            | Configure the checkmark color (overrides color scheme).                                               |
| Color? focusColor                                            | Configure the background color when the widget is focused.                                            |
| Color? hoverColor                                            | Configure the background color when the widget is hovered.                                            |
| bool readOnly                                                | Make the `FUIInputCheckbox` to be readonly.                                                           |
| bool enable                                                  | Enable/disable the `FUIInputCheckbox`.                                                                |

### Other parameters

The other parameters corresponds to the ones available in Flutter's `Checkbox`.
