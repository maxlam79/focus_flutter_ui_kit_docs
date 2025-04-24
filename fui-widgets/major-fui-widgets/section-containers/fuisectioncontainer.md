# FUISectionContainer

As outlined in the documentation section on the [**Basic UI Structure**](../../../theme-and-ui-kit-fundamentals/basic-ui-structure.md), the `FUISectionContainer` element corresponds to the HTML `<div>` tag, which is commonly employed within the UI Kit to construct padded containers within the`FUISectionPlain`.

### Widget Class Location

The `FUISectionContainer` widget class could be found in:

```
focus_ui_kit/components/section/fui_section_container.dart
```

### Widget Theme Location

The `FUISectionTheme` class serves as the theme class for `FUISectionContainer`, equivalent to `FUISectionPlain`. Kindly explore this theme class to examine various settings applicable to `FUISectionContainer`.

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
            child: ResponsiveGridRow(
              children: [
                ResponsiveGridCol(
                  md: 6,
                  xs: 12,
                  child: FUISectionContainer(
                    child: Regular(Text('This is FUISectionContainer 1')),
                  ),
                ),
                ResponsiveGridCol(
                  md: 6,
                  xs: 12,
                  child: FUISectionContainer(
                    child: Regular(Text('This is FUISectionContainer 2')),
                  ),
                ),
              ],
            ),
          ),
        ],
      ),
    );

}
```

### Other Parameters

The other parameters corresponds with Flutter's `Container` widget.
