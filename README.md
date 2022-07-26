## Assignment React OJT
<br />

---
<br />

#### Câu 1: Một trong các ưu điêm của React là gì?
- A: Không có lợi ích gì
- B: Tạo được các component có tính tái sử dụng
- C: Dễ dàng tối ưu SEO

<br />

---
<br />

#### Câu 2: React sử dụng cái gì để mô tả cấu trúc trang Web?
- A: Native component
- B: HTML
- C: JSX

<br />

---
<br />

#### Câu 3: Điền vào chỗ trống method thích hợp để tạo 1 React element.
```js
import React from 'react'

const reactElement = React.___________('div')
```
- A: `createElement`
- B: `createComponent`
- C: `appendChild`

<br />

---
<br />

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

<br />

---
<br />

#### Câu 5: Props là gì?
- A: Props có thể coi là đầu ra của Component và được sử dụng để trả về kết quả của Component 
- B: Props có thể coi là đối số của Component và được sử dụng để nhận dữ liệu từ bên ngoài vào
- C: Props có thể coi là tên của Component và được sử dụng để định danh cho Component

<br />

---
<br />

#### Câu 6: Một component có thể nhận vào bao nhiêu props?
- A: Một component chỉ có thể nhận vào 1 props
- B: Một component có thể nhận vào 1 số lượng props nhất định tùy vào việc chúng ta định nghĩa nó như thế nào
- C: Một component có thể nhận vào vô số props

<br />

---
<br />

#### Câu 7: Props sẽ hợp lệ khi được nhận các kiểu dữ liệu nào?
- A: Chuỗi
- B: Tất cả các kiểu dữ liệu có trong JavaScript
- C: Tất cả các kiểu dữ liệu ngoại trừ các kiểu dữ liệu tham chiếu (object, array, function)

<br />

---
<br />

#### Câu 8: Để sử dụng được JavaScript trong JSX, chúng ta sử dụng cặp ngoặc nào?
- A: `{}`
- B: `[]`
- C: Chỉ cần viết code JS vào là chạy được

<br />

--- 
<br />

#### Câu 9: Style inline trong JSX được viết dưới dạng nào?
- A: Object
- B: Chuỗi
- C: Array

<br />

--- 
<br />

#### Câu 10: Điền vào chỗ trống cú pháp hợp lý để chữ trong thẻ `p` có màu `#f00`.
```js
function Paragraph() {
    return <p style=___________>This is a paragraph</p>
}
```
- A: `{{ color: #f00 }}`
- B: `{{ color: '#f00' }}`
- C: `{{{ color: '#f00' }}}`

<br />

--- 
<br />

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

<br />

--- 
<br />

#### Câu 12: Component `Lock` trả về chuỗi JSX như nào?.
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

<br />

--- 
<br />

#### Câu 13: Component `Paragraph` trả về chuỗi JSX như nào?.
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

<br />

--- 
<br />
