# Basic UI Structure

### Starter (Skeleton)

To comprehend the fundamental UI structure of the theme, it is recommended to refer to the another separate GitHub project called _**focus\_flutter\_ui\_kit\_starter, found here:**_ [_**https://github.com/maxlam79/focus\_flutter\_ui\_kit\_starter**_](https://github.com/maxlam79/focus_flutter_ui_kit_starter)

The _**focus\_flutter\_ui\_kit\_starter**_ is a vanilla Flutter project that includes a pre-configured `pubspec.yaml`, a basic layout for the top bar, side menu drawers, page routers, and other essential assets. These assets are sufficient to initiate a new project utilizing the UI kit.

> Please ensure that you execute the command `flutter pub get` on the _**focus\_flutter\_ui\_kit\_starter**_.

### Section Containers

#### FUISectionPlain & FUISectionContainer

```dart
@override
Widget build(BuildContext context) {
    FUIThemeCommonColors fuiColors = context.theme.fuiColors;
    
    return FUISingleChildScrollView(
      child: FUIColumn(
        children: [
          FUISectionPlain(
            backgroundColor: fuiColors.shade2,
            child: FUISectionContainer(
              backgroundColor: fuiColors.shade0,
              child: SizedBox(
                height: 400,
                child: Center(
                  child: Text('This text is in FUISectionContainer'),
                ),
              ),
            ),
          ),
        ],
      ),
    );
}
```

Referring to the provided image and code snippets, that was typical container structure employed when utilizing the Focus Flutter UI kit.

The _**FUISectionPlain**_ element, as its name implies, denotes a distinct section or portion of a page dedicated to specific functionalities.

A _**FUISectionPlain**_ can accommodate multiple _**FUISectionContainer**_ elements, where the UI elements are to be placed.

In terms of HTML equivalents, _**FUISectionPlain**_ can be considered analogous to the \<section> tag, whil&#x65;_**FUISectionContainer**_ is comparable to the \<div> tag.

Both _**FUISectionPlain**_ and _**FUISectionContainer**_ elements by default incorporate default padding.

> Think of _**FUISectionPlain**_ as the mother container of one or more _**FUISectionContainer**_(s).

#### Horizontal Space Configuration

For the _**FUISectionPlain**_, you can configure the horizontal side spacing using the _horizontalSpace_ parameter.

> Note: This feature is applicable to medium devices and above (md). For smaller devices and below (sm & xs), the\
> horizontal side padding will be “full” by default.

Here's how it works.

**FUISectionHorizontalSpace.full**

The `FUISectionHorizontalSpace.full` option occupies the entire horizontal screen space.

An illustrative example of “full” is the dashboard and top banner of numerous demonstration applications.

**FUISectionHorizontalSpace.focus**

The `FUISectionHorizontalSpace.focus` option provides a slight padding on the sides of the section. The child widget will likely occupy approximately 85% to 90% of the available screen space.

By default, the “focus” option mode is set for the `FUISectionPlain` widget. You will likely encounter most demo page contents with “focus” horizontal spacing.

**FUISectionHorizontalSpace.tight**

The `FUISectionHorizontalSpace.tight` option provides a slight margin on the sides. The child widget will likely occupy approximately 70% of the available screen space.

A notable illustration of the “tight” layout is the content of the “_Elements -> Colors_” in the demo page.
