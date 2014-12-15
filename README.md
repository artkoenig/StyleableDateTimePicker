StylableDateTimePicker
======================

A styleable version of the date/time picker for Android 4.0+ with embedding support (using as normal fragment)

![Styled DatePicker](/../screenshots/screenshots/screenshot.png?raw=true "Example Theme")

Declare your style:

```java
<style name="DateTimePicker">
    <item name="headerBackgroundColor">...</item>
    <item name="hightlightedTextColor">...</item>
    <item name="buttonBackground">...</item>
    <item name="buttonTextColor">...</item>
    <item name="circleHighlightColor">...</item>
    <item name="defaultTextColor">...</item>
    <item name="selectedDayTextSize">...</item>
    <item name="selectedMonthTextSize">...</item>
    <item name="selectedYearTextSize">...</item>
</style>
```

Create the DatePicker/TimePicker with

```java
DatePickerDialog dialog = DatePickerDialog.newInstance(callBack, year, monthOfYear, dayOfMonth, R.style.DateTimePicker);
```
You can also add the pickers as content in your view hierarchy:

```java
DatePickerDialog picker = DatePickerDialog.newInstance(...);
FragmentTransaction ft = getFragmentManager().beginTransaction();
ft.add(R.id.picker_wrapper, picker);
ft.commit();
```
