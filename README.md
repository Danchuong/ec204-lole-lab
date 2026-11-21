# Lô lẻ Lab — prototype bài tập EC204.R12 (Marketing điện tử, UIT)

Trang thử nghiệm học thuật phục vụ các bài tập tuần 1–6 của môn Marketing điện tử.
**Không phải** trang chính thức của Anfin hay bất kỳ công ty chứng khoán nào; không thu thập dữ liệu cá nhân.

- Sinh viên: Đan Nguyễn Nguyên Chương — MSSV 24520007
- Anchor brand phân tích: Anfin (anfin.vn)
- Keyword mục tiêu của prototype: `đầu tư chứng khoán lô lẻ`

## Nội dung repo

| File | Vai trò trong bài |
|---|---|
| `index.html` | Landing page prototype. Có 2 biến thể hook (`?v=a`, `?v=b`) cho vòng tối ưu tuần 3, event log phía client, CTA gắn UTM. |
| `go.html` | Trang trung gian: hiển thị tham số UTM nhận được, ghi event `click_out`, rồi redirect sang đích. Dùng làm bằng chứng redirect chain / param kept-lost cho tuần 2. |

## Event được ghi

`page_view`, `cta_primary`, `cta_secondary`, `cta_outbound`, `objection_open`, `scroll_depth`, `click_out`.

Mỗi event gồm timestamp ISO, session id, biến thể A/B và các tham số UTM của phiên.
Log lưu ở `localStorage` của người truy cập và tải ra JSON qua link ở footer; đối chiếu chéo với GA4.

## Nguyên tắc tuân thủ

Không mạo danh thương hiệu, không chạy quảng cáo dưới tên thương hiệu, không thu thập dữ liệu cá nhân,
không đăng/mua đánh giá. Redirect chỉ cho phép đúng host `anfin.vn`.
