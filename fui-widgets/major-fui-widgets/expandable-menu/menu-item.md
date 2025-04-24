# Menu Item

The `FUIMenuItem` class represents the menu item type for the expandable menu `FUIExpMenu`.

### Usage

#### Typical usage

```dart
FUIMenuItem(
    label: Text('Item 1'),
    onPressed: () { // Do something... },
    selected: true, // Set for initial selection
    fuiSubMenuItems: [
        // Sub Menu Items here...
    ],
);
```

#### With icon

```dart
FUIMenuItem(
    label: Text('Item 1'),
    icon: const Icon(LineAwesome.chart_bar),
    onPressed: () { // Do something... },
    fuiSubMenuItems: [
        // Sub Menu Items here...
    ],
);
```

> Note: icon will always be on the left side of the label.

#### Change of color scheme (for selected)

```dart
FUIMenuItem(
    fuiColorScheme: FUIColorScheme.cobalt,
    label: Text('Item 1'),
    onPressed: () { // Do something... },
    fuiSubMenuItems: [
        // Sub Menu Items here...
    ],
);
```

#### With different selected label & icon

```dart
FUIMenuItem(
    label: Text('Item 1'),
    icon: Icon(LineAwesome.chart_bar),
    selectedLabel: Text('Item 1 Selected'),
    selectedIcon: Icon(LineAwesome.check_solid),
    onPressed: () { // Do something... },
    fuiSubMenuItems: [
        // Sub Menu Items here...
    ],
);
```
