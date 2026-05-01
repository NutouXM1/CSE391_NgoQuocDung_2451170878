Phần A:
    C1:
        -type="email"->ô nhập text, kiểm tra ký tự @->form đăng ký tài khoản.
        -type="password"->ô nhập text, ký tự hiển thị dưới dạng dấu *->Đăng nhập tài khoản khách hàng.
        -type="number"->ô nhập số, có nút tăng giảm, chỉ cho phép nhập số->nhập số lượng sản phẩm.
        -type="tel"->ô nhập text->nhập số điện thoại khách hàng.
        -type="url"->ô nhập text, kiểm tra định dạng URL hợp lệ->nhập link trang web.
        -type="date"->bộ chọn ngày, chỉ nhận giá trị ngày hợp lệ->chọn ngày sinh khách hàng.
        -type="time"->bộ chọn giờ, phút, chỉ nhận giá trị thời gian hợp lệ->chọn khung giờ giao hàng.
        -type="range"->thanh trượt, giá trị nằm trong khoảng min-max->chọn khoảng giá lọc sản phẩm.
        -type="color"->bộ chọn màu, giá trị là màu hợp lệ->cho phép chọn màu sản phẩm.
        -type="search"->ô nhập text có nút xóa nhanh->tìm kiếm sản phẩm.
    C2:
        -Trường hợp 1: fail validation vì ô này bắt buộc nhập dữ liệu.
        -Trường hợp 2: fail validation vì fail check ký tự "@" và phần phía sau.
        -Trường hợp 3: fail validation vì giá trị nhập lớn hơn trường giá trị được chấp nhận (1-10).
        -Trường hợp 4: fail validation vì giá trị không tuân theo pattern đã cho trước (10 số/mỗi số thuộc từ 0-9).
        -Trường hợp 5: fail validation vì mật khẩu nhập vào chưa đủ 8 ký tự.
    C3:
        -label for="email" giúp người dùng screen reader biết trường mình đang nhập dữ liệu là trường gì.
        -fieldset và legend sử dụng khi có một nhóm các input có liên quan tới nhau với fieldset để tạo nhóm và legend để viết mô tả của nhóm đó.
            +ví dụ: một fieldset nhập thông tin giao hàng với tên người nhận, địa chỉ nhận hàng, sđt người nhận.
            <fieldset>
                <legend>Thông tin giao hàng</legend>
                <label for="name">Họ và tên:</label>
                <input type="text" id="name" name="name" required><br><br>
                <label for="address">Địa chỉ:</label>
                <input type="text" id="address" name="address" required><br><br>
                <label for="phone">Số điện thoại:</label>
                <input type="tel" id="phone" name="phone" required>
            </fieldset>
        -aria-label nên dùng khi phần tử không có mô tả trực tiếp mà chỉ có icon hoặc hình ảnh, khi đó screen reader có thể xác định đúng chức năng của phần tử. aria-label cũng có thể dùng như 1 cách để mô tả chức năng phần tử.
        -dùng aria-label khi đã có label sẽ gây rối loạn thông tin cho screen reader
    C4:
        -loading="lazy": chỉ tải ảnh khi sắp xuất hiện trên màn hình. Không nên dùng với các ảnh ở đầu trang hoặc các hình ảnh quan trọng cần tải sớm.
        -cần nhiều source với mỗi video vì mỗi trình duyệt có thể hỗ trợ các định dạng video khác nhau. nếu 1 định dạng không được hỗ trợ có thể đổi sang 1 định dạng khác.
        -Các định dạng video phổ biến MP4, WebM, Ogg.
        -alt trong img cho 1 văn bản thay thế cho ảnh hỗ trợ screen reader đọc ảnh và hiển thị khi ảnh không tải được.
        -ví dụ alt:
            +iphone 16: iphone 16 màu đen, 256gb.
            +trang trí: để trống tránh gây nhiễu thông tin.
            +biểu đồ doanh thu: Biểu đồ doanh thu quý 1 năm 2026.
    C5:
        -img sử dụng cho 1 ảnh đơn lẻ, không cần chú thích.
        -figure+figcaption sử dụng cho 1 nhóm ảnh, các ảnh cần mô tả chi tiết, biểu đồ, hình minh họa.
Phần B:
    C1:
        -HTML5 không thể kiểm tra trùng khớp password bằng pattern vì pattern chỉ kiểm tra nội dung input không so sánh với giá trị khác.