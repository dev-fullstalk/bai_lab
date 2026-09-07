# CẨM NANG VẤN ĐÁP & GIẢI THÍCH CHI TIẾT TỪNG DÒNG CODE
> **Môn học:** Thiết kế Web (HTML5 & CSS3)  
> **Thư mục:** `ThietKeWeb/Lab_HTML_Structure`  
> **Mục tiêu:** Hiểu sâu bản chất từng dòng code, tự tin trả lời mọi câu hỏi vấn đáp của thầy cô.

---

## 📌 MỤC LỤC
1. [Phần 1: Thanh điều hướng (nav-bar.html & nav-bar.css)](#phần-1-thanh-điều-hướng-nav-barhtml--nav-barcss)
2. [Phần 2: Nội dung Blog (page-content.html & page-content.css)](#phần-2-nội-dung-blog-page-contenthtml--page-contentcss)
3. [Phần 3: Ghép nối trang web & Footer (simple-website.html & simple-website.css)](#phần-3-ghép-nối-trang-web--footer-simple-websitehtml--simple-websitecss)
4. [Phần 4: Bảng điểm thi (exam-results.html & exam-results.css)](#phần-4-bảng-điểm-thi-exam-resultshtml--exam-resultscss)
5. [Phần 5: Bố cục Flexbox (lab5.html & lab5.css)](#phần-5-bố-cục-flexbox-lab5html--lab5css)
6. [Tổng hợp các câu hỏi "bẫy" thầy cô hay hỏi nhất & cách trả lời](#tổng-hợp-các-câu-hỏi-bẫy-thầy-cô-hay-hỏi-nhất)

---

# PHẦN 1: THANH ĐIỀU HƯỚNG (nav-bar.html & nav-bar.css)

### 1.1. Giải thích từng dòng file `nav-bar.html`
```html
1:  <!DOCTYPE html>
2:  <html lang="en">
3:  <head>
4:      <meta charset="UTF-8">
5:      <title>Navigation Bar</title>
6:      <link rel="stylesheet" href="nav-bar.css">
7:  </head>
8:  <body>
9:      <nav>
10:         <ul>
11:             <li><a href="#">Home</a></li>
12:             <li><a href="#">Tutorials</a></li>
13:             <li><a href="#">About</a></li>
14:             <li><a href="#">Newsletter</a></li>
15:             <li><a href="#">Contact</a></li>
16:         </ul>
17:     </nav>
18: </body>
19: </html>
```
- **Dòng 1 (`<!DOCTYPE html>`):** Khai báo cho trình duyệt biết tài liệu này được viết theo chuẩn **HTML5**.
- **Dòng 2 (`<html lang="en">`):** Thẻ gốc (root) bao bọc toàn bộ trang web. Thuộc tính `lang="en"` báo cho công cụ tìm kiếm và trình đọc màn hình biết ngôn ngữ chính là tiếng Anh.
- **Dòng 3 - 7 (`<head>...</head>`):** Phần đầu trang, chứa siêu dữ liệu (metadata) không hiển thị trực tiếp lên giao diện người dùng.
  - **Dòng 4 (`<meta charset="UTF-8">`):** Đặt bảng mã ký tự UTF-8, giúp hiển thị đúng tiếng Việt có dấu và các ký tự đặc biệt mà không bị lỗi font.
  - **Dòng 5 (`<title>Navigation Bar</title>`):** Tiêu đề của trang web, hiển thị trên thanh tab của trình duyệt.
  - **Dòng 6 (`<link rel="stylesheet" href="nav-bar.css">`):** Liên kết file HTML với file CSS bên ngoài (`nav-bar.css`) để áp dụng giao diện.
- **Dòng 8 (`<body>`):** Phần thân của trang, chứa toàn bộ nội dung hiển thị cho người xem.
- **Dòng 9 (`<nav>`):** Thẻ ngữ nghĩa (Semantic HTML) chuyên dùng để bọc thanh điều hướng (menu). *Thầy hỏi tại sao dùng `<nav>` mà không dùng `<div>`? Trả lời: Dùng `<nav>` để chuẩn SEO và hỗ trợ người khiếm thị dùng máy đọc màn hình nhận biết đây là menu chính.*
- **Dòng 10 (`<ul>`):** Tạo một danh sách không có thứ tự (Unordered List) để chứa các nút bấm menu.
- **Dòng 11 - 15 (`<li><a href="#">...</a></li>`):**
  - `<li>` (List Item): Từng mục con trong danh sách menu.
  - `<a href="#">` (Anchor/Hyperlink): Tạo liên kết có thể click được. Dấu `#` là liên kết trống (anchor placeholder), khi click vào sẽ không chuyển trang mà giữ nguyên tại chỗ.
- **Dòng 16 - 19:** Đóng các thẻ `</ul>`, `</nav>`, `</body>`, `</html>`.

---

### 1.2. Giải thích từng dòng file `nav-bar.css`
```css
1:  body {
2:      margin: 0px;
3:      padding: 0px;
4:      background-color: #CCCCCC;
5:  }
6:  
7:  ul {
8:      margin: 0px;
9:      padding: 0px;
10:     background-color: #444;
11:     text-align: center;
12:     list-style: none;
13: }
14: 
15: li {
16:     font-size: 24px;
17:     height: 40px;
18:     line-height: 40px;
19:     padding: 20px;
20:     display: inline-block;
21: }
22: 
23: a {
24:     text-decoration: none;
25:     color: #ffffff;
26: }
```
- **Dòng 1 - 5 (`body`):**
  - `margin: 0px; padding: 0px;`: Xóa bỏ lề mặc định của trình duyệt. *Thầy hỏi: Nếu không có dòng này thì sao? Trả lời: Menu sẽ bị một khoảng hở màu trắng khoảng 8px quanh 4 viền màn hình, không bám sát mép trên cùng.*
  - `background-color: #CCCCCC;`: Tô màu nền toàn trang là màu xám nhạt (mã màu HEX: `#CCCCCC`).
- **Dòng 7 - 13 (`ul`):**
  - `margin: 0px; padding: 0px;`: Mặc định thẻ `<ul>` trong trình duyệt luôn có margin trên dưới và padding lùi đầu dòng 40px. Phải đặt về `0px` để thanh menu bám sát trên cùng và không bị lệch.
  - `background-color: #444;`: Đặt màu nền thanh menu thành xám đen (`#444` là viết tắt của `#444444`).
  - `text-align: center;`: Căn toàn bộ các mục menu nằm ra chính giữa màn hình theo chiều ngang.
  - `list-style: none;`: Xóa bỏ dấu chấm tròn đen mặc định ở đầu mỗi dòng của danh sách `<ul>`.
- **Dòng 15 - 21 (`li`):**
  - `font-size: 24px;`: Tăng kích thước chữ lên 24 pixel cho rõ ràng.
  - `height: 40px;`: Chiều cao khung của mỗi mục là 40px.
  - `line-height: 40px;`: Chiều cao dòng chữ bằng 40px. *Thầy hỏi: Tại sao `line-height` lại bằng đúng `height`? Trả lời: Đây là mẹo kinh điển trong CSS để căn giữa chữ theo chiều dọc (Vertical Center) mà không cần dùng Flexbox.*
  - `padding: 20px;`: Khoảng đệm bên trong 20px cho 4 phía, giúp các nút menu phình to ra và có khoảng cách bấm thoải mái.
  - `display: inline-block;`: **MẤU CHỐT CỦA BÀI 1.** Thẻ `<li>` bản chất là dạng khối (`block`) nên mặc định sẽ xếp dọc từ trên xuống dưới. Chuyển sang `inline-block` giúp các thẻ `<li>` vừa nằm ngang hàng cạnh nhau như chữ (inline), vừa giữ được kích thước chiều cao, padding, margin như khối (block).
- **Dòng 23 - 26 (`a`):**
  - `text-decoration: none;`: Bỏ đường gạch chân màu xanh mặc định dưới chữ của thẻ liên kết `<a>`.
  - `color: #ffffff;`: Đổi màu chữ liên kết thành màu trắng để nổi bật trên nền menu xám đen.

---

# PHẦN 2: NỘI DUNG BLOG (page-content.html & page-content.css)

### 2.1. Giải thích từng dòng file `page-content.html`
```html
1:  <!DOCTYPE html>
2:  <html lang="en">
3:  <head>
4:      <meta charset="UTF-8">
5:      <title>Page Content</title>
6:      <link rel="stylesheet" href="page-content.css">
7:  </head>
8:  <body>
9:      <section>
10:         <!-- Bài blog thứ 1 -->
11:         <article>
12:             <header>
13:                 <h1>Just Another Day</h1>
14:                 <p>Written by Christina on January 11th</p>
15:             </header>
16:             <p>This is my second blog entry, and I just wanted to check in on you</p>
17:         </article>
18: 
19:         <!-- Bài blog thứ 2 -->
20:         <article>
21:             <header>
22:                 <h1>My First Blog Entry</h1>
23:                 <p>Written by Christina on January 10th</p>
24:             </header>
25:             <p>I’m so happy to write my first blog entry – yay!</p>
26:         </article>
27:     </section>
28: </body>
29: </html>
```
- **Dòng 9 (`<section>`):** Vùng chứa bao bọc một khu vực nội dung có cùng chủ đề (ở đây là toàn bộ danh sách các bài blog).
- **Dòng 11 & 20 (`<article>`):** Thẻ đại diện cho một bài viết hoàn chỉnh, độc lập và có ý nghĩa riêng biệt. Nếu tách riêng bài này đưa lên nơi khác thì người đọc vẫn hiểu trọn vẹn.
- **Dòng 12 & 21 (`<header>`):** Khác với thẻ `<head>` ở trên, `<header>` ở đây là phần đầu của bài viết, dùng để nhóm tiêu đề chính `<h1>` và ngày đăng/tác giả `<p>`.
- **Dòng 13 & 22 (`<h1>`):** Tiêu đề bài viết, thẻ tiêu đề quan trọng nhất của bài blog.
- **Dòng 14 & 23 (`<p>` trong `<header>`):** Đoạn văn bản chứa thông tin tác giả và ngày đăng.
- **Dòng 16 & 25 (`<p>` con trực tiếp của `<article>`):** Đoạn văn bản chứa nội dung thân bài blog.

---

### 2.2. Giải thích từng dòng file `page-content.css`
```css
1:  body {
2:      margin: 0px;
3:      padding: 0px;
4:      background-color: #CCCCCC;
5:  }
6:  
7:  section {
8:      margin-left: 20px;
9:  }
10: 
11: header h1 {
12:     font-size: 28px;
13: }
14: 
15: header p {
16:     font-style: italic;
17: }
18: 
19: /* Ký hiệu ">" giúp chỉ định dạng cho thẻ <p> là đoạn văn nội dung nằm trực tiếp trong <article>, không ảnh hưởng tới thẻ <p> nằm trong <header> */
20: article > p {
21:     font-size: 24px;
22: }
```
- **Dòng 1 - 5 (`body`):** Xóa lề và đặt màu nền xám nhạt `#CCCCCC` đồng bộ với bài 1.
- **Dòng 7 - 9 (`section`):**
  - `margin-left: 20px;`: Thụt lề trái vào trong 20px. Giúp toàn bộ bài viết không bị dính sát mép trái màn hình.
- **Dòng 11 - 13 (`header h1`):**
  - Bộ chọn (selector) kết hợp: Chỉ chọn thẻ `<h1>` nằm bên trong thẻ `<header>`.
  - `font-size: 28px;`: Tăng kích thước chữ tiêu đề lên 28px.
- **Dòng 15 - 17 (`header p`):**
  - Chỉ chọn thẻ `<p>` nằm trong `<header>` (chính là dòng ngày tháng và tác giả).
  - `font-style: italic;`: In nghiêng chữ để phân biệt với phần thân bài viết.
- **Dòng 19 - 22 (`article > p`):** **ĐIỂM ĂN ĐIỂM CỦA BÀI 2.**
  - Ký hiệu `>` là **Child Combinator (Bộ chọn con trực tiếp)**.
  - *Thầy hỏi: Tại sao không viết `article p` hoặc `p` mà phải viết `article > p`?*
  - *Trả lời:* Trong mỗi bài blog có 2 thẻ `<p>`:
    1. Một thẻ `<p>` nằm trong `<header>` (chứa tác giả).
    2. Một thẻ `<p>` nằm trực tiếp dưới `<article>` (chứa nội dung bài viết).
    Nếu viết `p { font-size: 24px; }` hoặc `article p` thì cả dòng tác giả cũng bị phóng to chữ lên 24px. Dùng `article > p` chỉ chọn thẻ `<p>` con trực tiếp của `<article>`, nhờ vậy dòng tác giả vẫn giữ nguyên kích thước mặc định, chỉ có thân bài viết là phóng to 24px.

---

# PHẦN 3: GHÉP NỐI TRANG WEB & FOOTER (simple-website.html & simple-website.css)

### 3.1. Điểm mới trong `simple-website.html`
- Kết hợp cả 3 thành phần kinh điển của một website chuẩn:
  1. `<nav>`: Menu điều hướng trên cùng (từ Phần 1).
  2. `<section>`: Khu vực nội dung bài viết (từ Phần 2).
  3. `<footer>`: Chân trang web ở dưới cùng.
- Dòng code mới ở Footer:
  ```html
  <footer>
      <p>&copy; Copyright 2026 Duong Duc Trung</p>
  </footer>
  ```
  - `&copy;`: Là **HTML Entity** (thực thể HTML). Khi trình duyệt đọc mã `&copy;`, nó sẽ tự động render ra biểu tượng chữ C bản quyền: `©`.

### 3.2. Điểm mới trong `simple-website.css`
```css
footer {
    background-color: #444;
}

footer p {
    color: #fff;
    text-align: center;
    margin: 0px; 
    padding: 10px;
}
```
- `footer`: Đặt màu nền xám đen `#444` đồng bộ hoàn hảo với thanh menu `<ul>` ở trên đầu trang.
- `footer p`:
  - `color: #fff;`: Chữ màu trắng dễ đọc trên nền tối.
  - `text-align: center;`: Căn giữa dòng chữ bản quyền ra giữa trang.
  - `margin: 0px;`: Xóa bỏ khoảng cách thừa mặc định của thẻ `<p>`.
  - `padding: 10px;`: **Rất quan trọng.** Tạo khoảng đệm cách đều 10px trên, dưới, trái, phải. Nếu không có `padding: 10px;`, nền xám đen sẽ bó sát chặt vào viền chữ bản quyền trông rất chật chội và xấu.

---

# PHẦN 4: BẢNG ĐIỂM THI (exam-results.html & exam-results.css)

### 4.1. Giải thích từng dòng file `exam-results.html`
```html
1:  <table>
2:      <thead>
3:          <tr>
4:              <th colspan="4">Web fundamentals exam result</th>
5:          </tr>
6:          <tr>
7:              <td class="bold">&#8470;</td>
8:              <td class="bold">First name</td>
9:              <td class="bold">Last name</td>
10:             <td class="bold">Score</td>
11:         </tr>
12:     </thead>
13:     <tbody>
14:         <tr>
15:             <td>01</td>
16:             <td>Gosho</td>
17:             <td>Goshev</td>
18:             <td>500</td>
19:         </tr>
            ... (các dòng tiếp theo)
20:     </tbody>
21:     <tfoot>
22:         <tr>
23:             <td class="result" colspan="4">Average score from 05 participants: 500</td>
24:         </tr>
25:     </tfoot>
26: </table>
```
- **Dòng 1 (`<table>`):** Thẻ định nghĩa bảng dữ liệu.
- **Dòng 2 (`<thead>`):** Nhóm các dòng tiêu đề của bảng.
- **Dòng 3, 6, 14, 22 (`<tr>`):** Viết tắt của **Table Row** - Tạo một hàng mới trong bảng.
- **Dòng 4 (`<th colspan="4">`):** 
  - `<th>` (Table Header): Ô tiêu đề, mặc định chữ sẽ được in đậm và căn giữa.
  - `colspan="4"`: **Gộp 4 cột làm 1 ô.** Giúp dòng tiêu đề dài trải rộng bằng đúng độ rộng của 4 cột bên dưới.
- **Dòng 7 (`&#8470;`):** Thực thể HTML đại diện cho ký hiệu số thứ tự: **№**.
- **Dòng 13 (`<tbody>`):** Nhóm các dòng dữ liệu thân bảng (Table Body).
- **Dòng 15 - 18 (`<td>`):** Viết tắt của **Table Data** - Ô chứa dữ liệu bình thường.
- **Dòng 21 (`<tfoot>`):** Nhóm dòng tổng kết dưới chân bảng (Table Footer).
- **Dòng 23 (`<td class="result" colspan="4">`):** Dòng tổng kết điểm trung bình, cũng dùng `colspan="4"` để gộp trọn 4 cột.

---

### 4.2. Giải thích từng dòng file `exam-results.css`
```css
1:  table, td, tr, th {
2:      border: 1px solid #000000;
3:  }
4:  
5:  th {
6:      font-size: 20px;
7:      padding: 5px;
8:  }
9:  
10: .bold {
11:     font-weight: bold;
12:     text-align: center;
13: }
14: 
15: .result {
16:     width: 400px;
17:     text-align: right;
18:     padding-right: 5px;
19: }
20: 
21: td {
22:     padding-left: 5px; 
23: }
```
- **Dòng 1 - 3:** Gán viền liền màu đen dày 1px (`1px solid #000000`) cho bảng và tất cả các ô. Mặc định bảng sẽ có hiệu ứng viền đôi cổ điển đúng như đề bài.
- **Dòng 5 - 8 (`th`):** Tăng cỡ chữ tiêu đề lên 20px và đệm 5px để chữ không dính vào viền.
- **Dòng 10 - 13 (`.bold`):** Class tự đặt dùng để in đậm (`font-weight: bold;`) và căn giữa chữ (`text-align: center;`) cho hàng tiêu đề cột.
- **Dòng 15 - 19 (`.result`):** Định dạng riêng cho ô tổng kết ở footer:
  - `width: 400px;`: Khống chế chiều rộng tối thiểu của bảng là 400px.
  - `text-align: right;`: Căn chữ sang lề bên phải.
  - `padding-right: 5px;`: Giữ khoảng cách 5px so với viền bên phải để chữ không chạm sát viền.
- **Dòng 21 - 23 (`td`):** Tạo khoảng cách `padding-left: 5px;` để các chữ dữ liệu không bị dính vào vách ngăn bên trái của ô.

---

# PHẦN 5: BỐ CỤC FLEXBOX (lab5.html & lab5.css)

### 5.1. Cấu trúc `lab5.html`
- Gồm 3 vùng chính:
  1. `<header class="site-header">`: Đầu trang web.
  2. `<div class="container">`: Thân trang web, bọc 2 phần tử con là `<aside>` (thanh bên trái) và `<article>` (bài viết bên phải).
  3. `<footer>`: Chân trang web có chữ "2012".

### 5.2. Giải thích mấu chốt `lab5.css`
```css
.container {
    display: flex;
    max-width: 1000px;
    margin: 20px auto;
    gap: 20px;
}

aside {
    flex: 1;
    background-color: #e2e2e2;
    padding: 20px;
}

article {
    flex: 3;
    background-color: white;
    padding: 20px;
    border: 1px solid #ccc;
}
```
- `display: flex;`: **Cực kỳ quan trọng.** Biến `.container` thành một Flex Container. Mọi phần tử con bên trong (`aside` và `article`) sẽ tự động chuyển từ xếp dọc sang xếp hàng ngang cạnh nhau.
- `max-width: 1000px;` và `margin: 20px auto;`: Giới hạn độ rộng tối đa 1000px, và `margin: 20px auto;` sẽ tự động căn giữa toàn bộ khối nội dung ra chính giữa màn hình (lề trên dưới 20px, lề trái phải `auto`).
- `gap: 20px;`: Thuộc tính của Flexbox giúp tự động tạo khoảng trống 20px ngăn giữa cột trái và cột phải mà không cần dùng `margin-right`.
- `flex: 1;` và `flex: 3;`:
  - Tổng số phần không gian là $1 + 3 = 4$ phần.
  - `<aside>` chiếm 1 phần ($25\%$ độ rộng).
  - `<article>` chiếm 3 phần ($75\%$ độ rộng).
  - Kết quả: Cột bài viết luôn rộng gấp 3 lần cột menu bên trái, đúng chuẩn tỷ lệ layout hiện đại!

---

# TỔNG HỢP CÁC CÂU HỎI "BẪY" THẦY CÔ HAY HỎI NHẤT

### ❓ Câu 1: Thẻ `<head>` khác gì thẻ `<header>`?
> **Trả lời:**
> - `<head>`: Nằm ở đầu file HTML, chứa các thông tin cấu hình trang web như `<meta>`, `<title>`, `<link css>`. Toàn bộ nội dung trong `<head>` **không hiển thị** trên giao diện trang web (ngoại trừ thẻ title trên tab).
> - `<header>`: Nằm trong thẻ `<body>`, là thẻ ngữ nghĩa đại diện cho phần đầu trang web hoặc phần đầu của một bài viết. Nội dung trong `<header>` **có hiển thị** trực tiếp cho người dùng thấy.

---

### ❓ Câu 2: Tại sao phải dùng các thẻ `<nav>`, `<section>`, `<article>`, `<header>`, `<footer>` thay vì dùng thẻ `<div>`?
> **Trả lời:**
> Đây là các thẻ **Semantic HTML (HTML ngữ nghĩa)** của HTML5:
> 1. **Chuẩn SEO:** Giúp các công cụ tìm kiếm như Google hiểu rõ đâu là menu, đâu là bài viết chính, đâu là chân trang để đánh chỉ mục tốt hơn.
> 2. **Hỗ trợ tiếp cận (Accessibility):** Giúp các thiết bị đọc màn hình cho người khiếm thị biết cách phân biệt các khu vực của trang web.
> 3. **Dễ đọc, bảo trì code:** Lập trình viên nhìn vào biết ngay cấu trúc trang web thay vì nhìn một loạt thẻ `<div>` lồng nhau.

---

### ❓ Câu 3: Thuộc tính `display: inline-block` khác gì `inline` và `block`?
> **Trả lời:**
> - **`block`** (như `<div>`, `<p>`, `<li>` mặc định): Luôn chiếm trọn một hàng riêng biệt, bắt các phần tử sau phải xuống dòng. Cho phép chỉnh kích thước `width`, `height`, `padding`, `margin`.
> - **`inline`** (như `<span>`, `<a>`): Nằm cùng hàng với các chữ khác, nhưng **không cho phép** đặt `width` và `height`.
> - **`inline-block`** (mục menu `<li>` bài 1): Kết hợp ưu điểm của cả hai. Nó vừa nằm ngang hàng với phần tử khác (như inline), vừa có thể chỉnh được kích thước `width`, `height`, `padding`, `margin` (như block).

---

### ❓ Câu 4: Dấu `>` trong bộ chọn `article > p` có ý nghĩa gì? Nếu bỏ dấu `>` thành `article p` thì có chuyện gì xảy ra?
> **Trả lời:**
> - Dấu `>` là **Child Combinator (Bộ chọn con trực tiếp)**, nó chỉ tác động lên thẻ `<p>` nằm ngay dưới `<article>` cấp 1.
> - Nếu bỏ dấu `>` thành `article p` (Descendant selector), CSS sẽ chọn **tất cả** thẻ `<p>` nằm bên trong `<article>` kể cả thẻ `<p>` nằm lọt sâu bên trong `<header>`. Hậu quả là dòng tên tác giả trong `<header>` cũng sẽ bị phóng to kích thước thành 24px, làm sai lệch thiết kế bài viết.

---

### ❓ Câu 5: Trong CSS, mẹo `height: 40px; line-height: 40px;` dùng để làm gì?
> **Trả lời:**
> Khi đặt `line-height` (chiều cao của dòng văn bản) bằng đúng `height` (chiều cao của khung chứa), dòng chữ sẽ tự động được **căn ra chính giữa theo chiều dọc** (Vertical Centering).

---

### ❓ Câu 6: Trong bảng (Table), thuộc tính `colspan` là gì? Khác gì `rowspan`?
> **Trả lời:**
> - `colspan` (Column Span): Gộp nhiều **cột** trên cùng một hàng lại với nhau thành một ô dài nằm ngang. (Ví dụ: `colspan="4"` gộp 4 cột).
> - `rowspan` (Row Span): Gộp nhiều **hàng** trên cùng một cột lại với nhau thành một ô cao nằm dọc.

---

### ❓ Câu 7: Ký hiệu `&copy;` và `&#8470;` trong HTML gọi là gì?
> **Trả lời:**
> Được gọi là **HTML Entities (Thực thể HTML)**. Chúng dùng để hiển thị các ký tự đặc biệt hoặc các ký tự bị trùng với cú pháp HTML (như `<`, `>`, `&`).
> - `&copy;` $\rightarrow$ Biểu tượng bản quyền: `©`
> - `&#8470;` $\rightarrow$ Ký hiệu số thứ tự: `№`

---

### ❓ Câu 8: Flexbox trong Lab 5 hoạt động như thế nào?
> **Trả lời:**
> - Đặt `display: flex;` lên phần tử cha `.container` để kích hoạt mô hình hộp linh hoạt (Flexbox), biến các phần tử con thành các flex items nằm ngang.
> - `flex: 1` cho `<aside>` và `flex: 3` cho `<article>` chia độ rộng của `.container` thành 4 phần tỷ lệ ($1 : 3$), giúp cột bài viết luôn rộng gấp 3 lần cột điều hướng bên trái một cách tự động và co giãn linh hoạt khi thay đổi kích thước màn hình.
