# vue2-datepicker

> A Datepicker Component For Vue2

## Demo
<https://mengxiong10.github.io/vue2-datepicker/>

![image](https://github.com/mengxiong10/vue2-datepicker/raw/master/screenshot/demo.PNG)

## Install

```bash
$ npm install vue2-datepicker --save
```

## Usage

```html
<script>
import DatePicker from 'vue2-datepicker'

export default {
  components: { DatePicker },
  data() {
    return {
      time1: '',
      time2: '',
      shortcuts: [
        {
          text: 'Today',
          start: new Date(),
          end: new Date()
        }
      ]
    }
  }
}
</script>

<template>
  <div>
    <date-picker v-model="time1"></date-picker>
    <date-picker v-model="time2" range :shortcuts="shortcuts"></date-picker>
  </div>
</template>
```
## Attributes

| Prop            | Type          | Default     | Description                                       |
|-----------------|---------------|-------------|---------------------------------------------------|
| range           | Boolean       | false       | if true, the type is daterange                    |
| format          | String        | yyyy-MM-dd  | Date formatting string                            |
| lang            | String        | zh          | Translation (en/zh/es)                            |
| placeholder     | String        |             | input placeholder text                            |
| width           | String/Number | 210         | input size                                        |
| disabledDays    | Array         | []          | Days in YYYY-MM-DD format to disable              |
| showYearNav     | Boolean       | true        | Show the year nav in the calendar                 |
| notBefore       | String        | ''          | Disable all dates before date in YYY-MM-DD format |
| notAfter        | String        | ''          | Disable all dates after date in YYY-MM-DD format  |
| shortcuts       | Boolean/Array | true        | the shortcuts for the range picker                |

## shortcuts
* true -      show the default shortcuts
* false -     hide the shortcuts
* Object[] -  custom shortcuts, [{text, start, end}]

| Prop            | Type          |  Description           |
|-----------------|---------------|------------------------|
| text            | String        | Text                   |
| start           | Date          | Start Date             |
| end             | Date          | End Date               |



