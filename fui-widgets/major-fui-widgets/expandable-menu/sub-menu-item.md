# Sub-Menu Item

The submenu item widget class is named `FUISubMenuItem`. This widget is responsible for defining the submenu items within the main menu item.

### Usage

#### Typical usage

```dart
FUISubMenuItem(
    label: Text('Sub Item 1'),
    selected: true, // For initial selection
    onPressed: () { // Do something... },
);
```

#### With icon

```dart
FUISubMenuItem(
    label: Text('Sub Item 1'),
    icon: const Icon(LineAwesome.chart_bar),
    onPressed: () { // Do something... },
);
```

> Note: icon will always be on the left side of the label.

#### Change of color scheme (for selected)

```dart
FUISubMenuItem(
    fuiColorScheme: FUIColorScheme.cobalt,
    label: Text('Sub Item 1'),
    onPressed: () { // Do something... },
);
```

#### With different selected label & icon

```dart
FUISubMenuItem(
    label: Text('Sub Item 1'),
    icon: Icon(LineAwesome.chart_bar),
    selectedLabel: Text('Sub Item 1 Selected'),
    selectedIcon: Icon(LineAwesome.check_solid),
    onPressed: () { // Do something... },
);
```
