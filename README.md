StylableDateTimePicker
======================

A stylable version of the date/time picker for Android 4.0+

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
</style>
```

Create the DatePicker/TimePicker with

```java
DatePickerDialog dialog = DatePickerDialog.newInstance(callBack, year, monthOfYear, dayOfMonth, R.style.DateTimePicker);
```
