# Animation - FUIAnimationHelper

<figure><img src="../.gitbook/assets/fuianimation01.gif" alt=""><figcaption></figcaption></figure>

The Focus Flutter UI Kit includes the `FUIAnimationHelper` class, a utility class designed to facilitate animation during widget construction.

The `FUIAnimationHelper` serves as a convenience for the `flutter_animator` package, drawing inspiration from the widely-used web library `Animate.css`.

### Widget Class Location

The `FUIAnimationHelper` widget class could be found in:

```dart
lib/focus_ui_kit/animation/fui_animator_helper.dart
```

### Usage

A straightforward illustration of implementing a widget that gradually fades in:

```dart
FUIAnimationHelper.discernAnimator(
  fuiAnimationType: FUIAnimationType.fadeIn,
  child: FUIPanel(
    header: Text('Fade In Panel'),
    content: Center(
      child: Text('Hello...'),
    ),
  ),
);
```

The `FUIAnimationType` enum offers a comprehensive collection of predefined animation types. Please explore further.

#### Controlling the animation duration

The duration and other settings can be achieved via the `preferences` parameter.

For example:

```dart
FUIAnimationHelper.discernAnimator(
  fuiAnimationType: FUIAnimationType.fadeIn,
  preferences: AnimationPreferences(
    duration: Duration(milliseconds: 300),  // Have the animation duration to 300 milliseconds.
  ),
  child: FUIPanel(
    header: Text('Fade In Panel'),
    content: Center(
      child: Text('Hello...'),
    ),
  ),
);
```

#### Animation Status Callback - animationStatusListener

Callback methods can be attached to various animation states. For instance, an example of executing a callback when the animation is completed (via the `animationStatusListener`) is provided below:

```dart
FUIAnimationHelper.discernAnimator(
  fuiAnimationType: FUIAnimationType.fadeIn,
  preferences: AnimationPreferences(
      duration: Duration(milliseconds: 300),
      animationStatusListener: (status) {
        if (status.isCompleted) {
          // Do something...
        }
      }),
  child: FUIPanel(
    header: Text('Fade In Panel'),
    content: Center(
      child: Text('Hello...'),
    ),
  ),
);
```

Kindly refer to the [https://pub.dev/packages/flutter\_animator](https://pub.dev/packages/flutter_animator) package for\
further information.
