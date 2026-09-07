# Hướng dẫn tạo Thanh Chuyển Hướng (Navigation Bar)

## 1. File HTML (`nav-bar.html`)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Navigation Bar</title>
    <link rel="stylesheet" href="nav-bar.css">
</head>
<body>

    <nav>
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">Tutorials</a></li>
            <li><a href="#">About</a></li>
            <li><a href="#">Newsletter</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
    </nav>

</body>
</html>
```

### Giải thích file HTML (`nav-bar.html`)
- `<nav>`: Đây là thẻ chuyên dùng để bọc các thanh điều hướng (menu). Đề bài yêu cầu dùng thẻ này làm khung chứa (container).
- `<ul>`: Thẻ tạo một danh sách không có thứ tự (Unordered List).
- `<li>`: Thẻ định nghĩa từng mục con bên trong danh sách (List Item). Các mục như Home, Tutorials, About... đều được bọc trong thẻ này.
- `<a href="#">`: Thẻ tạo liên kết (Hyperlink). Chữ hiển thị trên menu phải bấm vào được, nên chúng ta đặt chữ vào trong thẻ `<a>`. Dấu `#` tạm thời làm liên kết trống.

---

## 2. File CSS (`nav-bar.css`)

```css
body {
    margin: 0px;
    padding: 0px;
    background-color: #CCCCCC;
}

ul {
    margin: 0px;
    padding: 0px;
    background-color: #444;
    text-align: center;
    list-style: none;
}

li {
    font-size: 24px;
    height: 40px;
    line-height: 40px;
    padding: 20px;
    display: inline-block;
}

a {
    text-decoration: none;
    color: #ffffff;
}
```

### Giải thích file CSS (`nav-bar.css`)

#### Phần định dạng toàn trang (`body`):
- `margin: 0px;` và `padding: 0px;`: Xóa bỏ mọi khoảng trống thừa ở lề ngoài và lề trong của trang web, giúp thanh menu bám sát lên mép trên cùng của màn hình.
- `background-color: #CCCCCC;`: Phủ màu nền xám nhạt cho toàn bộ trang web theo đúng yêu cầu.

#### Phần định dạng danh sách (`ul`):
- `background-color: #444;`: Tô màu nền xám đen cho thanh menu.
- `text-align: center;`: Căn giữa tất cả các chữ nằm trong menu.
- `list-style: none;`: Xóa bỏ các dấu chấm đen mặc định ở đầu mỗi dòng của danh sách `<ul>`.

#### Phần định dạng từng mục menu (`li`):
- `font-size: 24px;`: Chỉnh kích thước chữ to lên 24px.
- `height: 40px;` và `line-height: 40px;`: Chiều cao của khung chữ và khoảng cách dòng đều là 40px, giúp chữ được căn giữa theo chiều dọc.
- `padding: 20px;`: Tạo khoảng trống bên trong mỗi mục là 20px (giúp menu phình to ra và có không gian thoáng).
- `display: inline-block;`: Đây là mấu chốt (gợi ý của đề bài). Thuộc tính này ép các thẻ `<li>` vốn dĩ đang xếp dọc (trên xuống dưới) chuyển sang xếp hàng ngang cạnh nhau.

#### Phần định dạng liên kết (`a`):
- `text-decoration: none;`: Xóa bỏ đường gạch chân mặc định của các thẻ liên kết.
- `color: #ffffff;`: Đổi màu chữ thành màu trắng.