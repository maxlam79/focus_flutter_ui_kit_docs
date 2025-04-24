# Fonts & Colors

### Primary Font

The **InterV** font serves as the default font throughout the UI kit. It is a sans-serif, open-source font that comes with a comprehensive weight coverage.

#### InterV Font Files Location & pubspec.yaml

The font files are situated within the `focus_ui_kit_responsive/fonts/inter` folder.

In the _**pubspec.yaml**_, the font family is designated as “**Inter**”.

### Code Display Font

The UI kit consists of a widget named **FUICodeDisplayBox** specifically designed for code display purposes. This widget utilizes **JetBrains-Mono** for rendering code.

#### JetBrains-Mono Font Files Location & pubspec.yaml

The font files are situated in the directory _**focus\_ui\_kit\_responsive/fonts/jetbrains-mono/**_.

In the **pubspec.yaml** file, the font family is designated as “**JetBrainsMono**”.

### How to change the default fonts

Although not recommended, here are the steps to modify the default fonts:

1. Please include the font files in the directory \`_**focus\_ui\_kit\_responsive/fonts**_. Kindly create a new directory for the font files.
2. Edit the \`_**pubspec.yaml**_ file to define the fonts.
3. Investigate the file `focus_ui_kit/components/typography/fui_typography_theme.dart`. This file contains a static field that defines the default font used throughout the theme.
4. Replace the following code with your newly added font:

```dart
abstract class FUITypographyTheme {
    ...
    /// Font Family Names
    static const String fontFamilyPrimary = 'Inter';  // Replace to the newly installed font name 
    static const String fontFamilyCodeDisplay = 'JetBrainsMono';
    ...
}
```

5. There might be a need to adjust the font sizes, do this in`focus_ui_kit/components/typography/fui_typography_theme.dart`.

#### More info on Fonts and Typography

Please explore the demo app on _Menu -> Elements -> Typography_ to have a better understanding.

### Primary Color & Secondary Color

The Focus UI kit incorporates both primary and secondary colors to maintain a cohesive theme while emphasizing &#x6D;_&#x69;nimalist_ aesthetic.

| Color     | Code                 |
| --------- | -------------------- |
| Primary   | #D81E5B (Ruby)       |
| Secondary | #1C1C1C (Near Black) |

#### Color Scheme

To provide a broader range of color options, some FUI widgets offer the capability to customize the color scheme. This\
can be achieved by setting the _**FUIColorScheme**_ parameter.

Do explore the `focus_ui_kit/theme/fui_colors.dart` file on color scheme.

#### How to change the primary & secondary color

To change the primary & secondary color:

1. Explore the `focus_ui_kit/theme/fui_colors.dart` file;
2. Go to the section:

```dart
class FUIThemeCommonColorsLight extends FUIThemeCommonColors {
    ...
    
    /// *** General ***
    @override
    Color get primary => const Color(0xffD81E5B);
    
    @override
    Color get secondary => const Color(0xff1C1C1C);
    ...
}
```

Then, modify the getter for both the primary and/or the secondary.

#### How to access the colors

Colors can be called via:

```dart
@override
Widget build(BuildContext context) {
    FUIThemeCommonColors fuiColors = context.theme.fuiColors;
    
    /// Use it
    Color primaryColor = fuiColors.primary;
}  
```

#### Other Colors and Shades

The remaining colors and shades are defined in the `focus_ui_kit/theme/fui_theme.dart` file.

#### More info on Colors

Please explore the demo app through _Menu -> Elements -> Colors_ to have a better understanding.
