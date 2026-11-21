Đề bài / Yêu cầu

1. Mục tiêu

•	Thiết kế Prompt biến AI thành Mentor hỗ trợ học lập trình.

•	Áp dụng kỹ thuật giải thích đơn giản và đánh giá code theo Rubric.

•	Biết cách xây dựng phản hồi giúp người học cải thiện code.

2. Bối cảnh bài toán

Sinh viên mới học Python thường gặp khó khăn trong việc:

•	Hiểu lỗi trong chương trình.

•	Đánh giá chất lượng code.

•	Biết cách tối ưu và cải thiện bài làm.

Xây dựng Prompt để AI đóng vai:

"Python Programming Mentor hỗ trợ phân tích, chấm điểm và hướng dẫn cải thiện code."

3. Yêu cầu

Xây dựng một Prompt thực hiện 3 nhiệm vụ:

Nhiệm vụ 1: Phân tích code

•	Xác định chức năng chương trình.

•	Tìm lỗi logic và lỗi cú pháp.

•	Giải thích nguyên nhân.

Nhiệm vụ 2: Giải thích cho người mới

•	Sử dụng ngôn ngữ đơn giản.

•	Có ví dụ hoặc ẩn dụ thực tế.

•	Hạn chế thuật ngữ khó.

Nhiệm vụ 3: Chấm điểm theo Rubric

Rubric:

•	Correctness (Đúng chức năng): 40%

•	Algorithm Efficiency (Thuật toán): 30%

•	Code Style (Chất lượng code): 20%

•	Error Handling (Xử lý lỗi): 10%

4. Yêu cầu đầu ra

AI phản hồi gồm:

Giải thích code.

Chương trình này được viết ra để tính điểm trung bình cộng của một danh sách các con số.

Hãy tưởng tượng bạn có một chiếc giỏ đựng các quả táo có cân nặng khác nhau:

Biến tong giống như một chiếc cân điện tử bắt đầu từ số 0, bạn lần lượt bỏ từng quả táo vào để cộng dồn tổng khối lượng.

Biến so_luong đếm xem trong giỏ có tất cả bao nhiêu quả táo.

Cuối cùng, bạn lấy tổng cân nặng chia cho tổng số quả táo để tìm ra cân nặng trung bình của mỗi quả.

Phân tích lỗi.

Đoạn code gốc của bạn đang gặp 2 lỗi khiến chương trình không thể chạy hoặc chạy sai kết quả trong một số trường hợp:

Lỗi cú pháp (Syntax Error) ở dòng 4: Bạn viết for x in danh_sach nhưng lại thiếu dấu hai chấm (:) ở cuối dòng. Trong Python, dấu : bắt buộc phải có để báo hiệu cho máy tính biết khối lệnh bên trong vòng lặp sắp bắt đầu.

Lỗi logic / Lỗi thực thi (ZeroDivisionError) ở dòng 7: Nếu danh sách đầu vào bị rỗng ([]), biến so_luong sẽ bằng 0. Khi thực hiện phép chia tong / so_luong, chương trình sẽ bị sập ngay lập tức vì trong toán học không thể chia một số cho 0.

Bảng điểm Rubric dạng Markdown.

Tiêu chí	Trọng số	Điểm (Thang 10)	Điểm quy đổi	Nhận xét chi tiết

Correctness (Đúng chức năng)	40%	5.0/10	2.0	Tư duy thuật toán đúng nhưng code chưa chạy được do thiếu dấu :.

Algorithm Efficiency (Thuật toán)	30%	7.0/10	2.1	Vòng lặp chạy ổn định, tuy nhiên Python có sẵn hàm sum() và len() giúp code ngắn gọn và chạy nhanh hơn.

Code Style (Chất lượng code)	20%	8.5/10	1.7	Đặt tên biến tiếng Việt không dấu rất rõ ràng, dễ hiểu (tong, danh_sach), thụt lề chuẩn xác.

Error Handling (Xử lý lỗi)	10%	2.0/10	0.2	Chưa kiểm tra trường hợp danh sách rỗng hoặc dữ liệu đầu vào không phải là số.

TỔNG ĐIỂM	100%		6.0/10	Đạt mức trung bình khá, cần sửa lỗi cú pháp và bổ sung bẫy lỗi.

Nhận xét ưu điểm, hạn chế.

Ưu điểm:

Hiểu rõ bản chất của vòng lặp for và cách dùng biến tích lũy (tong += x).

Đặt tên biến có ý nghĩa, không dùng các ký tự vô nghĩa như a, b, c.

Hạn chế:

Còn bất cẩn ở các quy tắc cú pháp cơ bản của Python (quên dấu :).

Chưa lường trước các tình huống ngoại lệ (edge cases) như danh sách trống.

Code Python cải tiến có comment.

def tinh_trung_binh(danh_sach):

# Bước 1: Kiểm tra nếu danh sách rỗng thì trả về 0 để tránh lỗi chia cho 0
    
    if not danh_sach:
    
        return 0

# Bước 2: Sử dụng hàm có sẵn sum() và len() của Python để tối ưu tốc độ
    tong = sum(danh_sach)
    so_luong = len(danh_sach)
    
# Bước 3: Tính và trả về kết quả trung bình cộng
    trung_binh = tong / so_luong
    return trung_binh

# --- Chạy thử nghiệm chương trình ---

diem_so = [8, 7.5, 9, 10]

ket_qua = tinh_trung_binh(diem_so)

print(f"Điểm trung bình là: {ket_qua}")
