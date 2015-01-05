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

## Installation
At the moment you have to install the library "by hand" (I will release it for using with gradle soon):

copy the library to your "libs" folder. Then include the following line in your "settings.gradle":

```gradle
include ':libs:datetimepicker'
```
then add the following lines to your "build.gradle":

```gradle
repositories {
    mavenCentral()
    flatDir {            <--- add this
        dirs 'libs'      <---
    }                    <---
}

dependencies {
    compile project(':libs:datetimepicker')  <-- add this line
...
```

## License

    Copyright 2014 Artjom König

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at
    
       http://www.apache.org/licenses/LICENSE-2.0
    
    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
