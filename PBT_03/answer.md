Phần A:
    C1:
        -inline css:
            +ưu điểm:
                _Nhanh chóng, dễ áp dụng.
                _Không cần file ngoài.
            +Nhược điểm:
                _Khó bảo trì.
                _gây rối code.
            +Sử dụng khi chỉ cần chỉnh sửa cho 1 phần tử duy nhất.
            +Ví dụ:
            <h1 style= "color: blue "></h1>
        -internal css:
            +ưu điểm:
                _Dễ quản lý.
                _Không cần file ngoài.
            +Nhược điểm:
                _Không thể tái sự dụng.
            +Sử dụng khi chỉ có trang nhỏ.
            +Ví dụ:
            <head>
                <style>
                    p {
                    color: blue;
                    font-size: 18px;
                    }
                </style>
            </head>
        -external css:
            +ưu điểm:
                _Có thể tái sử dụng.
                _Dễ bảo trì.
            +Nhược điểm:
                _Phụ thuộc file ngoài.
            +Sử dụng khi cần quản lý tập trung nhiều trang web.
            +Ví dụ:
            <head>
                <link rel="stylesheet" href="styles.css">
            </head>
            p {
                color: green;
                font-size: 20px;
            }
    C2:
        -Các selector:
            +h1: Chọn thẻ h1; nội dung: ShopTLU
            +.price: chọn tất cả thẻ thuộc class price; nội dung:
                     25.990.000
                     45.990.000
            +#app header: chọn thẻ header trong app; nội dung:
                    ShopTLU
                    Home
                    Products
                    About
            +nav a:first-child: chọn thẻ a đầu tiên trong nav; nội dung:
                    Home
            +.product.featured h2: chọn thẻ h2 trong thẻ thuộc class featured; nội dung:
                    
            +article > p: chọn thẻ p là con trực tiếp của article; nội dung:
                    25.990.000
                    Mô tả sản phẩm....
                    45.990.000
                    Mô tả sản phẩm....
            +a[href="/"]: chọn thẻ a có thuộc tính href="/"; nội dung:
                    Home
            +.top-bar.dark h1: chọn thẻ h1 trong các thẻ thuộc class dark; nội dung:


    C3:
        -Trường hợp 1:
            +chiều rộng hiển thị: 400+20*2+5*2 = 450px
            +không gian chiếm trên trang: 400+20*2+5*2+10*4 = 490px
        -Trường hợp 2:
            +chiều rộng hiển thị: 400px
            +kích thước content thực tế: 400-20*2-5*2 = 350px
            +không gian chiếm trên trang: 400+10*4 = 440
        -Trường hợp 3:
            +khoảng cách giữa box-a và box-b: 40px
            +không phải 65px do margin dọc chỉ lấy giá trị lớn nhất mà không cộng tổng giá trị khi margin chồng lên nhau.
    C4:
        -A: 0 0 1
        -B: 0 1 0
        -C: 1 0 0
        -D: 0 1 1
        -element có màu đỏ vì id có giá trị ưu tiên cao.
        -thêm lệnh <p class="price" id="main-price" style="color: orange;"> element có màu cam.
        -nếu thêm !important element có màu đen do !important có ưu tiên cao nhất.
Phần B:
    C2:
        -box 1: chiều rộng thực tế 350px
        -box 2: chiều rộng thực tế 300px
        
Phần C:
    C1:
        -chiều rộn thực tế:
            +sidebar: 300+20*2+1*2=342px
            +content: 660+30*2+1*2=722px
        -layout vỡ do chiều rộng sidebar và content cộng lại vượt quá chiều rộng container chứa cả 2.
    C2: