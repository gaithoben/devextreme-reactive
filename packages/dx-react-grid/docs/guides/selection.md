# React Grid Row Selection

## Introduction

Grid allows users to select/deselect rows. It seamlessly integrates with paging, sorting, filtering and grouping.

## Plugin List

There are several plugins that implement selection. Here is the list:
- [SelectionState](../reference/selection-state.md)
- [TableSelection](../reference/table-selection.md)

Note that [plugin order](../README.md#plugin-order) is very important.

## Basic setup

The following example demonstrates the basic Grid selection setup:

.embedded-demo(selection/basic)

As you can see, in this example we use controlled mode by specifying the `selection` and `onSelectionChange` options for the `SelectionState` plugin.

## Select by Row Click

By default, rows can be selected by ticking a check box. In some cases, it may be convenient to allow users to select rows by clicking on the whole item. The following example demonstrates this scenario:

.embedded-demo(selection/select-by-row-click)

In some scenarios, it is useful to hide check boxes completely and highlight selected rows. Here is a demo:

.embedded-demo(selection/hidden-checkboxes)

## Select All

If your Grid configuration has the `TableHeaderRow` plugin, you can see a check box inside a header row. This check box provides a capability to select/deselect all rows.

### Without Paging

In the following example, we are using TableView with virtual mode. It allow us to demonstrate the Select All behavior with multiple rows:

.embedded-demo(selection/select-all-virtual)

### With Paging

If you are using the `LocalPaging` plugin, it is easy to integrate the Select All behavior with the `PagingState` plugin.

In the following example, we have implemented the Select All behavior within a visible page. You can achieve this result by placing the `SelectionState` plugin after `LocalPaging`:

.embedded-demo(selection/select-all-by-page)

If you place the `SelectionState` plugin before `LocalPaging`, it will be possible to select rows on all pages:

.embedded-demo(selection/select-all-by-all-pages)

### Hidden Select All

It is also possible to hide the Select All check box:

.embedded-demo(selection/hidden-select-all)
