# Radio Buttons - FUIInputRadio

<figure><img src="../../../.gitbook/assets/fuiinputradio01.gif" alt=""><figcaption></figcaption></figure>

The `FUIInputRadio` widget is the UI Kit’s representation of a radio button.

### Widget Class Location

The `FUIInputRadio` widget classes could be found in:

```
lib/focus_ui_kit/components/input/fui_input_radio.dart
```

### Widget Theme Location

The `FUIInputRadio` class is the theme class holds the default theme variables/values.

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

The `FUIInputRadio` widget is recommended to be utilized within a Stateful widget, typically in conjunction with the`FUIInputFieldRadioGroupController`, which functions as the common value holder for multiple radio buttons of the same group.

Here's an example:

```dart

// Define the radio group controller
FUIInputFieldRadioGroupController<int> radioGroupCtrl = FUIInputFieldRadioGroupController<int>(1);

// With value 1
FUIInputRadio<int>(
  fuiInputFieldRadioGroupController: radioGroupCtrl,
  value: 1,
  onChanged: (val) {},
);

// With value 2
FUIInputRadio<int>(
  fuiInputFieldRadioGroupController: radioGroupCtrl,
  value: 2,
  onChanged: (val) {},
);

// With value 3
FUIInputRadio<int>(
  fuiInputFieldRadioGroupController: radioGroupCtrl,
  value: 3,
  onChanged: (val) {},
);

// To get the value...
int? selectedVal = radioGroupCtrl.groupValue;
```

When multiple `FUIInputRadio` widgets share the same `FUIInputFieldRadioGroupController`, they collectively form a\
group. Consequently, when different `FUIInputRadio`(s) with the same `FUIInputFieldRadioGroupController` are utilized,\
the`groupValue` within the `FUIInputFieldRadioGroupController` undergoes a change.

#### Data Type of Value

The `FUIInputRadio` and the `FUIInputFieldRadioGroupController` accept a generic type parameter, thereby determining the`groupValue` type as well.

If a different data type, such as `String`, is desired, it can be easily achieved as follows:

```dart
FUIInputFieldRadioGroupController<String> radioGroupCtrl = FUIInputFieldRadioGroupController<String>('A');

FUIInputRadio<String>(
    fuiInputFieldRadioGroupController: radioGroupCtrl,
    ...
);
```

#### Using a controller

The `FUIInputFieldRadioController` facilitates the management of the enable/disable and readonly status of the`FUIInputRadio`.

For example:

```dart
// Define the controller
FUIInputFieldRadioController ctrl = FUIInputFieldRadioController();

// Assign the controller 
FUIInputRadio<String>(
    fuiInputFieldRadioController: ctrl,
    ...
);

// Toggle enable
ctrl.trigger(FUIInputFieldRadioEvent(
  enable: true,
));

// Toggle disable
ctrl.trigger(FUIInputFieldRadioEvent(
  enable: false,
));

// Toggle readOnly
ctrl.trigger(FUIInputFieldRadioEvent(
  readOnly: true,
));
```

### Parameters

| Parameters                                                               | Description                                                                                       |
| ------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------- |
| FUIColorScheme fuiColorScheme                                            | The color scheme for the `FUIInputRadio`.                                                         |
| FUIInputFieldRadioGroupController\<T>? fuiInputFieldRadioGroupController | The radio button group value controller .                                                         |
| FUIInputFieldRadioController? fuiInputFieldRadioController               | The general purpose controller.                                                                   |
| T value                                                                  | The value when the radio button is selected (conform to the generic type of the `FUIInputRadio`). |
| FUIInputSize fuiInputSize                                                | Configure the display size of the checkbox.                                                       |

### Other parameters

The other parameters corresponds to the ones available in Flutter's `Radio`.
