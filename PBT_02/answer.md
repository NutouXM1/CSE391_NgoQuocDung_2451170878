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
Phần C:
    C1:
        -Dòng 1 thiếu thuộc tính action và method của form, vi phạm validation
        sửa: <form action="#" method="post">
             ...
             </form>
        -Dòng 2 trường nhập tên thiếu label, vi phạm accessibility
        sửa: <label for="name">Tên</label>
             <input type="text" id="name">
        -Dòng 4 trường nhập email thiếu label, vi phạm accessibility
        sửa: <label for="email">Email</label>
             <input type="email" id="email" placeholder="email của bạn">
        -Dòng 6 trường nhập password thiếu label, vi phạm accessibility
        sửa: <label for="password">Mật khẩu</label>
             <input type="password" id="password" placeholder="Mật khẩu">
        -Dòng 7 trường nhập lại password thiếu label, vi phạm accessibility
        sửa: <label for="re_password">Nhập lại</label>
             <input type="password" id="re_password" placeholder="Nhập lại mật khẩu">
        -Dòng 9 trường nhập sđt thiếu label, nhận sai kiểu dữ liệu, có dữ liệu tĩnh được cho sẵn, vi phạm validation và accessibility.
        sửa: <label for="phone_number">Số điện thoại</label>
             <input type="tel" pattern="[0-9]{10}" placeholder="0901234567">
        -Dòng 11-14 chưa có label cho hộp chọn, thiếu placeholder, vi phạm accessibility và best practices
        sửa: <label for="city">Thành phố:</label>
             <select id="city" name="city" required>
                <option value="">--Chọn thành phố--</option>
                <option value="hanoi">Hà Nội</option>
                <option value="hcm">TP.HCM</option>
             </select>
        -Dòng 16-18 chưa có input cho người dùng đồng ý, vi phạm validation
        sửa: <input type="checkbox" id="agreement" required>
             <label for="agreement">Tôi đồng ý điều khoản</label>
    C2:
        -Regex cho CMND/CCCD và Số tài khoản
            +CMND/CCCD: Phải đúng 12 chữ số → pattern="^\d{12}$"
            +Số tài khoản: Từ 10 đến 15 chữ số → pattern="^\d{10,15}$"
        -HTML5 validation có an toàn không với ngân hàng?
            +HTML5 validation chưa đủ an toàn cho ngân hàng
            +Bởi HTML5 validation chỉ hoạt động ở trình duyệt phía khách hàng (frontend), người dùng có thể disable hoặc chỉnh sửa bằng DevTools.
            +Ngân hàng phải verify lại dữ liệu trên server (backend).
        -3 việc HTML5 validation không thể thực hiện
            +Validate dữ liệu có xuất hiện trong hệ thống (như check xem số tài khoản đó đã được đăng ký hay chưa)
            +Validate logic phức tạp (chẳng hạn như mật khẩu phải chứa ít nhất 1 chữ in hoa, 1 ký tự đặc biệt)
            +Validate comparison between 2 fields (ví dụ “Nhập lại mật khẩu” phải giống mật khẩu).
        -Two security risks khi chỉ validate frontend
            +Người dùng có thể bypass HTML5 validation thông qua việc disable JavaScript hoặc chỉnh sửa HTML.
            +Hackers cũng có thể bypass HTML5 validation bằng cách gửi các dữ liệu