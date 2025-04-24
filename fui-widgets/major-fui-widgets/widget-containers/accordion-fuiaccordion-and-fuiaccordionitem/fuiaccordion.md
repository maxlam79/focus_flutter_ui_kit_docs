# FUIAccordion

### Usage

Below is a typical usage example demonstrating the functionality of `FUIAccordion` and `FUIAccordionItem`:

> IMPORTANT NOTE: each `FUIAccordionItem` has a default `UniqueKey`.\
> For more control (with the controller) you may assign a `Key`\
> to all `FUIAccordionItem` - a `ValueKey('someTabId')` will do the job.

```dart
@override
Widget build(BuildContext context) {
    Key itemKey1 = ValueKey('item1');
    Key itemKey2 = ValueKey('item2');
    Key itemKey3 = ValueKey('item3');
    
    List<FUIAccordionItem> accordionItemList = [
      FUIAccordionItem(
        key: itemKey1,
        headLabel: Text('Accordion 1'),
        fuiAccordionHeadSideIconPosition: FUIAccordionHeadTextIconPosition.iconRightTextLeft,
        content: FUIColumn(
          children: [
            Regular(Text('Content for accordion 1')),
          ],
        ),
      ),
      FUIAccordionItem(
        key: itemKey2,
        headLabel: Text('Accordion 2'),
        content: FUIColumn(
          children: [
            Regular(Text('Content for accordion 2')),
          ],
        ),
      ),
      FUIAccordionItem(
        key: itemKey3,
        headLabel: Text('Accordion 3'),
        content: FUIColumn(
          children: [
            Regular(Text('Contents for accordion 3')),
          ],
        ),
      ),
    ];
    
    return FUIColumn(
      children: [
        FUIAccordion(
          fuiAccordionItems: accordionItemList,
        ),
      ],
    );
}
```

#### Expanding accordion items via controller

To externally control the expansion of accordion items, you can attach a `FUIAccordionController` to the `FUIAccordion`.

Example:

```dart
FUIAccordionController ctrl = FUIAccordionController();

FUIAccordion(
  fuiAccordionController: ctrl,
  fuiAccordionItems: accordionItemList,
);
```

**Expanding an accordion item**

Example: to expand item1:

```dart
ctrl.trigger(FUIAccordionEvent(
  itemKey: itemKey1,
  expand: true,
));
```

**Collapsing an accordion item**

Example: to collapse item1:

```dart
ctrl.trigger(FUIAccordionEvent(
  itemKey: itemKey1,
  expand: false,
));
```

### Parameters

| Parameters                                     | Description                                                                      |
| ---------------------------------------------- | -------------------------------------------------------------------------------- |
| FUIAccordionController? fuiAccordionController | The accordion controller for expanding or collapsing the desired accordion item. |
| List\<FUIAccordionItem> fuiAccordionItems      | The accordion items. The widget has to be of class `FUIAccordionItem`.           |
