# ant-design

1. 프로그램 설치

```javascript
//1.
create-react-app@5.0.0 my-doc
//2.
cd my-doc
//3.
npm i antd
```

2. setting

```javascript
// index.js 파일에서
import React from "react";
import ReactDOM from "react-dom";
//import "antd/dist/antd.css";입력
import "antd/dist/antd.css";
// 아래 index.css위에 입력
import "./index.css";
import App from "./App";
import reportWebVitals from "./reportWebVitals";
```

3. 사용법1 - 필요한것만 찾아서 붙여넣기.

```javascript
import

import { DatePicker } from "antd";
import 'antd/es/date-picker/style/css';

function App() {
  return (
    <div className="App">
      <header className="App-header">
        <img src={logo} className="App-logo" alt="logo" />
        <p>
          Edit <code>src/App.js</code> and save to reload.
        </p>
        <DatePicker />
      </header>
    </div>
  );
}
```

3. 사용법2 -babel의 플러그인을 사용

```javascript

npm run eject
npm install babel-plugin-import --save-dev

```

4. 그외

```javascript
import {Row, Col} from 'antd';

const colStyle = () => ({
  height: 50,
  backgroundColor: 'red',
  opacity: Math.round(Math.random() * 10) / 10,
});

function App() {
  return(
    <div className="App">
      <Row
        // type="flex" => 생략가능
        justify="좌우정렬";
        // start|center|end|space-between|space-around

        align="위아래정렬";
        // top|middle|bottom
      >
      // 컬럼당 span의 수는 24여야 한다. 12 *2 = 24
      // <Col span={24 중에 어느정도 차지할 지 정수}>
        <Col span={12} style={colStyle()}>
        <Col span={12} style={colStyle()}>
      </Row>
      <Row gutter={16}>
      // gutter={16 + 8n 의 정수} *px임 최소한으로 16은 줘야한다.
        <Col span={8} style={colStyle()}>
        <Col span={8} style={colStyle()}>
        <Col span={8} style={colStyle()}>
      </Row>
      <Row>
      // <Col offset = {} ={24중 건너띄고 싶은 정수} >
        <Col span={6} offset={?} style={colStyle()}>
        <Col span={6} style={colStyle()}>
        <Col span={6} style={colStyle()}>
        <Col span={6} style={colStyle()}>
      </Row>
    </div>
  );
}

export default App;
}
```
