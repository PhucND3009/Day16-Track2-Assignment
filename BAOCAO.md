Benchmark LightGBM trên CPU t3.medium cho thời gian load dữ liệu khoảng 2.31 giây và thời gian training khoảng 2.52 giây, cho thấy mô hình có thể huấn luyện khá nhanh trên CPU.
Mô hình đạt AUC-ROC 0.9517, thể hiện khả năng phân biệt tốt giữa giao dịch bình thường và giao dịch gian lận.
Accuracy đạt 99.89%, tuy nhiên do dữ liệu Credit Card Fraud có độ mất cân bằng cao nên không nên chỉ dựa vào Accuracy để đánh giá mô hình.
F1-Score đạt 0.7273, với Precision 0.6557 và Recall 0.8163.
Recall tương đối cao cho thấy mô hình phát hiện được phần lớn các giao dịch gian lận trong tập test.
Inference latency cho một dòng dữ liệu khoảng 1.21 ms, phù hợp với các tác vụ cần dự đoán nhanh.
Khi dự đoán theo batch 1000 dòng, throughput đo được khoảng 685,642 rows/s trong benchmark này.
Nhìn chung, LightGBM cho hiệu năng tốt trên CPU cả về thời gian training, chất lượng phân loại và tốc độ inference mà không cần sử dụng GPU.