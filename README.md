# homework-react-4
## Câu 1: Props trong React là gì?
- Props (viết tắt của "properties") là các tham số được truyền vào các component của React. Chúng hoạt động tương tự như các tham số của hàm trong JavaScript và cho phép bạn truyền dữ liệu từ component cha xuống component con.
- Props là immutable, có nghĩa là không thể thay đổi giá trị của chúng trong component nhận chúng.
- Props giúp component trở nên linh hoạt và tái sử dụng được bằng cách cung cấp các giá trị khác nhau cho component.
- Props được truyền từ component cha xuống component con dưới dạng thuộc tính của thẻ component.
## Câu 2: Tại sao cần viết hoa các component?
- Trong React, các component phải được viết hoa để React có thể phân biệt giữa các thành phần HTML và các component của React. Khi tên component bắt đầu bằng chữ viết hoa, React sẽ coi đó là một React Component và không phải là một thẻ HTML.
## Câu 3: Fragment là gì?
Fragment là một công cụ trong React cho phép bạn nhóm nhiều element lại với nhau mà không thêm các thẻ không cần thiết vào DOM. Nó rất hữu ích khi bạn muốn trả về nhiều phần tử từ một component mà không tạo ra các thẻ không mong muốn.
Fragment giữ cho DOM sạch sẽ và gọn gàng bằng cách không thêm các thẻ không cần thiết, cải thiện hiệu suất bằng cách giảm bớt các node trong DOM.
- Cách 1:
```js
import React, { Fragment } from 'react';

const App = () => {
  return (
    <Fragment>
      <h1>Title</h1>
      <p>Paragraph</p>
    </Fragment>
  );
};

export default App;

```
- Cách 2 (viết ngắn gọn):
```js
import React from 'react';

const App = () => {
  return (
    <>
      <h1>Title</h1>
      <p>Paragraph</p>
    </>
  );
};

export default App;

```
## Câu 4: Sự khác biệt giữa “Element” và “Component” trong React?
**React Element**
1. Định nghĩa:
- React Element là khối xây dựng cơ bản của React ứng dụng.
- Nó mô tả những gì bạn muốn thấy trên giao diện người dùng: một thẻ HTML hoặc một thành phần React.
2. Đặc điểm:
- React Element là một đối tượng không thể thay đổi (immutable).
- Khi một React Element được tạo ra, bạn không thể thay đổi các thuộc tính của nó. Điều này giúp đảm bảo rằng giao diện người dùng có thể dự đoán được và nhất quán.
3. Tạo ra React Element:
- Có thể tạo ra bằng cách sử dụng JSX hoặc React.createElement().
```js
const element = <h1>Hello, world!</h1>;
```
```js
const element = React.createElement('h1', null, 'Hello, world!');
```
**React Component**
1. Định nghĩa:
- React Component là một lớp hoặc hàm JavaScript chấp nhận đầu vào (props) và trả về React Element để mô tả những gì xuất hiện trên giao diện người dùng.
- React Element giống như các thẻ HTML cơ bản, trong khi React Component giống như các hàm hoặc lớp có thể chứa logic phức tạp và quản lý trạng thái.
2. Đặc điểm:
- Có thể có trạng thái (state) và vòng đời (lifecycle methods) riêng.
- Giúp tổ chức và tái sử dụng mã trong ứng dụng.
- Có hai loại chính: Functional Component và Class Component.
3. Tạo ra React Component:
- Class Component:
```js
class Welcome extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}
```
- Functional Component:
```js
const Welcome = (props) => {
  return <h1>Hello, {props.name}</h1>;
}
```
