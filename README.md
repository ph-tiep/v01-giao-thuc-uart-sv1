# V01 – Giao thức khung UART (phần SV1)

Đề tài mức vừa **V01**: giao thức khung dữ liệu UART giữa PC và vi điều khiển STM32.

**SV1: Phạm Văn Tiệp** — đặc tả giao thức và tầng khung trên board.

## Việc của SV1

- Định dạng khung, bảng lệnh, mã lỗi.
- Máy trạng thái tách khung, đồng bộ lại khi có rác hoặc sai CRC.
- Checksum (SUM-8, CRC-8, CRC-16), bộ đệm vòng, nhận/gửi UART.

Đặc tả đầy đủ: [docs/DAC_TA_GIAO_THUC.md](docs/DAC_TA_GIAO_THUC.md).

Kế hoạch 4 tuần và tên nhánh: [docs/KE_HOACH_4_TUAN.md](docs/KE_HOACH_4_TUAN.md).

## Nhánh

| Nhánh | Tuần |
|---|---|
| `tuan-1-phan-tich-thiet-ke` | Đặc tả và API (file `.h`) |
| `tuan-2-hoan-thien-module` | Mã nguồn tầng khung (`firmware/Src`) |
| `main` | Trùng với tuần đã xong mới nhất |

## Mã nguồn

```
firmware/Inc/proto_cfg.h     cấu hình checksum, chế độ nhận, kích thước bộ đệm
firmware/Inc/checksum.h      SUM-8, CRC-8, CRC-16
firmware/Inc/protocol.h      định dạng khung, lệnh, mã lỗi, bộ tách khung
firmware/Inc/ringbuf.h       bộ đệm vòng
firmware/Inc/proto_uart.h    nhận/gửi khung qua UART
firmware/Src/                hiện thực các module trên
```
