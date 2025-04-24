# Responsive UX/UI

The default responsive UX/UI library upon which the UI Kit relies is [**responsive\_grid**](https://pub.dev/packages/responsive_grid).

If you are familiar with the HTML/Javascript Bootstrap framework, the terms _“xl,” “lg,” “md,” “sm,” and “xs”_ should be well-known to you.

### Usage of responsive\_grid in UI Kit

For responsive UX/UI design, the standard approach involves utilizing **ResponsiveGridRow** and **ResponsiveGridCol** to render content within a **FUISectionContainer**.

> Please consult the `pub.dev` documentation for `responsive_grid`.

In this instance, it has three `FUISectionContainers` (within the `FUISectionPlain`) aligned horizontally evenly on a medium device (md); and once the device’s height and width change to something small that resembles that of a small device, the `FUISectionContainers` should be aligned vertically instead.

```dart
@override
Widget build(BuildContext context) {
    FUIThemeCommonColors fuiColors = context.theme.fuiColors;
    
    return FUISingleChildScrollView(
      child: Column(
        mainAxisAlignment: MainAxisAlignment.start,
        crossAxisAlignment: CrossAxisAlignment.start,
        children: [
          FUISectionPlain(
            backgroundColor: fuiColors.shade2,
            child: ResponsiveGridRow(
              children: [
                ResponsiveGridCol(
                  sm: 12,
                  md: 4,
                  child: FUISectionContainer(
                    backgroundColor: fuiColors.shade0,
                    child: SizedBox(
                      height: 400,
                      child: Center(
                        child: Text('This is 1st widget'),
                      ),
                    ),
                  ),
                ),
                ResponsiveGridCol(
                  sm: 12,
                  md: 4,
                  child: FUISectionContainer(
                    backgroundColor: fuiColors.shade0,
                    child: SizedBox(
                      height: 400,
                      child: Center(
                        child: Text('This is 2nd widget'),
                      ),
                    ),
                  ),
                ),
                ResponsiveGridCol(
                  sm: 12,
                  md: 4,
                  child: FUISectionContainer(
                    backgroundColor: fuiColors.shade0,
                    child: SizedBox(
                      height: 400,
                      child: Center(
                        child: Text('This is 3rd widget'),
                      ),
                    ),
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

### What about responsive values?

In certain scenarios, it is necessary to assign distinct values for different device sizes. This is where the _**responsiveValue**_ (a component of the `responsive_grid`) plays a crucial role.

#### Usage of responsiveValue

Here is a simple illustration of applying distinct padding values to accommodate varying device screen sizes:

```dart
FUISectionPlain(
    child: FUISectionContainer(
      padding: responsiveValue(
        context,
        xl: EdgeInsets.all(20),
        lg: EdgeInsets.all(15),
        md: EdgeInsets.all(10),
        sm: EdgeInsets.all(5),
        xs: EdgeInsets.all(2),
      ),
      child: Center(
        child: Text('responsiveValue in action'),
      ),
    ),
);
```
