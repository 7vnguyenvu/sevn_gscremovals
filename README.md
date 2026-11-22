# GOOGLE SEARCH CONSOLE - BULK REMOVALS 
📌 Tiện ích yêu cầu xoá URL hàng loạt trên Google Search Console (GSC) ⚡

### Tính năng nổi bật (v1.1)
- 🚀 **Chạy ngầm độc lập (Background Service Worker):** Toàn bộ tiến trình xử lý nằm ở Background. Người dùng có thể thoải mái đóng popup, click ra ngoài màn hình hoặc chuyển sang tab/công việc khác mà tiện ích vẫn chạy bình thường.
- 📊 **Theo dõi tiến độ trực quan:** Hiển thị số lượng URL đang chạy trực tiếp trên icon tiện ích (Badge) và trong popup.
- 📝 **Nhật ký & Báo cáo chi tiết:** Ghi nhận thời gian, URL, trạng thái (*Thành công*, *Trùng lặp*, *Lỗi*) và thông tin chi tiết.
- 📋 **1-Click Copy sang Google Sheets:** Nút copy xuất dữ liệu chuẩn TSV, dán (Ctrl + V) vào Google Sheets hoặc Excel là tự động khớp từng cột hoàn hảo.

---

### Build bản phát hành
- Cài Node.js, sau đó chạy:
  ```bash
  npm install
  npm run build
  ```
- Thư mục `dist/` là bản đã sẵn sàng nạp vào Chrome.
- File `gsc-bulk-remove.zip` dùng để chia sẻ hoặc phát hành lên GitHub Releases.

---

### Hướng dẫn cài đặt và sử dụng
- **Bước 1:** Tải xuống file zip từ GitHub Release hoặc giải nén mã nguồn.
- **Bước 2:** Mở trình duyệt Chrome và truy cập `chrome://extensions`.
- **Bước 3:** Bật chế độ **"Developer mode"** (Chế độ dành cho nhà phát triển) ở góc trên bên phải.
- **Bước 4:** Bấm **"Load unpacked"** (Tải tiện ích đã giải nén) và chọn thư mục `dist/` (hoặc thư mục nguồn tiện ích).
- **Bước 5:** Truy cập vào Google Search Console -> Mục **Xóa URL (Removals)**.
- **Bước 6:** Bấm vào icon tiện ích trên thanh công cụ:
  - Dán danh sách URL cần xóa vào ô nhập (mỗi dòng 1 URL).
  - Chọn chế độ *Chỉ xóa URL này* hoặc *Xóa URL có tiền tố này*.
  - Nhấn nút **Bắt đầu**.
- **Bước 7:** Bạn có thể đóng popup hoặc chuyển sang làm việc khác. Sau khi hoàn thành, mở lại tiện ích và bấm **"Copy cho GG Sheet"** để lưu lại báo cáo.
