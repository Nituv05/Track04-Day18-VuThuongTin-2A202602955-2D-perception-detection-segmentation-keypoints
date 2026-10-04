# Chạy và nộp Lab 18

Notebook đã điền các hàm TODO, sửa `FLIP_IDX`, hoàn thành AP bonus và Q1–Q12. Các câu Q2, Q4, Q6–Q8, Q11 lấy số liệu từ kết quả chạy, không dùng số mẫu trong README. Các hàm đã qua 38 phép kiểm tra có sẵn với `ultralytics==8.4.171`. Toàn bộ notebook đã chạy trên server RTX 4090 tại `/mnt/disk3/tinvt/lab18_2d_perception`, gồm train GPU 40 epoch, imgsz 640; bản notebook lấy về giữ nguyên output và có bộ `submission/`.

1. Mở notebook bằng nút Colab trong README (trỏ tới bản đã hoàn thiện trong repo này), hoặc upload `lab_2d_perception_student.ipynb` bằng **File → Upload notebook**.
2. Chọn **Runtime → Change runtime type → T4 GPU**.
3. Chọn **Runtime → Restart session and run all**. Kiểm tra Phần 0 in `device = cuda`; Phần 4 train **40 epoch, imgsz 640**. Giữ trang mở đến khi ô cuối chạy xong.
4. Đọc hình và câu trả lời Q11 dưới 6 ảnh val tệ nhất. Q11 đã phân tích ảnh `Frame_31.jpg` và `Frame_155.jpg` thực tế: dự đoán chân trái/phải tụ gần nhau và bàn chân vươn ra trước bị định vị về gần thân; OKS/sai số được lấy lại từ lần chạy hiện tại.
5. Checklist cuối phải có đủ ✅ ở phần bắt buộc. Ô cuối tạo `submission/ket_qua.json`, `submission/autolabel/bus.txt` và `submission.zip`.
6. Tải **notebook đã chạy có output** qua File → Download → Download .ipynb và tải `submission.zip` từ bảng Files bên trái. Giải nén zip và đưa notebook cùng `submission/` lên repo GitHub public; dán URL repo vào LMS. Không mở PR.

Nếu hết bộ nhớ GPU, giảm `batch=16` thành `batch=8` ở các ô train/val; giữ nguyên 40 epoch và imgsz 640. Lần chạy CPU 3 epoch chỉ để thử pipeline và checklist sẽ không đánh dấu phần train đạt yêu cầu nộp.

Nếu nộp ngay bản đã chạy trên server, dùng notebook có output và thư mục `submission/` trong workspace, không cần chạy lại Colab.

Bonus AP đã bật. Bonus 4C vẫn tùy chọn: đặt `RUN_4C = True` và `TRAIN_IDENTITY = True` để train thêm model và so sánh hai quy ước trên val gốc/val gương. Việc này tốn thêm một lần train; chưa có kết quả 4C hay bài tập ONNX để báo cáo bonus tương ứng.
