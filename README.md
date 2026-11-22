# GOOGLE SEARCH CONSOLE - BULK REMOVALS 
📌 Tiện ích giải quyết vấn đề yêu cầu xoá url hàng loạt trên GSC ⚡

### Tải xuống và sử dụng: [▶ Xem hướng dẫn trên YouTube](https://youtu.be/dZkCfoxTK0M)
- **Bước 1:** Tải xuống file zip [sevn_gscremovals.zip](https://github.com/7vnguyenvu/sevn_gscremovals/archive/refs/heads/main.zip) hoặc clone mã nguồn từ repository.
- **Bước 2:** Mở trình duyệt Chrome (hoặc Edge, Cốc Cốc, Brave...) và truy cập `chrome://extensions`.
- **Bước 3:** Bật chế độ **"Developer mode"** (Chế độ dành cho nhà phát triển) ở góc trên bên phải.
- **Bước 4:** Bấm **"Load unpacked"** (Tải tiện ích đã giải nén) và chọn thư mục `dist/` (hoặc thư mục nguồn chứa tiện ích).
- **Bước 5:** Truy cập vào Google Search Console -> Chọn đúng tài sản cần xử lý -> Vào mục **Xóa URL (Removals)**.
- **Bước 6:** Bấm vào biểu tượng tiện ích trên thanh công cụ trình duyệt:
  - Dán danh sách URL vào ô nhập (mỗi dòng 1 URL).
  - Chọn 1 trong 3 chế độ:
    - *Chỉ xóa URL này (Remove this URL only)*
    - *Xóa URL có tiền tố này (Remove all URLs with this prefix)*
    - *Hủy yêu cầu (Cancel request)*
  - (Tùy chọn) Bật checkbox *"Tự động Cancel request nếu trùng lặp & đang Processing/Temporarily removed"*.
  - (Tùy chọn) Điều chỉnh khoảng nghỉ giữa các URL: từ `0.75s` đến `1.5s`.
  - Bấm nút **Bắt đầu**.
- **Bước 7:** Bạn có thể đóng popup tiện ích hoặc chuyển sang tab khác làm việc bình thường. Khi hoàn tất, mở lại tiện ích và bấm **"Copy bảng kết quả"** để dán trực tiếp vào Google Sheets hoặc Excel.

---

### ✨ Tính năng nổi bật
- 🚀 **Chạy ngầm độc lập (Background Service Worker MV3):** Toàn bộ tiến trình chạy ở Background. Bạn có thể thoải mái đóng popup, tắt cửa sổ popup hoặc chuyển sang làm việc khác mà tiến trình vẫn tiếp tục chạy mượt mà.
- ⚡ **Điều chỉnh Delay linh hoạt (0.75s – 1.5s):** Tinh chỉnh khoảng nghỉ giữa các URL bằng nút `+` / `-` hoặc nhập trực tiếp (mặc định 0.75s), cập nhật tức thì ngay cả khi đang chạy.
- 🎯 **3 Chế độ xử lý toàn diện:**
  - **Chỉ xóa URL này:** Xóa chính xác từng URL đơn lẻ.
  - **Xóa URL có tiền tố này:** Xóa toàn bộ URL có chung prefix/thư mục.
  - **Hủy yêu cầu (Cancel request):** Tính năng riêng biệt giúp hủy hàng loạt các yêu cầu xóa đang chờ xử lý (`Processing request`) hoặc đã xóa tạm thời (`Temporarily removed`).
- 🔄 **Tự động Cancel & Submit lại nếu trùng lặp:** Tùy chọn thông minh tự động tìm kiếm trong bảng GSC, hủy yêu cầu cũ đang bị trùng và ngay lập tức gửi lại yêu cầu mới không có thời gian chết.
- 📑 **Hỗ trợ phân trang tự động:** Tự động trở về Trang 1 và duyệt qua các trang của bảng lịch sử GSC để tìm kiếm URL cần hủy.
- ⏯ **Quản lý tiến trình an toàn (Tạm dừng / Tiếp tục / Dừng hẳn):** 
  - *Tạm dừng (Pause):* Chờ xử lý nốt URL hiện tại rồi dừng an toàn, không làm hỏng trạng thái form.
  - *Tiếp tục (Resume):* Tiếp tục chạy tiếp danh sách còn lại mà không cần nhập lại.
  - *Dừng hẳn (Stop):* Dừng hẳn tiến trình và tự động dọn dẹp các form/modal đang mở trên trang.
- 📊 **Theo dõi trực quan qua Badge icon:** Hiển thị trực tiếp số URL còn lại ngay trên icon extension trên thanh công cụ.
- 📋 **1-Click Copy sang Google Sheets / Excel:** Dữ liệu nhật ký được định dạng chuẩn bảng (TSV): STT, Thời gian, URL, Trạng thái (Thành công, Đã hủy, Trùng lặp, Không thuộc tài sản, Hết quota, Lỗi), Chi tiết lỗi rõ ràng. Chỉ cần Ctrl + V là dán vào Google Sheets tự động tách cột.
