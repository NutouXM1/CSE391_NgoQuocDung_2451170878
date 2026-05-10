Phần A:
    C1:
static      có chiếm chỗ trong flow         không tham chiếu                        có cuộn theo trang      không cần kiểm soát vị trí đặc biệt

relative    có chiếm chỗ trong flow         tham chiếu chính nó                     có cuộn theo trang      cần dịch chuyển nhẹ và giữ layout

absolute    không chiếm chỗ trong flow      tham chiếu thẻ cha gần nhất(nếu có)     có cuộn theo trang      pop-up, layout phức tạp

fixed       không chiếm chỗ trong flow      tham chiếu viewport                     không cuộn theo trang   cần cố định element

sticky      có chiếm chỗ trong flow         tham chiếu chính nó                     không cuộn theo trang   
    C2:(text art)
    -Trường hợp 1:
        [ item1 ][ item2 ][ item3 ][ item4 ]
    -Trường hợp 2:
        [ item1 ][ item2 ]
        [ item3 ][ item4 ]
        [ item5 ][ item6 ]
    -Trường hợp 3:
        item1 ___ item2 ___ item3
    -Trường hợp 4:
        [200px][   1fr   ][200px]
        [ item1 ][ item2 ][ item3 ]
    -Trường hợp 5:
        [ item1 ][ item2 ][ item3 ]
        [ item4 ][ item5 ][ item6 ]
        [ item7 ]