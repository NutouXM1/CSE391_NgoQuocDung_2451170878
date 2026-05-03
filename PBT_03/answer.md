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