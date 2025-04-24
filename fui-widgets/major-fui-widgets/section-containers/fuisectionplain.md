# FUISectionPlain

Previously outlined in the documentation section on the [**Basic UI Structure**](../../../theme-and-ui-kit-fundamentals/basic-ui-structure.md), the `FUISectionPlain` element corresponds to the HTML `<section>` tag. This widely used tag in the UI Kit enables the creation of “sections” on a page, encapsulating various widgets within a single container.

### Widget Class Location

The `FUISectionPlain` widget class could be found in:

```
focus_ui_kit/components/section/fui_section_plain.dart
```

### Widget Theme Location

The `FUISectionTheme` class serves as the theme class for `FUISectionPlain`. Kindly explore this theme class to ascertain various settings applicable to `FUISectionPlain`.

#### Accessing the theme

To access the theme class object, do the following:

```dart
@override
Widget build(BuildContext context) {
    FUISectionTheme fuiSectionTheme = context.theme.fuiSection;
    
    // ...
}
```

### Usage

```dart
@override
Widget build(BuildContext context) {

    return FUISingleChildScrollView(
      child: FUIColumn(
        children: [
          FUISectionPlain(
            horizontalSpace: FUISectionHorizontalSpace.tight,
            child: FUISectionContainer(
              child: Column(
                children: [
                  H1(Text('Heading 1')),
                  Regular(Text('Content Text')),
                ],
              ),
            ),
          ),
        ],
      ),
    );
    
}
```

> **Please refer to the** [**Basic UI Structure**](../../../theme-and-ui-kit-fundamentals/basic-ui-structure.md) **section to learn more on horizontalSpace.**

### Major Parameters

| Parameters                                | Description                                                                                                                                                                                                                               |
| ----------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| EdgeInsets? padding                       | <p>Corresponds to the padding of a <code>Container</code>.<br>Please explore some of the pre-defined padding EdgeInsets in <code>FUISectionTheme.eiSecPaddingXX</code> before configuring this with specific <code>EdgetInsets</code></p> |
| Color? backgroundColor                    | The default color of the is `fuiColors.bg0`.                                                                                                                                                                                              |
| FUISectionHorizontalSpace horizontalSpace | Accepts values from `FUISectionHorizontalSpace`; the default is `FUISectionHorizontalSpace.focus`.                                                                                                                                        |

### Other Parameters

The other parameters correspond with Flutter's `Container` widget.
