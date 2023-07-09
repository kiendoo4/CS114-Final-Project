![image](https://github.com/kiendoo4/final-project/assets/95215777/43cb2a5f-05cf-45e1-8f94-ce07765af616)


**TRƯỜNG ĐẠI HỌC CÔNG NGHỆ THÔNG TIN**

**ĐỒ ÁN CUỐI KỲ MÔN MÁY HỌC - CS114.N21**



**ĐỒ ÁN: DỰ ĐOÁN GIỚI TÍNH CỦA NGƯỜI VIỆT DỰA VÀO HỌ TÊN NGƯỜI ĐÓ**

Lớp: CS114.N21

Giảng viên: TS. Lê Đình Duy, ThS. Phạm Nguyễn Trường An

Thành viên nhóm HKV:

Nguyễn Trung Kiên - 21521024

Nguyễn Sĩ Hùng - 21522119

Phạm Quốc Việt - 21522792

1. Mô tả bài toán
Đề tài dự đoán giới tính một người dựa vào họ tên là đề tài hướng đến việc sử dụng họ và tên của một người để có thể phân loại người đó là nam hay nữ. Trong Machine Learning, đây là dạng bài toán có tên gọi Binary Classification, trong đó bài toán chỉ có hai classes, cũng là hai giới tính cần được phân loại.
1.2. Input và output của bài toán
- Input: Dataset bao gồm họ và tên và giới tính tương ứng
- Output: Họ và tên người cần dự đoán và giới tính được dự đoán của người đó
1.3. Các thuật toán máy học mà đồ án sử dụng
Trong bài báo cáo, nhóm sẽ sử dụng 4 mô hình classification, đó là: Logistics Regression, SVM, Gaussian Naive Bayes và Decision Tree. Sau khi qua các bước xử lý dữ liệu và trích chọn đặc trưng, data được xử lý sẽ đưa vào các mô hình classification và sau cùng đánh giá từng mô hình bằng confusion matrix và giá trị của các metrics: accuracy, precision, recall và f1-score.
1.4. Các tiêu chí về một mô hình được đánh giá tốt
2 tiêu chí mà nhóm sử dụng để đánh giá một mô hình có thể xem là tốt đó là:
- f1-score cao: f1- score là giá trị trung bình điều hòa của precision và recall. Hiểu một cách đơn giản, f1-score cân bằng hai giá trị precision và recall. Đôi khi trong một số trường hợp, tập dữ liệu quá nghiêng về trường hợp positive, giá trị precision sẽ cao nhưng recall thấp, và ngược lại. Hiện tượng này thường được đề cập với tên gọi precision-recall trade-off. Do đó, để tránh việc này, f1-score phải cao thì mới tương ứng với precision cao và recall cao. Nhóm hi vọng f1-score của nhóm đạt trên 90%.
- Confusion matrix: Mô hình tốt là khi confusion matrix có giá trị lớn (đậm đặc về màu sắc) trên đường chéo chính của nó, cho thấy các điểm dữ liệu đã được phân loại đúng là lớn.  

2. Tập dữ liệu
- Nguồn dữ liệu được lấy từ những file excel đã được public của các trường đại học, là danh sách sinh viên của một trường, được các thành viên nhóm tổng hợp lại, xử lý và làm thành file json.
- Dataset ban đầu chứa cả tên một số sinh viên không phải người Việt Nam đã được lược bỏ đi vì quy mô của đề tài, tên của một số người dân tộc được giữ lại để tăng sự đa dạng cho dataset, đây cũng là một tiêu chí mà nhóm đặt ra với dataset của mình.
- Dữ liệu của nhóm chúng em bao gồm 8975 họ và tên, kèm theo đó là giới tính của người đó, nam hoặc nữ. 2 thông tin chính trong file json là full_name (họ và tên) và gender (giới tính) có giá trị được quy ước là 1 với nam giới, và 0 đối với nữ giới.
- Data chứa 16613 người là nam và 12188 người là nữ, hiển thị như hình dưới
3. Mô tả về đặc trưng + feature engineering
- Các features:
+ full_name : họ và tên
+ gender : 0 hoặc 1 (Quy ước: 0 là nữ, 1 là nam)
- Feature extraction xem xét:
+ Đối với văn bản dạng text: PhoBERT, Bag-of-words, n-grams, Tf-Idf
+ Về mặt ngữ nghĩa: Bỏ bớt họ của người đó (Thông thường họ của người Việt Nam là Nguyễn, Trần, Lê, ...)
4. Mô tả thuật toán máy học
+ Classification model: Decision Tree, Support Vector Machine, Multinomial Naive Bayes, Logictics Regression)
6. Đánh giá kết quả, kết luận: Kết quả f1-score cao nhất là 96.11% sử dụng SVM, Bag-of-words và không bỏ bớt họ.
