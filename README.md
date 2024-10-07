# Hướng dẫn Hoàn Chỉnh Tạo Issue Trên GitHub Cho Dự Án VitaDairy

**Link tạo issue:** [Tạo Issue Mới](https://github.com/VitaDairy/vtd-community/issues/new?assignees=&labels=&projects=&template=bug.yml)

Trong hướng dẫn này, chúng ta sẽ đi qua các bước chi tiết để tạo một issue đúng cách sử dụng template đã cung cấp trên dự án VitaDairy. Điều này giúp đảm bảo rằng đội ngũ phát triển nhận được đủ thông tin cần thiết để giải quyết vấn đề một cách nhanh chóng.

Chắc chắn rằng bug tạo ra không bị trùng với bất kỳ bug nào trước đây.  

Nếu bug đã tồn tại, vui lòng không tạo bug mới mà tìm ID của bug đó để tiếp tục thảo luận. Chúng tôi sẽ đóng/closed bug của bạn (kèm comment giải thích) nếu phát hiện sự trùng lặp đó.

---

### Bước 1: Truy cập link tạo Issue

Sử dụng link [Tạo Issue Mới](https://github.com/VitaDairy/vtd-community/issues/new?assignees=&labels=&projects=&template=bug.yml), bạn sẽ được đưa đến trang tạo issue với mẫu báo cáo lỗi (bug template) đã được cấu hình sẵn.

Trang issue sẽ hiển thị các trường thông tin để bạn điền vào, bao gồm các phần mô tả chi tiết về vấn đề bạn đang gặp phải.

---

### Bước 2: Tiêu đề Issue (Title)

- **Mục tiêu:** Đảm bảo tiêu đề ngắn gọn và mô tả chính xác vấn đề.
- **Cấu trúc:** "Tính năng hoặc thành phần gặp lỗi – Mô tả ngắn gọn về vấn đề."

Ví dụ:

- "Trang Đăng Nhập – Không thể đăng nhập với tài khoản hợp lệ"
- "API Đặt hàng – Phản hồi sai trạng thái đơn hàng"

**Mẹo:** Tiêu đề nên tóm gọn được vấn đề chính để đội ngũ phát triển dễ dàng nhận diện.

---

### Bước 3: Mô tả Vấn Đề (Description)

**Phần mô tả này đã được cấu hình sẵn qua file bug template với các trường cụ thể. Dưới đây là cách hoàn thành các trường trong mẫu:**

#### 3.1. **Mức độ ưu tiên (Priority)**

- **Câu hỏi:** Vấn đề này có ảnh hưởng lớn đến người dùng hay không?
- **Ví dụ:**
  - High (Cao): Lỗi này ảnh hưởng đến nhiều người dùng hoặc chức năng chính.
  - Low (Thấp): Lỗi nhỏ không ảnh hưởng lớn đến trải nghiệm người dùng.

---

### Xác định mức độ ưu tiên

Để xác định mức độ ưu tiên của bug, vui lòng trả lời các câu hỏi sau:

1. Bug có đang ảnh hưởng trực tiếp đến users của App không?
2. Số lượng users gặp phải bug có lớn hơn 50 cases và đang tăng liên tục không?
3. Bug có xảy ra trên các core functions của App và ngăn người dùng không thực hiện được các chức năng này không?
   (Ví dụ: Tích xu, Đổi quà, Lên đơn, Tham gia event)

=> Nếu tất cả các câu hỏi trên đều là "Có", đây là bug **Critical**.  
=> Nếu bug ảnh hưởng tới một bộ phận users nhưng số lượng case không tăng, xảy ra ở luồng chính, đây là bug **High**.  
=> Nếu bug ảnh hưởng tới một bộ phận users, số lượng case không tăng và không ảnh hưởng ở luồng chính, đây là bug **Normal**.  
=> Nếu bug ảnh hưởng tới một số ít users, không xảy ra ở luồng chính, đây là bug **Low**.

---

### Bug ảnh hưởng đến luồng vận hành admin

Nếu bug không ảnh hưởng đến luồng người dùng app nhưng ảnh hưởng đến luồng vận hành admin trên app và tác động đến việc vận hành app:  
=> Đây là bug **High**.

Nếu bug không ảnh hưởng đến luồng người dùng app, không ảnh hưởng đến luồng vận hành admin trên app nhưng có ảnh hưởng đến vận hành nội bộ của VTD:  
=> Đây là bug **Normal**.

Nếu bug không ảnh hưởng đến luồng người dùng app, không ảnh hưởng đến luồng vận hành admin, và không tác động đến vận hành nội bộ của VTD:  
=> Đây là bug **Low**.

---

#### 3.2. **Hệ điều hành (Operating System)**

- Điền hệ điều hành mà bạn đang gặp vấn đề (ví dụ: iOS, Android, Windows).

Ví dụ:

```markdown
iOS 13, Android 10
```

#### 3.3. **Phiên bản ứng dụng bạn đang sử dụng (App Version)**

- Phiên bản của ứng dụng hoặc hệ thống tại thời điểm gặp vấn đề.

Ví dụ:

```markdown
2.1.4
```

#### 3.4. **Loại Bug (Bug Type)**

- Xác định loại bug (ví dụ: UI/UX, logic, database).

Ví dụ:

```markdown
UI/UX
```

#### 3.5. **Môi trường (Environment)**

- Môi trường bạn đang thử nghiệm (ví dụ: Local, Production, Staging).

Ví dụ:

```markdown
Production
```

#### 3.6. **Ảnh hưởng chức năng khác (Other Function Affected)**

- Liệt kê các chức năng khác bị ảnh hưởng bởi vấn đề này, nếu có.

Ví dụ:

```markdown
Không có chức năng khác bị ảnh hưởng.
```

#### 3.7. **Chi tiết bug (Bug Details)**

- Mô tả chi tiết về vấn đề. Giải thích rõ ràng những gì bạn đã làm và kết quả mong đợi.

Ví dụ:

```markdown
Khi người dùng bấm nút đăng nhập với tài khoản hợp lệ, ứng dụng trả về lỗi và không thể truy cập. Vấn đề xảy ra trên cả iOS và Android. Mong đợi: Người dùng có thể đăng nhập thành công.
```

---

### Bug ảnh hưởng đến luồng vận hành admin

Nếu bug ảnh hưởng đến quy trình vận hành của admin hoặc các luồng quan trọng khác, hãy chỉ rõ trong phần mô tả. Điều này giúp đội ngũ phát triển ưu tiên giải quyết các vấn đề có tác động lớn đến hệ thống.

---

#### 3.8. **Các bước tái hiện (Steps to Reproduce)**

- Liệt kê các bước cụ thể để đội ngũ phát triển có thể tái hiện lỗi.

Ví dụ:

```markdown
1. Mở ứng dụng trên iOS 13.
2. Nhập tài khoản và mật khẩu hợp lệ.
3. Bấm nút đăng nhập.
4. Ứng dụng trả về lỗi "Unable to login".
```

#### 3.9. **Thông báo về ghi chú, dữ liệu, dẫn chứng liên quan (Additional Notes or Documentation)**

- Đính kèm thông tin bổ sung, ảnh chụp màn hình, logs hoặc bất kỳ dữ liệu nào hỗ trợ.

Ví dụ:

```markdown
Log lỗi:
```

```text
[Error] Login failed: Invalid session token.
```

---

### Bước 4: Đính kèm tệp (Attachments)

Nếu bạn có tệp logs, ảnh chụp màn hình hoặc video mô tả vấn đề, hãy đính kèm chúng trong phần "Attach files by dragging & dropping". Các file này sẽ giúp đội ngũ phát triển dễ dàng hơn trong việc xác định vấn đề.

---

### Bước 5: Gửi Issue

Sau khi điền đầy đủ thông tin, hãy bấm nút **"Submit new issue"** để gửi.

---

### Ví dụ hoàn chỉnh về issue

```markdown
# Trang Đăng Nhập – Không thể đăng nhập với tài khoản hợp lệ

## Mức độ ưu tiên

High

## Hệ điều hành

iOS 13, Android 10

## Phiên bản ứng dụng bạn đang sử dụng

2.1.4

## Loại Bug

UI/UX

## Môi trường

Production

## Ảnh hưởng chức năng khác

Không có chức năng khác bị ảnh hưởng.

## Chi tiết bug

Khi người dùng bấm nút đăng nhập với tài khoản hợp lệ, ứng dụng trả về lỗi và không thể truy cập. Vấn đề xảy ra trên cả iOS và Android.

## Các bước tái hiện

1. Mở ứng dụng trên iOS 13.
2. Nhập tài khoản và mật khẩu hợp lệ.
3. Bấm nút đăng nhập.
4. Ứng dụng trả về lỗi "Unable to login".

## Thông báo về ghi chú, dữ liệu, dẫn chứng liên quan

Log lỗi:
[Error] Login failed: Invalid session token.
```

---

### Lưu ý khi tạo issue

- **Cung cấp càng nhiều chi tiết càng tốt.** Đội ngũ phát triển cần biết rõ ràng các bước tái hiện vấn đề.
- **Đảm bảo rằng thông tin bạn cung cấp là chính xác và cập nhật.** Điều này giúp tiết kiệm thời gian của cả hai bên.

Với hướng dẫn này, bạn đã sẵn sàng tạo issue một cách chuyên nghiệp và chi tiết trên dự án VitaDairy.
