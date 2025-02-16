---
category: Components
type: Feedback
title: Drawer
---

A panel which slides in from the edge of the screen.

## When To Use

A Drawer is a panel that is typically overlaid on top of a page and slides in from the side. 
It contains a set of information or actions.  
Since the user can interact with the Drawer without leaving the current page,
 tasks can be achieved more efficiently within thesame context.

- Use a Form to create or edit a set of information.
- Processing subtasks. When subtasks are too heavy for a Popover and we still want to keep the subtasks in the context of the main task, 
Drawer comes very handy.
- When the same Form is needed in multiple places.

## API

### Drawer

| Property | Description | Type | Default Value |
| --- | --- | --- | --- |
| Title            | the title for drawer         | string or slot | -         |
| BodyStyle | Style of the drawer content part                               | object        | -         |
| Closable            | Whether a close (x) button is visible on top right of the Drawer dialog or not.           | boolean | true         |
| ChildContent | Subcomponent                                 | object        | -         |
| MaskClosable              | Clicking on the mask (area outside the Drawer) to close the Drawer or not.         | boolean        | true        |
| MaskStyle | Style for Drawer's mask element.                               | object        | -         |
| Placement | The placement of the Drawer, option could be `left` , `top`,`right`,`bottom`        | string  | `right`         |
| WrapClassName | The class name of the container of the Drawer dialog.                               | string        | -         |
| Width | 	Width of the Drawer dialog.                               | |int        | 256         |
| Height | placement is top or bottom, height of the Drawer dialog.                               | int        | 256        |
| ZIndex | 	The z-index of the Drawer.                              | int        | -         |
| OffsetX | the offset of in X-axis                                 | int        | 0         |
| OffsetY |  the offset of in Y-axis                                | int        | 0         |
| Visible | Whether the Drawer dialog is visible or not.                               | boolean        | -         |
| Keyboard | Whether support press esc to close                          | boolean        | true         |
| OnClose        |Specify a callback that will be called when a user clicks mask, close button or Cancel button.                                   | function(e)     | -         |
| OnViewInit             | Specify a callback that will be called before drawer displayed | function(e)        | - |

### DrawerService

| 方法名 | 说明                  | 参数                       | 返回             |
| ------ | --------------------- | -------------------------- | ---------------- |
| CreateAsync | create and open an Drawer  | `DrawerConfig`  | `DrawerRef` |
| CreateAsync | create and open an Drawer  | `DrawerConfig` , TContentParams  | `DrawerRef<R>` |

### DrawerConfig

| 参数                | 说明                                                                                                                 | 类型                                                                | 默认值    |
| ------------------- | -------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- | --------- |
| Content           | The drawer body content.                                                                                                | `OneOf<RenderFragment, string>`       | -         |
| ContentParams     | The component inputs the param / The Template context.                                                                            | `D`                                                                 | -         |
| OnCancel          | Execute when click on the mask or the upper cancel button (return false to prevent closing)    | -         |
| Closable          | Whether a close (x) button is visible on top right of the Drawer dialog or not.              | `boolean`                                                           | `true`    |
| MaskClosable      | Clicking on the mask (area outside the Drawer) to close the Drawer or not.                                                                                            | `boolean`                                                           | `true`    |
| Mask              | Whether to show mask or not.                         | `boolean`                                                           | `true`    |
| CloseOnNavigation | Whether to close the drawer when the navigation history changes           | `boolean`                                                           | `true`    |
| Keyboard          | 是否支持键盘esc关闭                                                                                                  | `boolean`                                                           | `true`    |
| MaskStyle         | Style for Drawer's mask element.                     | `string`                                                            | `{}`      |
| BodyStyle         |  Body style for modal body element. Such as height, padding etc.                          | `string`                                                            | `{}`      |
| Title             | The title for Drawer.                                                    | `OneOf<RenderFragment, string>`                                       | -         |
| Width             | Width of the Drawer dialog.                            | `int`                                                  | `256`     |
| Height            | Height of the Drawer dialog, only when placement is `'top'` or `'bottom'`.                | `int`                                                  | `256`     |
| WrapClassName     | The class name of the container of the Drawer dialog.               | `string`                                                            | -         |
| ZIndex            |  The `z-index` of the Drawer.                      | `int`                                                            | `1000`    |
| Placement         |  The placement of the Drawer.                                   | `'top' \| 'right' \| 'bottom' \| 'left'`                            | `'right'` |
| OffsetX           |  The the X coordinate offset(px).                     | `int`                                                            | `0`       |
| OffsetY           | The the Y coordinate offset(px), only when placement is `'top'` or `'bottom'`.    | `int`                                                            | `0`       |

### DrawerRef

| 名称  | 说明        | 类型                   |
| ----- | ----------- | ---------------------- |
| CloseAsync | close the drawer. | `` |
| OpenAsync  | open the drawer. | ``           |