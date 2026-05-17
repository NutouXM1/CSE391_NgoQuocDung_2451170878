Phần A:
    C1:
    Kích thước màn hình   |  <768px(mobile)   |   768-991px(tablet)    |   >=992px(pc)              |
    số cột hiện thị       |      1 cột        |       2 cột            |       4 cột                |
    box layout            |  4 box xếp dọc    |   2 box mỗi hàng       |   4 box trên cùng 1 hàng   |

    col-md-6: cột ở thiết bị có độ rộng hiện thị trong khoảng md(768-991) sẽ có độ rộng 6 đơn vị.
    C2:
    -d-none: ẩn trên tất cả kích thước.
    -d-md-block: màn hình từ md trở lên sẽ hiển thị dưới dạng block.
    -> d-none d-md-block: ẩn trên mobile và hiện trên table và desktop theo kiểu block.
    -5 spacing utilities:
        mt-3: margin top 3px
        px-4: padding trục x(trái, phải) 4px
        mb-auto: margin bottom auto
        py-5: padding trục y(trên dưới) 5px
        mb-9: margin bottom 9px
    -so sánh:
        +container:         có max-width cố định theo breakpoint.
        +container-fluid:   luôn chiếm 100% chiều ngang màn hình, không giới hạn.
        +container-md:      .container nhưng chỉ bắt đầu cố định từ breakpoint md trở lên.