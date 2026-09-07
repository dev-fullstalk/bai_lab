# Hướng dẫn Lab HTML Structure

---

# Phần 1: Thanh Chuyển Hướng (Navigation Bar)

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

---

# Phần 2: Nội Dung Trang Web (Page Content)

## 1. File HTML (`page-content.html`)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Page Content</title>
    <link rel="stylesheet" href="page-content.css">
</head>
<body>

    <section>
        <!-- Bài blog thứ 1 -->
        <article>
            <header>
                <h1>Just Another Day</h1>
                <p>Written by Christina on January 11th</p>
            </header>
            <p>This is my second blog entry, and I just wanted to check in on you</p>
        </article>

        <!-- Bài blog thứ 2 -->
        <article>
            <header>
                <h1>My First Blog Entry</h1>
                <p>Written by Christina on January 10th</p>
            </header>
            <p>I’m so happy to write my first blog entry – yay!</p>
        </article>
    </section>

</body>
</html>
```

---

## 2. File CSS (`page-content.css`)

```css
body {
    margin: 0px;
    padding: 0px;
    background-color: #CCCCCC;
}

section {
    margin-left: 20px;
}

header h1 {
    font-size: 28px;
}

header p {
    font-style: italic;
}

/* Ký hiệu ">" giúp chỉ định dạng cho thẻ <p> là đoạn văn nội dung nằm trực tiếp trong <article>, không ảnh hưởng tới thẻ <p> nằm trong <header> */
article > p {
    font-size: 24px;
}
```

### Giải thích nhanh các điểm quan trọng (Phần 2):

#### Về HTML (Cấu trúc):
- `<section>`: Thẻ đóng vai trò là một vùng/phân đoạn lớn chứa toàn bộ nội dung bài viết.
- `<article>`: Thẻ bọc một bài viết độc lập (ở đây mình có 2 bài blog, nên dùng 2 thẻ `<article>`).
- `<header>`: Khác với thẻ `<head>` trên cùng, `<header>` ở đây dùng để nhóm phần "tiêu đề bài viết" (`<h1>`) và "thông tin tác giả/ngày tháng" (`<p>`) lại với nhau cho chuẩn cấu trúc.

#### Về CSS (Định dạng):
- `margin-left: 20px;` (trong `section`): Đẩy lùi toàn bộ khung chứa bài viết vào trong 20px so với lề trái màn hình, giúp chữ không bị dính sát vào viền trình duyệt.
- `font-style: italic;` (trong `header p`): In nghiêng dòng chữ tên tác giả.
- `article > p { font-size: 24px; }`: Chỗ này là một mẹo nhỏ. Vì thẻ `<p>` được dùng cho cả phần tên tác giả và phần nội dung bài blog, nên nếu ta dùng `p { font-size: 24px; }` thì tên tác giả cũng bị phình to ra. Dấu `>` (Child Combinator) giúp ta chỉ phóng to cỡ chữ 24px cho thẻ `<p>` đóng vai trò là đoạn nội dung nằm ngay dưới `<article>`.

---

# Phần 3: Ghép Nối Trang Web (Simple Website)

## 1. File HTML (`simple-website.html`)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Simple Website</title>
    <link rel="stylesheet" href="simple-website.css">
</head>
<body>

    <!-- Phần 1: Thanh Menu (Từ bài 1) -->
    <nav>
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">Tutorials</a></li>
            <li><a href="#">About</a></li>
            <li><a href="#">Newsletter</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
    </nav>

    <!-- Phần 2: Nội dung Blog (Từ bài 2) -->
    <section>
        <article>
            <header>
                <h1>Just Another Day</h1>
                <p>Written by Christina on January 11th</p>
            </header>
            <p>This is my second blog entry, and I just wanted to check in on you</p>
        </article>

        <article>
            <header>
                <h1>My First Blog Entry</h1>
                <p>Written by Christina on January 10th</p>
            </header>
            <p>I’m so happy to write my first blog entry – yay!</p>
        </article>
    </section>

    <!-- Phần 3 mới: Chân trang (Footer) -->
    <footer>
        <!-- Ký hiệu &copy; dùng để in ra chữ C bản quyền © -->
        <p>&copy; Copyright 2026 Duong Duc Trung</p>
    </footer>

</body>
</html>
```

---

## 2. File CSS (`simple-website.css`)

```css
/* --- CODE CỦA BÀI 1 & 2 GỘP LẠI --- */
body {
    margin: 0px;
    padding: 0px;
    background-color: #CCCCCC;
}

ul {
    background-color: #444;
    text-align: center;
    padding: 0px;
    margin: 0px;
    list-style: none;
}

li {
    font-size: 24px;
    line-height: 40px;
    height: 40px;
    padding: 20px;
    display: inline-block; /* Xếp hàng ngang */
}

a {
    text-decoration: none;
    color: #ffffff;
}

section {
    margin-left: 20px; /* Thụt lề cho nội dung */
}

header h1 {
    font-size: 28px;
}

header p {
    font-style: italic;
}

article > p {
    font-size: 24px;
}

/* --- CODE MỚI CHO BÀI 3 (FOOTER) --- */
footer {
    background-color: #444; /* Nền xám đen giống menu */
}

footer p {
    color: #fff; /* Chữ màu trắng */
    text-align: center; /* Căn giữa chữ */
    margin: 0px; 
    padding: 10px; /* Thêm padding để khung chân trang không bị ép sát vào chữ */
}
```

### Giải thích nhanh các điểm quan trọng (Phần 3):

- **Lắp ráp HTML**: Trong file HTML, đặt thẻ `<nav>` lên đầu tiên, sau đó đến `<section>` (nội dung), và cuối cùng gọi thẻ `<footer>` mới. Đây là cấu trúc kinh điển và chuẩn semantic của một trang web.
- **Ký tự đặc biệt (`&copy;`)**: Ký tự thực thể HTML `&copy;` khi hiển thị trên trình duyệt sẽ tự động biến thành biểu tượng bản quyền `©`.
- **Thêm padding cho Footer**: Việc thêm `padding: 10px;` vào `footer p` giúp vùng màu xám đen của `<footer>` không bị ép bẹp vào dòng chữ bản quyền, tạo khoảng thở cân đối và đẹp mắt.

---

# Phần 4: Bảng Điểm Thi (Exam Results)

## 1. File HTML (`exam-results.html`)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Exam Results</title>
    <link rel="stylesheet" href="exam-results.css">
</head>
<body>

    <table>
        <thead>
            <!-- Dòng 1: Tiêu đề bảng (gộp 4 cột) -->
            <tr>
                <th colspan="4">Web fundamentals exam result</th>
            </tr>
            <!-- Dòng 2: Tiêu đề các cột -->
            <tr>
                <!-- &#8470; là mã HTML để in ra ký hiệu "Số" (№) -->
                <td class="bold">&#8470;</td>
                <td class="bold">First name</td>
                <td class="bold">Last name</td>
                <td class="bold">Score</td>
            </tr>
        </thead>
        <tbody>
            <!-- Các dòng dữ liệu -->
            <tr>
                <td>01</td>
                <td>Gosho</td>
                <td>Goshev</td>
                <td>500</td>
            </tr>
            <tr>
                <td>02</td>
                <td>Tosho</td>
                <td>Toshev</td>
                <td>500</td>
            </tr>
            <tr>
                <td>03</td>
                <td>Gencho</td>
                <td>Genchev</td>
                <td>500</td>
            </tr>
            <tr>
                <td>04</td>
                <td>Draga</td>
                <td>Draganova</td>
                <td>500</td>
            </tr>
            <tr>
                <td>05</td>
                <td>Gosho</td>
                <td>Goshev</td>
                <td>500</td>
            </tr>
        </tbody>
        <tfoot>
            <!-- Dòng cuối: Footer của bảng (gộp 4 cột) -->
            <tr>
                <td class="result" colspan="4">Average score from 05 participants: 500</td>
            </tr>
        </tfoot>
    </table>

</body>
</html>
```

---

## 2. File CSS (`exam-results.css`)

```css
/* Đóng khung viền đen 1px cho bảng, hàng, và từng ô */
table, td, tr, th {
    border: 1px solid #000000;
}

/* Thẻ th mặc định sẽ được in đậm và căn giữa */
th {
    font-size: 20px;
    padding: 5px;
}

/* Định dạng cho các ô chứa nội dung in đậm */
.bold {
    font-weight: bold;
    text-align: center;
}

/* Định dạng riêng cho dòng kết quả cuối bảng */
.result {
    width: 400px;
    text-align: right; /* Đẩy chữ sang lề phải */
    padding-right: 5px; /* Khoảng cách lề phải 5px */
}

/* Định dạng khoảng cách chữ so với viền trái cho các ô dữ liệu (Table data) */
td {
    padding-left: 5px; 
}
```

### Giải thích nhanh các điểm quan trọng (Phần 4):

- **Thẻ cấu trúc bảng**: `<table>` chứa toàn bộ bảng, `<thead>` định nghĩa phần đầu bảng, `<tbody>` chứa các dòng dữ liệu và `<tfoot>` định nghĩa phần chân bảng.
- **Gộp cột (`colspan="4"`)**: Sử dụng ở dòng `<th>` tiêu đề và dòng `<td class="result">` để hợp nhất 4 ô ngang thành 1 ô duy nhất trải dài toàn bộ chiều rộng bảng.
- **Ký tự đặc biệt (`&#8470;`)**: Mã thực thể HTML biểu thị ký hiệu số thứ tự (№).
- **Viền bảng (`border: 1px solid #000000;`)**: Tạo viền đơn đen quanh bảng, hàng và ô. Mặc định bảng sẽ có hiệu ứng viền đôi; nếu muốn viền đơn sát nhau có thể thêm `border-collapse: collapse;` vào `table`.

---

# Phần 5: Bố Cục Trang Web Hoàn Chỉnh (Lab 5 - Layout)

## 1. File HTML (`lab5.html`)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Lab 5 - Layout</title>
    <link rel="stylesheet" href="lab5.css">
</head>
<body>

    <!-- Phần đầu trang -->
    <header class="site-header">
        <h1>Site Header</h1>
    </header>

    <!-- Khung chứa phần thanh bên (Aside) và Nội dung (Article) -->
    <div class="container">
        
        <!-- Thanh điều hướng bên trái -->
        <aside>
            <h2>Aside Header Nav</h2>
            <ul>
                <li><a href="#">Home Link</a></li>
                <li><a href="#">Link</a></li>
                <li><a href="#">Link</a></li>
            </ul>
        </aside>

        <!-- Nội dung bài viết bên phải -->
        <article>
            <h2>Article Header</h2>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam blandit, augue vel pulvinar tincidunt, erat nunc facilisis tortor, vel commodo lorem purus nec magna. Sed et vehicula dui. Vivamus pulvinar pellentesque convallis. Nunc ornare blandit lacinia. Phasellus purus leo elementum vehicula laoreet id, aliquet vel lectus.</p>
            <p>Nullam fringilla ornare magna, a varius ibero viverra sed, nulla rutrum laoreet magna, quis eleifend arcu dictum ut. Ut velit lectus, sodales viverra gravida quis, auctor sit amet risus. Duis elementum, abero sed cursus fermentum, lectus est dictum sapien, ac pulvinar mauris dolor sit amet diam.</p>
        </article>

    </div>

    <!-- Phần chân trang -->
    <footer>
        <h2>Footer</h2>
        <p>2012</p>
    </footer>

</body>
</html>
```

---

## 2. File CSS (`lab5.css`)

```css
/* Đặt lại lề mặc định và chọn font chữ dễ nhìn */
body {
    margin: 0;
    padding: 0;
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
}

/* Định dạng cho Header và Footer (Màu nền tối, chữ trắng, căn giữa) */
.site-header, footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 20px;
}

/* Dùng Flexbox để chia cột cho phần Container */
.container {
    display: flex; /* Kích hoạt chế độ nằm ngang */
    max-width: 1000px; /* Giới hạn chiều rộng trang web */
    margin: 20px auto; /* Căn giữa toàn bộ phần thân */
    gap: 20px; /* Tạo khoảng trống 20px giữa Aside và Article */
}

/* Định dạng cột trái (Aside) */
aside {
    flex: 1; /* Chiếm 1 phần không gian */
    background-color: #e2e2e2;
    padding: 20px;
}

aside ul {
    list-style: none; /* Xóa dấu chấm đầu dòng */
    padding: 0;
}

aside li {
    margin-bottom: 10px;
}

aside a {
    text-decoration: none;
    color: #333;
    font-weight: bold;
}

/* Định dạng cột phải (Article) */
article {
    flex: 3; /* Chiếm 3 phần không gian (rộng gấp 3 lần Aside) */
    background-color: white;
    padding: 20px;
    border: 1px solid #ccc;
}
```

### Điểm mấu chốt của bài Lab 5:

- **Bố cục 2 cột bằng Flexbox**: Để chia trang web thành 2 cột (Menu bên trái và Bài viết bên phải), sử dụng thuộc tính `display: flex;` cho phần tử cha `.container`.
- **Tỉ lệ phân chia (`flex: 1;` và `flex: 3;`)**: 
  - Cột `<aside>` đặt `flex: 1;`.
  - Cột `<article>` đặt `flex: 3;`.
  - Nhờ vậy, `<article>` luôn rộng gấp 3 lần `<aside>`, tạo nên bố cục cân đối và co giãn mượt mà.
- **Khoảng cách cột (`gap: 20px;`)**: Tự động tạo rãnh ngăn cách 20px giữa 2 cột mà không cần chỉnh margin phức tạp.