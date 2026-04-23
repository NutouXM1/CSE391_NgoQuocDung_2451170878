Phần A:
    CÂU A1
        1
            - Sau khi nhập link shoppe và nhấn Enter, trình duyệt sẽ chuyển đổi tên miền thành địa chỉ IP
            - IP được gửi đi để tìm kiếm trang web trên mạng
            - Sau khi tìm thấy, trình duyệt sẽ gửi đi một request GET để xem trang chủ
            - Server sau khi nhận được request sẽ xử lý và gửi trả một response 200 OK
            - Trình duyệt nhận được file trả về và render lại lên màn hình
        2
            status code:PBT_01/screenshots/statuscodeandtotalloadtime.png
            thời gian load trang:PBT_01/screenshots/statuscodeandtotalloadtime.png
            request trả về file CSS:PBT_01/screenshots/returnCSS.png
            tham chiếu: tuan1html5/01_introduction_html_universe.md

    CÂU A2
            <div class="header">
                <div class="logo">ShopTLU</div>
                <div class="menu">
                    <div><a href="/">Trang chủ</a></div>
                    <div><a href="/products">Sản phẩm</a></div>
                </div>
            </div>
            <div class="main">
                <div class="product">
                    <div class="title">iPhone 16 Pro</div>
                    <div class="price">25.990.000đ</div>
                    <div class="image"><img src="iphone.jpg"></div>
                </div>
            </div>
            <div class="footer">© 2026 ShopTLU</div>

        Đoạn code bị đánh giá SEO thấp do lạm dụng tag div và không có bố cục rõ ràng.

        Cách sửa đề xuất:
            <header>
            <div class="logo">ShopTLU</div>
            <nav>
                <ul>
                <li><a href="/">Trang chủ</a></li>
                <li><a href="/products">Sản phẩm</a></li>
                </ul>
            </nav>
            </header>

            <main>
            <article>
                <h1>iPhone 16 Pro</h1>
                <p class="price">25.990.000đ</p>
                <img src="iphone.jpg" alt="iPhone 16 Pro">
            </article>
            </main>
            <footer>© 2026 ShopTLU</footer>

        tham chiếu: tuan1html5/04_visible_part_html.md

    CÂU A3
        tham chiếu: tuan1html5/04_visible_part_html.md

    CÂU A4
        thead được sử dụng để viết tên các cột trong bảng.
        tbody được sử dụng để viết dữ liệu vào các ô trong bảng.
        tfoot được sử dụng để viết dòng tổng hợp ở cuối các bảng(nếu có).
Phần B:
    B3:
        dòng 4 - không đóng thẻ title - thêm </title>.
        dòng 8 - đóng thẻ h1 sai cú pháp - thay bằng </h1>.
        dòng 12 - đóng thẻ link a sai cú pháp - thay bằng </a>.
        dòng 20 - src sai cú pháp - thay bằng <img src="iphone.jpg">.
        dòng 22 - đóng thẻ cha con sai thứ tự - đóng thẻ b trước thẻ p.
        dòng 27-36 - table không chia head body foot - chia thead gồm <td> tên và <td> giá; tbody gồm <td> iphone 16 pro và <td> 25.990.000.
        dòng 45 - không đóng thẻ p - thêm </p>.
        dòng 2-hết -  không đóng thẻ html - thêm </html>.
        dòng 41 - không đúng semantic - thay thẻ p bằng <aside>
    B4:
        3 thẻ semantic shopee.vn sử dụng: section, nav, footer
        ảnh: PBT_01/screenshots/shopeeSemantic.png
        form đăng nhập tài khoản shopee:
            Method sử dụng: get
            action không được gọi
        ảnh: PBT_01/screenshots/shopeeForm.png
Phần C:
    C1:
    <!DOCTYPE html>
    <html>
        <head>
            <title>Shop landing</title> <!-- tiêu đề trang hiển thị trên tab -->
            <meta charset="UTF-8"> <!-- hỗ trợ tiếng Việt -->
        </head>
        <body>
            <header>
                <section class="head">
                    <h2></h2> <!-- tiêu đề website -->
                </section>
                <section class="nav">
                    <nav> <!-- nav vì đây là điều hướng -->
                        <ul></ul> <!-- danh sách các mục menu -->
                    </nav>
                </section>
            </header>
            <main>
                <section class="proimgs">
                    <figure>
                        <img src="" alt="" srcset=""> <!-- ảnh sản phẩm -->
                        <img src="" alt="" srcset="">
                        <img src="" alt="" srcset="">
                        <img src="" alt="" srcset="">
                        <img src="" alt="" srcset="">
                    </figure>
                </section>
                <section class="proinfo">
                    <div id="pro1"> <!-- khối thông tin sản phẩm -->
                        <h2 class="proname"></h2> <!-- tên sản phẩm -->
                        <strong class="proprice"></strong> <!-- giá sản phẩm -->
                        <p class="prosyp"></p> <!-- mô tả ngắn -->
                        <figure class="prorating">
                            <img src="" alt="" srcset=""> <!-- hình đánh giá sao -->
                        </figure>
                    </div>
                    <div id="pro2">
                        <h2 class="proname"></h2>
                        <strong class="proprice"></strong>
                        <p class="prosyp"></p>
                        <figure class="prorating">
                            <img src="" alt="" srcset="">
                        </figure>
                    </div>
                    <div id="pro3">
                        <h2 class="proname"></h2>
                        <strong class="proprice"></strong>
                        <p class="prosyp"></p>
                        <figure class="prorating">
                            <img src="" alt="" srcset="">
                        </figure>
                    </div>
                    <div id="pro4">
                        <h2 class="proname"></h2>
                        <strong class="proprice"></strong>
                        <p class="prosyp"></p>
                        <figure class="prorating">
                            <img src="" alt="" srcset="">
                        </figure>
                    </div>
                    <div id="pro5">
                        <h2 class="proname"></h2>
                        <strong class="proprice"></strong>
                        <p class="prosyp"></p>
                        <figure class="prorating">
                            <img src="" alt="" srcset="">
                        </figure>
                    </div>
                </section>
                <section class="prospecs">
                    <table></table> <!-- dùng table để hiển thị thông số -->
                </section>
                <section class="procomments">
                    <form action="" class="starrating"></form> <!-- form đánh giá sao -->
                    <form action="" class="comments"></form> <!-- form nhập bình luận -->
                </section>
                <section class="prosimilar">
                    <aside></aside> <!-- aside vì là nội dung phụ -->
                </section>
            </main>
            <footer>
                <p>copyright</p> <!-- thông tin bản quyền -->
            </footer>
        </body>
    </html>