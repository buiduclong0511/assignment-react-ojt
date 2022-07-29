---
#### Câu 1: Một trong các ưu điêm của React là gì?
- A: Không có lợi ích gì
- B: Tạo được các component có tính tái sử dụng
- C: Dễ dàng tối ưu SEO
---
#### Câu 2: React sử dụng cái gì để mô tả cấu trúc trang Web?
- A: Native component
- B: HTML
- C: JSX
---
#### Câu 3: Điền vào chỗ trống method thích hợp để tạo 1 React element.
```js
import React from 'react'

const reactElement = React.___________('div')
```
- A: `createElement`
- B: `createComponent`
- C: `appendChild`
---
#### Câu 4: Cho sẵn component `PostItem`, cách sử dụng nào trong 2 cách sau đây là đúng?
```js
function PostItem() {
    return (
        <div>
            <h2>Title</h2>
            <p>Description</p>
        </div>
    )
}

// Cách 1
function ProductsList() {
    return (
        <>
            <PostItem />
            <PostItem />
            <PostItem />
        </>
    )
}

// Cách 2
function ProductsList() {
    return (
        <>
            <PostItem></PostItem>
            <PostItem></PostItem>
            <PostItem></PostItem>
        </>
    )
}
```
- A: Cách 1
- B: Cách 2
- C: Cả 2 cách
---
#### Câu 5: Props là gì?
- A: Props có thể coi là đầu ra của Component và được sử dụng để trả về kết quả của Component 
- B: Props có thể coi là đối số của Component và được sử dụng để nhận dữ liệu từ bên ngoài vào
- C: Props có thể coi là tên của Component và được sử dụng để định danh cho Component
---
#### Câu 6: Trong ReactJS, một component có thể nhận vào bao nhiêu props?
- A: Một component chỉ có thể nhận vào 1 props
- B: Một component có thể nhận vào 1 số lượng props nhất định tùy vào việc chúng ta định nghĩa nó như thế nào
- C: Một component có thể nhận vào vô số props
---
#### Câu 7: Trong ReactJS, props sẽ hợp lệ khi được nhận các kiểu dữ liệu nào?
- A: Chuỗi
- B: Tất cả các kiểu dữ liệu có trong JavaScript
- C: Tất cả các kiểu dữ liệu ngoại trừ các kiểu dữ liệu tham chiếu (object, array, function)
---
#### Câu 8: Để sử dụng được JavaScript trong JSX, chúng ta sử dụng cặp ngoặc nào?
- A: `{}`
- B: `[]`
- C: Chỉ cần viết code JS vào là chạy được
---
#### Câu 9: Style inline trong JSX được viết dưới dạng nào?
- A: Object
- B: Chuỗi
- C: Array
---
#### Câu 10: Điền vào chỗ trống cú pháp hợp lý để chữ trong thẻ `p` có màu `#f00`.
```js
function Paragraph() {
    return <p style=___________>This is a paragraph</p>
}
```
- A: `{{ color: #f00 }}`
- B: `{{ color: '#f00' }}`
- C: `{{{ color: '#f00' }}}`
---
#### Câu 11: Hãy dự đoán nội dung của đoạn `console.log` sau đây.
```js
function Paragraph({ key, children }) {
    console.log('Key: ', key)

    return <p>{children}</p>
}

function App() {
    return <Paragraph key={1}>This is a paragraph</Paragraph>
}
```
- A: `Key: 1`
- B: `Key: undefined`
- C: `Key: null`
---
#### Câu 12: Component `Lock` trả về chuỗi JSX như nào?
```js
function Lock({ key }) {
    const hasKey = !!key

    if (hasKey) {
        return <p>Lock is opened!</p>
    }

    return <p>Lock is locked!</p>
}

function App() {
    return <Lock key="0" />
}
```
- A: `<p>Lock is opened!</p>`
- B: `<p>Lock is locked!</p>`
- C: `null`
---
#### Câu 13: Component `Paragraph` trả về chuỗi JSX như nào?
```js
function Paragraph({ children }) {
    const hasChildren = !!children

    return hasChildren ? <p>{children}</p> : <p>Children is not found</p>
}

function App() {
    return <Paragraph children="This is paragraph" />
}
```
- A: `<p>This is paragraph</p>`
- B: `<p>Children is not found</p>`
- C: `null`
---
#### Câu 14: `useState` dùng để làm gì?
- A: Tạo ra 1 biến không thể bị thay đổi theo thời gian
- B: Tạo ra 1 biến chỉ để lưu dữ liệu của response trả về khi gọi API
- C: Tạo ra 1 biến thể hiện trạng thái của component
---
#### Câu 15: Khi thay đổi giá trị của state thì component sẽ như thế nào? 
- A: Component sẽ render lại
- B: Component không được render lại
- C: Giá trị của state sẽ không thể bị thay đổi
---
#### Câu 16: Các lệnh `console.log` sau đây sẽ in ra theo thứ tự nào?
```js
function App() {
    useEffect(() => {
        console.log('Hi')
    }, [])

    return (
        <div>
            {console.log('Hello')} 
            <h1>Hello world</h1>
        </div>
    )
}

const root = ReactDOM.createRoot(document.getElementById('root'))

root.render(<App />)
```
- A: `Hi`, `Hello`, `Hi`
- B: `Hi`, `Hello`
- C: `Hello`, `Hi`
---
#### Câu 17: Các lệnh `console.log` sau đây sẽ in ra theo thứ tự nào?
```js
function App() {
    useEffect(() => {
        console.log('Hi')

        return () => console.log('Goodbye')
    }, [])

    return (
        <div>
            {console.log('Hello')}
            <h1>Hello world</h1>
        </div>
    )
}

const root = ReactDOM.createRoot(document.getElementById('root'))

root.render(<App />)
```
- A: `Hi`, `Hello`, `Goodbye`
- B: `Hello`, `Hi`, `Goodbye`
- C: `Hello`, `Hi`
---
#### Câu 18: Các lệnh `console.log` sau đây sẽ in ra theo thứ tự nào?
```js
function App() {
    const [state, setState] = useState(0)

    useEffect(() => {
        setState(1)
    }, [])

    useEffect(() => {
        console.log('Hi')

        return () => console.log('Goodbye')
    }, [state])

    return (
        <div>
            <h1>Hello world</h1>
        </div>
    )
}

const root = ReactDOM.createRoot(document.getElementById('root'))

root.render(<App />)
```
- A: `Hi`, `Goodbye`, `Hi`
- B: `Hi`, `Hi`, `Goodbye`
- C: `Hi`, `Goodbye`
---
#### Câu 19: Các lệnh `console.log` sau đây sẽ in ra theo thứ tự nào?
```js
function App() {
    const [state, setState] = useState(0)

    useEffect(() => {
        setState(1)
    }, [])

    useEffect(() => {
        console.log('Hi')

        return () => console.log('Goodbye')
    }, [state])

    return (
        <div>
            {consol.log('Hello')}
            <h1>Hello world</h1>
        </div>
    )
}

const root = ReactDOM.createRoot(document.getElementById('root'))

root.render(<App />)
```
- A: `Hello`, `Hi`, `Goodbye`, `Hello`, `Hi`
- B: `Hello`, `Hi`, `Hello`, `Goodbye`, `Hi`
- C: `Hi`, `Goodbye`, `Hello`
---
#### Câu 20: Lệnh `console.log` sau đây sẽ in ra giá trị bao nhiêu?
```js
function Add() {
    const [state, setState] = useState(0)

    let variable = 10

    console.log(`${state} ${variable}`)

    variable = 11;

    useEffect(() => {
        setState(1)
    }, [])

    return <div>Hello world</div>
}

const root = ReactDOM.createRoot(document.getElementById('root'))

root.render(<App />)
```
- A: `0 10`, `1 11`
- B: `0 10`, `1 10`
- C: `0 10`, `0 11`
---
#### Câu 21: Lệnh `console.log` sau đây sẽ in ra giá trị bao nhiêu?
```js
function Add() {
    const [state, setState] = useState(0)

    const variable = useRef(10)

    console.log(`${state} ${variable.current}`)

    variable.current = 11

    useEffect(() => {
        setState(1)
    }, [])

    return <div>Hello world</div>
}

const root = ReactDOM.createRoot(document.getElementById('root'))

root.render(<App />)
```
- A: `0 10`, `1 11`
- B: `0 10`, `1 10`
- C: `0 10`, `0 11`
---
#### Câu 22: Lệnh `console.log` sau đây sẽ in ra giá trị bao nhiêu?
```js
function Add() {
    let [state, setState] = useState(0);

    let variable = 10;

    console.log(`${state} ${variable}`);

    variable = 11;

    useEffect(() => {
        state = 1;
    }, []);

    return <div>Hello world</div>;
}

const root = ReactDOM.createRoot(document.getElementById('root'))

root.render(<App />)
```
- A: `0 10`
- B: `0 10`, `1 10`
- C: `0 10`, `0 10`

---
#### Câu 23: Phát biểu nào sau đây là **sai**?
- A: Redux là một mô hình quản lý dữ liệu
- B: Redux-toolkit và React-redux chỉ được sử dụng trong ứng dụng React
- C: Redux có thể được sử dụng trong bất kỳ 1 ứng dụng nào được viết bởi JavaScript

---
#### Câu 24: Trong các thành phần sau đây, đâu là những thành phần có trong Redux?
 - A: Reducer, State, Ref, Store, Actions
 - B: Reducer, State, Middleware, Store, Actions
 - C: Reducer, Style, Middleware, Store, Actions

 ---
#### Câu 25: `combineReducers` dùng để làm gì?
- A: Gom các reducer nhỏ thành 1 reducer duy nhất (Root reducer)
- B: Gom các store nhỏ thành 1 store duy nhất
- C: Tách reducer lơn thành các reducer nhỏ

---
#### Câu 26: Điền vào chỗ trống từ khóa thích hợp?
```js
const reducer = (state = { value: 0 }, action) => {
    switch(action.___________) {
        case 'increment':
            return { value: state.value + 1 }
        case 'decrement':
            return { value: state.value - 1 }
        default:
            return state
    }
}
```
- A: `payload`
- B: `type`
- C: `typical`

---
#### Câu 27: Điền vào chỗ trống từ khóa thích hợp?
```js
const counterSlice = createSlice({
    name: 'counter',
    initialState: {
        value: 0
    },
    ___________: {
        increment: (state) => {
            state.value += 1
        },
        decrement: (state) => {
            state.value -= 1
        },
    },
    ___________: (builder) => {
        builder.addCase(asyncIncrement.fulfilled, (state) => {
            state.value += 1
        })
    }
})
```
- A: `actions`, `asyncActions`
- B: `reducers`, `asyncReducers`
- C: `reducers`, `extraReducers`

---
#### Câu 28: Action được thể hiện dưới dạng như nào?
- A: 1 plain object với các key là `type` (required) và `payload` (optional)
- B: 1 plain object với các key là `type` (required) và `payload` (required)
- C: 1 plain object với các key là `type` (optional) và `payload` (optional)

---
#### Câu 29: `Async action` là gì?
- A: Là 1 action có khả năng xử lý các tác vụ bất đồng bộ
- B: Là 1 action có khả năng trả về 1 `plain object`
- C: Là 1 action có `type` và `payload`

---
#### Câu 30: Flow của redux là gì?
- A: Dispatch action -> Reducer nhận vào action -> Reducer phân loại action và thay đổi state -> Cập nhật state mới trên view
- B: Dispatch action -> Reducer nhận vào action -> Reducer phần lại action và thay đổi state
- C: Reducer nhận vào action -> Dispatch action -> Reducer thay đổi state -> Cập nhật state mới trên view

---
#### Câu 31: Thư viện `Redux persist` dùng để làm gì?
- A: Lưu state của redux vào cookie
- B: Lưu state của redux vào session
- C: Lưu state của redux vào local storage