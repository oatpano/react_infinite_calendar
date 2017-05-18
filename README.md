**วิธีติดตั้ง React Infinite Calendar(เริ่มจาก Repo อันนี้)**
=============================


**1. Clone repository นี้**
[https://github.com/oatpano/react_infinite_calendar.git](https://github.com/oatpano/react_infinite_calendar.git)

**2. เมื่อ clone เสร็จแล้ว**
พิมพ์คำสั่ง
```sh
npm install
```

**3. สั่งให้แสดงผลบน Browser**

```sh
npm start
```





**วิธีติดตั้ง React Infinite Calendar(เริ่มจาก0)**
=============================


**1.สร้างโปรเจ็ค React native**

```sh
create-react-app app-name
```


**2.เพิ่ม dependency**

มี dependency 2 อันนี้ และให้บันทึกลง package.json ด้วย --save

```sh
npm install react-infinite-calendar react-transition-group@1.1.1 --save
```


**3.แก้ไขไฟล์ index.js ตามนี้**
```js
import React from 'react'
import ReactDOM from 'react-dom'
import './index.css'
import InfiniteCalendar from 'react-infinite-calendar';
import 'react-infinite-calendar/styles.css'; // Make sure to import the default stylesheet

// Render the Calendar
var today = new Date();
var lastWeek = new Date(today.getFullYear(), today.getMonth(), today.getDate() - 7);

ReactDOM.render(
  <InfiniteCalendar
    width={400}
    height={600}
    selected={today}
    disabledDays={[0,6]}
    minDate={lastWeek}
  />,
  document.getElementById('root')
)
```


**4.สั่งคำสั่งรันบน Browser**

```sh
npm start
```



**อ้างอิง**

github: [https://github.com/clauderic/react-infinite-calendar](https://github.com/clauderic/react-infinite-calendar)

fix: [https://www.npmjs.com/package/react-addons-css-transition-group](https://github.com/clauderic/react-infinite-calendar)