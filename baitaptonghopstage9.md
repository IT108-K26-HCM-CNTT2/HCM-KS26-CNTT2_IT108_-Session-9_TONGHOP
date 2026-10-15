
# PHẦN 1 & PHẦN 2: TÀI LIỆU README.MD DỰ ÁN SMARTCAMPUS

# SmartCampus 

![Logo SmartCampus](https://via.placeholder.com/150 "SmartCampus Logo")

**SmartCampus** là *ứng dụng di động* giúp sinh viên PTIT tra cứu lịch học, phòng học trống và nhận các thông báo mới nhất từ nhà trường một cách nhanh chóng.

* Trang chủ CLB Lập trình: [CLB Lập Trình PTIT](https://clblaptrinh.ptit.edu.vn)

### Tính năng đã hoàn thành:
- Tra cứu lịch học theo mã sinh viên
  - Tự động đồng bộ lịch học theo từng học kỳ
- Xem danh sách phòng trống theo tòa nhà

>  **Cảnh báo:** Dự án hiện đang trong giai đoạn thử nghiệm và phát triển, chưa được sử dụng cho các mục đích chính thức của nhà trường.

---

## :rocket: Hướng dẫn Cài đặt & Kỹ thuật

### 1. Hướng dẫn chạy dự án (Installation)
Chạy các lệnh sau trong Terminal (Bash) để khởi chạy ứng dụng:

```bash
git clone https://github.com/clb-lap-trinh/smartcampus.git
npm install
npm start
```

### 2. Tiến độ phát triển (Task List)
- [x] Tra cứu lịch học theo mã sinh viên
- [x] Xem danh sách phòng trống theo tòa nhà
- [ ] Thông báo đẩy (push notification)
- [ ] Đăng nhập bằng tài khoản trường

### 3. Bảng thư viện sử dụng

| Thư viện | Phiên bản | Mục đích |
| :--- | :---: | ---: |
| React Native | 0.74 | Xây giao diện đa nền tảng iOS/Android |
| Axios | 1.6 | Gọi API lấy dữ liệu lịch học |

\# Lưu ý: Sử dụng cú pháp escape `\#` và `\*` để hiển thị nguyên văn dấu `#` hoặc `*` mà không bị biến thành Heading hay chữ in nghiêng.

---

# PHẦN 3: HỎI AI VỀ API VÀ LƯU TÀI LIỆU TRA CỨU

### 1. Prompt 3 phần dùng để hỏi AI:

## Tôi là ai / Bối cảnh
Em là sinh viên năm nhất ngành CNTT và mới tham gia dự án SmartCampus. Em đang tìm hiểu về cách ứng dụng kết nối với máy chủ nhưng chưa hiểu rõ thuật ngữ API.

## Chủ đề / Nội dung cần xử lý
Giải thích khái niệm thuật ngữ kỹ thuật API.

## Yêu cầu
- Giải thích bằng ví dụ thực tế dễ hình dung nhất (như người phục vụ trong nhà hàng).
- Trình bày ngắn gọn, chia thành các gạch đầu dòng rõ ràng.
- Nêu rõ vai trò của API trong ứng dụng di động SmartCampus.

## Không cần
- Không sử dụng từ ngữ quá chuyên ngành sâu hoặc lý thuyết học thuật phức tạp.
- Không viết code mẫu.

---

### 2. Tóm tắt câu trả lời của AI (Đọc 3 bước theo lời của em):
* **Tóm tắt 3 câu:** API đóng vai trò như một "người đưa thư" giúp ứng dụng di động gửi yêu cầu và nhận dữ liệu phản hồi từ máy chủ. Ví dụ như khi sinh viên gõ mã số sinh viên trên app SmartCampus, API sẽ chuyển mã đó về server và mang kết quả lịch học quay lại hiển thị trên màn hình điện thoại. Nhờ có API, ứng dụng không cần phải lưu trữ toàn bộ dữ liệu trường học trực tiếp trên máy của người dùng.

---

### 3. Nội dung tài liệu lưu file `api_giai_thich.md`:

```markdown
# Tài liệu tra cứu: Khái niệm API đơn giản

## API là gì?
API (Application Programming Interface) là giao diện lập trình ứng dụng, đóng vai trò làm cầu nối trung gian cho phép hai ứng dụng hoặc hệ thống phần mềm trò chuyện và trao đổi dữ liệu với nhau.

## Ví dụ thực tế: Dịch vụ trong nhà hàng
- **Bạn (Người dùng):** Khách hàng ngồi tại bàn xem menu và đặt món.
- **Nhà bếp (Server):** Nơi chứa nguyên liệu và chế biến thức ăn (chứa dữ liệu).
- **Phục vụ bàn (API):** Lấy yêu cầu gọi món từ bạn mang xuống bếp, sau đó bưng món ăn từ bếp lên cho bạn.

## Vai trò của API trong ứng dụng SmartCampus
- Kết nối ứng dụng di động với cơ sở dữ liệu của nhà trường.
- Truy xuất danh sách phòng trống và lịch học theo mã sinh viên theo thời gian thực.
- Giúp ứng dụng hoạt động nhẹ nhàng mà không cần lưu trữ dữ liệu khổng lồ trên máy người dùng.
```

---

# PHẦN 4: BẪY CÚ PHÁP & CÁCH SỬA

### 1. Chỉ ra 2 lỗi cú pháp trong đoạn code mã nguồn mẫu:
1. **Lỗi ở phần Bảng (Table):** Bị thiếu dòng phân cách tiêu đề `| --- | --- |` nằm ngay dưới hàng tiêu đề `| Tính năng | Trạng thái |`.
2. **Lỗi ở phần Task List:** Dấu gạch ngang bị viết dính liền với dấu ngoặc vuông (`-[x]`). Quy tắc bắt buộc phải có ít nhất một khoảng trắng ở giữa (`- [x]`).

### 2. Đoạn mã Markdown đã được sửa:

| Tính năng | Trạng thái |
| :--- | :--- |
| Tra cứu lịch học | Xong |
| Push notification | Đang làm |

- [x] Tra cứu lịch học
- [ ] Push notification