# FUITabItem

### Tab Item Head With Label & Icon

You may include an icon on either the left or right of the tab item head label, as follows:

```dart
FUITabItem(
  key: UniqueKey(),
  tabHeadLabel: Text('Tab 1'),
  tabHeadIcon: Icon(CupertinoIcons.check_mark),
  content: ...
);
```

**To change the position of the icon**

The position of the icon or label can be modified by defining the `fuiTabHeadSideIconPosition` value.

```dart
FUITabItem(
  key: UniqueKey(),
  tabHeadLabel: Text('Tab 1'),
  tabHeadIcon: Icon(CupertinoIcons.check_mark),
  fuiTabHeadSideIconPosition: FUITabHeadTextIconPosition.iconLeftTextRight, // Do explore more.
  content: ...
);
```
