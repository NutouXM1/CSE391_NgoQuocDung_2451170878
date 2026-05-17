Phần A:
    C1:
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    -Các thuộc tính:
        +width=device-width: chiều rộng trang web bằng chiều rộng thiết bị.
        +initial-scale=1.0: mức zoom ban đầu bằng 100%
    -Nếu thiếu thẻ này iphone sẽ hiển thị giống như màn hình desktop thu nhỏ với chữ và hình ảnh quá nhỏ để đọc.
    -Mobile-first: bắt đầu thiết kế từ giao diện di động và mở rộng dần cho các màn hình lớn hơn.
        css:
            @media (min-width: 768px){}
    -Desktop-first: bắt đầu thiết kế từ giao diện desktop và thu hẹp dần cho các màn hình nhỏ.
        css:
            @media (max-width: 768px){}
    C2:
    breakpoints theo bootstrap:
    kích thước  thiết bị đại diện   ví dụ: lưới sản phẩm(cột)
    576px       điện thoại                  1-2
    768px       máy tính bảng                3
    992px       laptop                       4
    1200px      desktop                     5-6
    1400px      màn hình lớn                6-8
    C3:
    Chiều rộng màn hình     width
    375px                   100%
    600px                   540px
    800px                   720px
    1000px                  960px
    1400px                  1140px
    C4:
    -Các tính năng:
        +variables: sử dụng để khai báo các giá trị dùng nhiều lần, ví dụ: màu sắc, font, kích thước,....
            $primary: #805ad5;
            $radius: 8px;

            .btn {
            background: $primary;
            border-radius: $radius;
            }
        +nesting: cho phép viết css theo cấu trúc html->gọn gàng hơn.
            .navbar {
                ul {
                    li {
                        a {
                            color: white;
                            &:hover { color: $primary; }
                        }
                    }
                }
            }
        +mixins: sử dụng định nghĩa khối css tái sử dụng nhiều lần.
            @mixin flex-center {
                display: flex;
                justify-content: center;
                align-items: center;
            }

            .hero {
                @include flex-center;
                height: 100vh;
            }
        +partials và import: cho phép tách code thành nhiều file nhỏ.
            _variables.css
            _mixins.css
            @import 'variables';
            @import 'mixins';
Phần C:
    C1:
        -nav:
            +điện thoại: toàn bộ chức năng chuyển về nút hamburger.
            +tablet: sử dụng cả sidebar và hamburger
            +pc: thanh nav đầy đủ.
        -content grid:
            +điện thoại: 1 cột.
            +tablet: 2 cột.
            +pc: 2 cột+sidebar.
        -trên điện thoại ẩn đi các bộ lọc, sidebar.
        -font:
            +điện thoại: nhỏ.
            +tablet: trung bình.
            +pc: lớn.
        