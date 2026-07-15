# BÀI TẬP VỀ NHÀ - BUỔI 1 (PYTHON BASIC)

---

## Bài 1: Python là ngôn ngữ thông dịch hay biên dịch? Tại sao?

Python được định nghĩa là một **ngôn ngữ thông dịch (Interpreted Language)**. Tuy nhiên, về mặt kỹ thuật, quá trình thực thi của Python là sự kết hợp giữa **biên dịch (Compilation)** và **thông dịch (Interpretation)**.

### Tại sao lại như vậy?

1. **Quá trình dịch ngầm (Biên dịch ra Bytecode):** Khi bạn chạy một file Python (`.py`), trước tiên trình biên dịch của Python sẽ dịch mã nguồn của bạn sang một dạng mã trung gian gọi là **Bytecode** (lưu dưới dạng file `.pyc` trong thư mục `__pycache__`). Bước này giúp tối ưu hóa hiệu suất chạy chương trình.
2. **Quá trình thực thi (Thông dịch trực tiếp):** Sau đó, Bytecode này sẽ được chuyển đến **Python Virtual Machine (PVM)**. Tại đây, trình thông dịch (Interpreter) của PVM sẽ dịch từng dòng Bytecode sang mã máy (Machine Code) để CPU thực thi.

> **Kết luận:** Mặc dù có bước biên dịch trung gian, Python vẫn được gọi là ngôn ngữ thông dịch vì lập trình viên không cần phải tự tay biên dịch code ra file thực thi (như `.exe` trong C/C++) trước khi chạy. Mọi quá trình dịch và chạy đều diễn ra tự động và tuần tự từng dòng tại thời điểm chạy chương trình (Runtime).

---

## Bài 2: Tổng quan về Kiến thức Cơ bản trong Python

### 1. Các kiểu dữ liệu trong Python (Data Types)

Python có các kiểu dữ liệu cơ bản được chia thành các nhóm sau:

| Nhóm kiểu dữ liệu     | Tên kiểu dữ liệu                                              | Ví dụ                                  |
| :-------------------- | :------------------------------------------------------------ | :------------------------------------- |
| **Kiểu số (Numeric)** | `int` (Số nguyên)<br>`float` (Số thực)<br>`complex` (Số phức) | `x = 10`<br>`y = 3.14`<br>`z = 1 + 2j` |
| **Kiểu chuỗi (Text)** | `str` (Chuỗi ký tự)                                           | `name = "Bac"`                         |
| **Kiểu logic**        | `bool` (Boolean)                                              | `is_active = True`                     |
| **Kiểu danh sách**    | `list` (Danh sách có thứ tự, có thể thay đổi)                 | `numbers = [1, 2, 3]`                  |
| **Kiểu bộ**           | `tuple` (Danh sách có thứ tự, không thể thay đổi)             | `coordinates = (10, 20)`               |
| **Kiểu tập hợp**      | `set` (Tập hợp không thứ tự, không trùng lặp)                 | `unique_ids = {101, 102}`              |
| **Kiểu ánh xạ**       | `dict` (Từ điển lưu dạng key-value)                           | `student = {"name": "Bac", "age": 20}` |
| **Kiểu rỗng**         | `NoneType` (Đại diện cho giá trị rỗng)                        | `result = None`                        |

---

### 2. Các toán tử trong Python (Operators)

- **Toán tử số học (Arithmetic Operators):**
  - `+` (Cộng), `-` (Trừ), `*` (Nhân), `/` (Chia lấy số thực)
  - `%` (Chia lấy dư), `//` (Chia lấy nguyên)
  - `**` (Lũy thừa)
- **Toán tử so sánh (Comparison Operators):**
  - `==` (Bằng), `!=` (Khác)
  - `>` (Lớn hơn), `<` (Nhỏ hơn), `>=` (Lớn hơn hoặc bằng), `<=` (Nhỏ hơn hoặc bằng)
- **Toán tử logic (Logical Operators):**
  - `and` (Trả về True nếu cả hai đều đúng)
  - `or` (Trả về True nếu một trong hai đúng)
  - `not` (Phủ định giá trị logic)
- **Toán tử gán (Assignment Operators):**
  - `=`, `+=`, `-=`, `*=`, `/=`, `%=`, `//=`, `**=`
- **Toán tử thành viên (Membership Operators):**
  - `in` (Trả về True nếu giá trị nằm trong tập hợp)
  - `not in` (Trả về True nếu giá trị không nằm trong tập hợp)
- **Toán tử danh tính (Identity Operators):**
  - `is` (Trả về True nếu hai biến cùng trỏ tới một đối tượng)
  - `is not` (Trả về True nếu hai biến trỏ tới hai đối tượng khác nhau)

---

### 3. Mệnh đề điều kiện và vòng lặp (Control Flow)

#### Mệnh đề điều kiện (Conditional Statements)

Sử dụng cấu trúc `if - elif - else` để rẽ nhánh chương trình:

```python
score = 8.5

if score >= 8.0:
    print("Học lực giỏi")
elif score >= 6.5:
    print("Học lực khá")
else:
    print("Học lực trung bình")
```