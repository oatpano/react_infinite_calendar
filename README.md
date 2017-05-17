**วิธีติดตั้ง React Infinite Calendar**
=============================


<B>**1.สร้างโปรเจ็ค React native**</B>

```
create-react-app app-name
```


<B>**2.เพิ่ม dependency**</B>

มี dependency 2 อันนี้ และให้บันทึกลง package.json ด้วย --save
```
npm install react-infinite-calendar react-transition-group@1.1.1 --save
```


<B>**3.แก้ไขไฟล์ index.js ตามนี้**</B>
```
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


<B>**4.สั่งคำสั่งรันบน Browser**</B>
```
npm start
```


<B>**อ้างอิง**</B>

github: [https://github.com/clauderic/react-infinite-calendar](https://github.com/clauderic/react-infinite-calendar)

fix: [https://www.npmjs.com/package/react-addons-css-transition-group](https://github.com/clauderic/react-infinite-calendar)