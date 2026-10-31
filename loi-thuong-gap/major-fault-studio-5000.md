# Major Fault trong Studio 5000: cách đọc và xử lý

Khi bộ điều khiển Logix gặp **Major Fault**, CPU thường dừng chương trình để bảo vệ hệ thống. Điều quan trọng là **đọc đúng thông tin lỗi trước khi xóa lỗi**.

## Bước 1: Xem thông tin lỗi
Trong Studio 5000 Logix Designer, mở **Controller Properties → tab Major Faults**. Bạn sẽ thấy:
- **Type** (loại lỗi) và **Code** (mã lỗi)
- Mô tả và vị trí gây lỗi (routine, rung) nếu có

Chụp lại màn hình trước khi xử lý.

## Bước 2: Phân nhóm nguyên nhân thường gặp
| Nhóm | Dấu hiệu | Hướng kiểm tra |
|---|---|---|
| Lỗi I/O / kết nối | Module mất kết nối | Kiểm tra nguồn, cáp mạng, module bị rút, cấu hình I/O khớp phần cứng |
| Lỗi chương trình | Chỉ số mảng vượt giới hạn, nhảy tới nhãn hoặc routine không tồn tại | Mở đúng routine báo lỗi, kiểm tra chỉ số mảng và lệnh nhảy |
| Watchdog | Thời gian quét vượt giới hạn | Kiểm tra vòng lặp dài, task quá tải, chu kỳ task |
| Mất nguồn / Power-up | Lỗi sau khi cấp điện lại | Kiểm tra Power-Up Handler và vị trí khóa chế độ |

Mã lỗi cụ thể thay đổi theo dòng PLC và phiên bản firmware. **Luôn đối chiếu với tài liệu chính hãng của Rockwell** (Logix 5000 Controllers Major, Minor and I/O Faults, mã 1756-PM014) cho phiên bản bạn đang dùng.

## Bước 3: Sửa nguyên nhân, rồi mới xóa lỗi
1. Sửa nguyên nhân gốc (phần cứng hoặc chương trình).
2. Ở tab Major Faults, chọn xóa lỗi (Clear Majors).
3. Đưa bộ điều khiển trở lại chế độ Run theo quy trình an toàn của nhà máy.

> ⚠️ Xóa lỗi mà chưa hiểu nguyên nhân chỉ khiến lỗi quay lại, đôi khi ở thời điểm tệ hơn. Làm theo quy trình an toàn và khóa nhãn (LOTO) của nhà máy khi can thiệp thiết bị.

Bài đầy đủ hơn trên website: https://haiauautomation.com

---
*Nội dung: Hải Âu Automation, CC BY 4.0.*
