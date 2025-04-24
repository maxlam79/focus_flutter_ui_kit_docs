# Theme Files & How To Access

The **Focus Flutter UI Kit** is a themable kit, but not in the manner of the Flutter _Material_ or _Material3_ styles.

### How to import / use the FUI widgets and themes

To utilize the UI kit’s FUI (_acronym for Focus UI_) widgets, simply import a single file.

```
import 'focus_ui_kit/exports.dart';
```

### Theme Structured

The UI kit comprises a common theme and specific themes for the FUI widgets.

### Common Theme

The common theme file is situated at:

```
focus_ui_kit/theme/fui_theme.dart
```

Specifically, the **FUITheme** extension extends the **ThemeData** class, which provides access to all specific themes of all other FUI widgets.

#### How to access FUITheme

The FUITheme serves as a comprehensive wrapper that encapsulates the color palette in the UI kit. Furthermore, it provides specific themes (including font sizes and other size parameters) for various FUI widgets.

Here's a general way on gaining access to these themes.

```dart
@override
Widget build(BuildContext context) {
    
    /// Colors
    FUIThemeCommonColors fuiColors = context.theme.fuiColors;
    
    /// FUIPanel specifics
    FUIPanelTheme panelTheme = context.theme.fuiPanel;
    
    /// and so on... 
}
```

> Note: Only one theme ("light" theme) is available for now. The "dark" theme may be developed in the near future.

### Specific FUI Widget Themes

Each FUI widget or UI category has a distinct theme file. These files are detailed in the corresponding sections on the specific Focus UI widget documentation.

Please refer to the following table for a concise list of FUI widgets and their respective theme files (relative to the`lib/focus_ui_kit` directory):

| FUI Widget              | Theme Class            | Theme File                                                |
| ----------------------- | ---------------------- | --------------------------------------------------------- |
| General Colors          | FUIThemeCommonColors   | theme/fui\_colors.dart                                    |
| Major Theme             | FUITheme               | theme/fui\_theme.dart                                     |
| Accordion               | FUIAccordionTheme      | components/accordion/fui\_accordion\_theme.dart           |
| Action Tile             | FUIActionTileTheme     | components/actiontile/fui\_action\_tile\_theme.dart       |
| Avatar                  | FUIAvatarTheme         | components/avatar/fui\_avatar\_theme.dart                 |
| Buttons                 | FUIButtonTheme         | components/button/fui\_button\_theme.dart                 |
| Calendar                | FUICalendarTheme       | components/calendar/fui\_calendar\_theme.dart             |
| DataTable               | FUIDataTable2Theme     | components/datatable2/fui\_datatable2\_theme.dart         |
| File Upload             | FUIFileUploadTheme     | components/fileupload/fui\_file\_upload\_theme.dart       |
| Input Fields            | FUIInputTheme          | components/input/fui\_input\_theme.dart                   |
| Menu                    | FUIMenuTheme           | components/menu/fui\_menu\_theme.dart                     |
| Modals                  | FUIModalTheme          | components/modal/fui\_modal\_theme.dart                   |
| Toasts                  | FUIToastTheme          | components/notification/fui\_toast\_theme.dart            |
| Pace Bar                | FUIPaceBarTheme        | components/pacebar/fui\_pacebar\_theme.dart               |
| Pane                    | FUIPaneTheme           | components/pane/fui\_pane\_theme.dart                     |
| Popup Menu              | FUIPopupMenuTheme      | components/popupmenu/fui\_popupmenu\_theme.dart           |
| Sections                | FUISectionTheme        | components/section/fui\_section\_theme.dart               |
| Spinner                 | FUISpinnerTheme        | components/spinner/fui\_spinner\_theme.dart               |
| Tabs                    | FUITabTheme            | components/tab/fui\_tab\_theme.dart                       |
| Timeline                | FUITimelineTileTheme   | components/timeline/fui\_timeline\_theme.dart             |
| Tooltip                 | FUITooltipTheme        | components/tooltip/fui\_tooltip\_theme.dart               |
| Text - Code Display Box | FUICodeDisplayBoxTheme | components/typography/fui\_code\_display\_box\_theme.dart |
| Text - Quote            | FUIQuoteTheme          | components/typography/fui\_quote\_theme.dart              |
| Text Pill               | FUITextPillTheme       | components/typography/fui\_text\_pill\_theme.dart         |
| Typography              | FUITypographyTheme     | components/typography/fui\_typography\_theme.dart         |
| Wizard                  | FUIWizardTheme         | components/wizard/fui\_wizard\_theme.dart                 |
