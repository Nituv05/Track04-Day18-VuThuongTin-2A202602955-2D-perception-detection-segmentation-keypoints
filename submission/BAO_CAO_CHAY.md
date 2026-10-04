# Kết quả chạy Lab 18

- Server: RTX 4090, thư mục `/mnt/disk3/tinvt/lab18_2d_perception`.
- Môi trường: torch 2.5.1+cu121, ultralytics 8.4.171, CUDA.
- Toàn bộ 53 ô code đã chạy, không có output lỗi; notebook giữ 19 hình kết quả.
- Các mục bắt buộc và AP bonus đều đạt kiểm tra, không dùng phao.
- Train YOLO26n-pose: 40 epoch, imgsz 640, seed 0.
- Box mAP50–95: 0.9056.
- Pose mAP50: 0.9950; Pose mAP50–95: 0.4285.
- Có đủ 4 cấu hình latency, 12 câu trả lời và 5 polygon auto-label hợp lệ.
- Q11 được phân tích từ overlay thực tế; mAP50 cao vẫn đi kèm sai số chân và mAP50–95 thấp hơn đáng kể.
- Bonus 4C và bài tập ONNX/auto-label bổ sung chưa chạy.

Notebook được thực thi lại từ đầu bằng kernel mới sau khi hoàn thiện Q6/Q11. Số liệu chi tiết ở `ket_qua.json`; output và hình nằm trong notebook.
