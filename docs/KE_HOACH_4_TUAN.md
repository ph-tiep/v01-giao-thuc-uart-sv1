# Kế hoạch 4 tuần — đề V01, phần SV1

Đề tài: **V01 – Giao thức khung dữ liệu UART giữa PC và vi điều khiển**.

Thành viên: **SV1 – Phạm Văn Tiệp**.

Phần phụ trách: đặc tả giao thức (định dạng khung, bảng lệnh, mã lỗi) và FSM phân tích khung trên STM32. Mã nguồn nằm ở `firmware/` (`proto_cfg.h`, `checksum`, `protocol`, `ringbuf`, `proto_uart`) và `docs/DAC_TA_GIAO_THUC.md`.

Mỗi tuần là một nhánh. Nhánh sau được tạo từ nhánh tuần trước, nên lịch sử Git đi đúng thứ tự kế hoạch.

| Tuần | Nhánh | Mục tiêu trong kế hoạch | Việc của SV1 | Sản phẩm trên nhánh |
|---|---|---|---|---|
| 1 | `tuan-1-phan-tich-thiet-ke` | Phân tích, thiết kế, chốt API | Đặc tả khung, bảng lệnh, mã lỗi, máy trạng thái tách khung; chốt file `.h` | `docs/DAC_TA_GIAO_THUC.md`, `firmware/Inc/` |
| 2 | `tuan-2-hoan-thien-module` | Hoàn thiện module riêng, commit trên Git | Viết module theo API đã chốt: checksum, đóng/tách khung, bộ đệm vòng, UART | thêm `firmware/Src/` |
| 3 | `tuan-3-tich-hop-kiem-thu` | Tích hợp và kiểm thử hệ thống | Sửa tầng khung khi ghép với tầng ứng dụng, PC và kịch bản kiểm thử | chưa tới tuần này |
| 4 | `tuan-4-bao-cao-bao-ve` | Báo cáo và bảo vệ | Viết chương báo cáo phần giao thức và sẵn sàng vấn đáp code của mình | chưa tới tuần này |

Nhánh `main` trùng với tuần đã hoàn thành mới nhất.
