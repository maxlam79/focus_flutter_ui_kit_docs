# FUITabPane

Usage

Here's a typical usage example for `FUITab` and `FUITabItem`:

> IMPORTANT NOTE: each `FUITabItem` has a default `UniqueKey`.\
> For more control (with the controller) you may assign a `Key`\
> to all `FUITabItem` - a `ValueKey('someTabId')` will do the job.

```dart
var tab1Key = ValueKey('tab1');
var tab2Key = ValueKey('tab2');
var tab3Key = ValueKey('tab3');

FUITabPane(
  fuiTabItems: [
    FUITabItem(
      key: tab1Key,
      tabHeadLabel: Text('Tab 1'),
      content: Center(
        child: H2(
          Text('This is tab1 content'),
          alignment: Alignment.center,
        ),
      ),
    ),
    FUITabItem(
      key: tab2Key,
      tabHeadLabel: Text('Tab 2'),
      content: Center(
        child: H2(
          Text('This is tab2 content'),
          alignment: Alignment.center,
        ),
      ),
    ),
    FUITabItem(
      key: tab3Key,
      tabHeadLabel: Text('Tab 3'),
      content: Center(
        child: H2(
          Text('This is tab3 content'),
          alignment: Alignment.center,
        ),
      ),
    ),
  ],
);
```

The `FUITabPane` by default has a maximum height of `300`. Kindly modify the height setting to align with your specific\
requirements. An unbounded height may result in unpredictable outcomes.

#### Changing the position of the tabs head

The position of the tab items head could be changed via `fuiTabHeadPosition`:

```dart
FUITabPane(
    fuiTabHeadPosition: FUITabHeadPosition.bottomRight,
    fuiTabItems: [...],
);            
```

#### Changing the tab head label alignment

By default, the item head label is positioned at the center. Alignment can be customized as follows:

```dart
FUITabPane(
    fuiTabHeadLabelAlignment: FUITabHeadLabelAlignment.right,
    fuiTabItems: [...],
);  
```

### Content Display Animation

The `FUITabPane` natively supports a range of animation types when tab content is switched and displayed. The default\
animation type is a fade-in effect.

Please refer to the `FUIAnimationType` enum for further details.

```
lib/focus_ui_kit/animation/fui_animator_helper.dart
```

#### To change the animation type and duration for content display

```dart
FUITabPane(
    contentDisplayAniType: FUIAnimationType.bounceIn,
    contentDisplayAniDuration: Duration(milliseconds: 300),
    fuiTabItems: [...],
);
```

#### Callback after tab content display and after animation rendered

If necessary, the `FUITabPane` could execute a callback once the animation of the content display is rendered.

```dart
FUITabPane(
    onContentDisplayAniRendered: (_key) {
        print('Tab item with key: ${_key.toString()} has finished rendering.');
    },
    fuiTabItems: [...],
);
```

### With controller

Programmatic control of tab item switching is possible.

#### Initialize the `FUITabPaneController`

Do this in a Stateful Widget.

```dart
late FUITabPaneController tabPaneCtrl;

@override
void initState() {
    super.initState();
    tabPaneCtrl = FUITabPaneController();
}

@override
void dispose() {
    tabPaneCtrl.close();
    super.dispose();
}
```

#### Switching tabs via controller

```dart
// Assuming tab1Key is already defined and has been set to one of the FUITabItem.

tabPaneCtrl.trigger(
    FUITabPaneEvent(selectedTabItemKey: tab1Key),
);
```

### Parameters

| Parameters                                        | Description                                                                                                               |
| ------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| List\<FUITabItem> fuiTabItems                     | The list of tab item widgets.                                                                                             |
| FUITabPaneController? fuiTabPaneController        | The tab pane controller for switching tabs programmatically.                                                              |
| FUITabHeadPosition fuiTabHeadPosition             | The position of the tab head where the label is displayed. It can be configured with values from `FUITabHeadPosition`.    |
| FUITabHeadLabelAlignment fuiTabHeadLabelAlignment | The alignment of the tab head label - left, center, right. Can be configures with values from `FUITabHeadLabelAlignment`. |
| FUIAnimationType? contentDisplayAniType           | The animation type for displaying tab content when switched. For no animation, just set to `Null`.                        |
| Duration? contentDisplayAniDuration               | The animation duration for displaying content when switching.                                                             |
