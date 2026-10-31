# PLC là gì?

**PLC (Programmable Logic Controller)** là bộ điều khiển logic khả trình: một máy tính công nghiệp chuyên dùng để điều khiển máy móc và dây chuyền theo chương trình do kỹ sư viết.

## Thành phần cơ bản
- **CPU:** chạy chương trình điều khiển.
- **Nguồn:** cấp điện cho bộ điều khiển và các module.
- **Module ngõ vào (Input):** nhận tín hiệu từ nút nhấn, cảm biến, công tắc hành trình.
- **Module ngõ ra (Output):** điều khiển contactor, van, đèn báo, biến tần.
- **Truyền thông:** kết nối HMI, biến tần, PLC khác qua mạng như EtherNet/IP.

## Vòng quét (scan cycle)
PLC lặp đi lặp lại rất nhanh bốn bước:
1. Đọc trạng thái các ngõ vào.
2. Thực hiện chương trình từ trên xuống dưới.
3. Cập nhật các ngõ ra.
4. Xử lý truyền thông và chẩn đoán.

Hiểu vòng quét giúp bạn giải thích vì sao thứ tự các rung trong chương trình có thể ảnh hưởng đến kết quả.

## Ngôn ngữ lập trình
Phổ biến nhất là **Ladder Logic** (giống sơ đồ rơ-le), ngoài ra còn Function Block Diagram, Structured Text và Sequential Function Chart.

## PLC Rockwell Allen-Bradley
Dòng thường gặp là **CompactLogix** (máy vừa và nhỏ) và **ControlLogix** (hệ thống lớn), lập trình bằng **Studio 5000 Logix Designer**.

## Thử ngay
Viết mạch Start/Stop tự giữ đầu tiên trong [Ladder Lab](https://lab.haiauautomation.com).

---
*Nội dung: Hải Âu Automation, CC BY 4.0. Học bài bản tại https://haiauautomation.com*
