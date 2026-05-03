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