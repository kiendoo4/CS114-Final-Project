Mô tả đồ án: Dự đoán giới tính của một người thông qua họ tên (tiếng Việt)
1. Mô tả bài toán
- Input: Tập dataset bao gồm họ và tên, format tiếng Việt + giới tính
- Output: Giới tính của người cần được dự đoán
- Ứng dụng bài toán - WHY:
+ Thử tưởng tượng bạn gặp phải một vấn đề như sau, bạn có một dataset rất lớn với rất nhiều cột, ví dụ, cột họ và tên, giới tính, độ tuổi, địa chỉ nhà, email, ... để phục vụ cho mục đích gì đó. Bỗng nhiên vì một sự cố nào đó mà cột giới tính bị xóa đi. Vì tập dataset có số lượng đối tượng lớn nên việc đi thu thập lại từ đầu sẽ tốn rất nhiều thời gian và chi phí. Do đó, nếu có một mô hình machine learning đủ tin cậy, ta có thể sử dụng nó để dự đoán giới tính mà không phải đi tìm từng người để biết giới tính của họ là gì. Ví dụ này muốn ám chỉ việc con người có thể đoán, nhưng có quá nhiều để đoán, vì thế cần một mô hình machine learning để phục vụ cho việc dự đoán giới tính.
+ Trong thực tế, nhóm cho rằng việc dự đoán giới tính của một người có thể phục vụ cho một số công việc, ví dụ như tiếp thị và quảng cáo sản phẩm. Ví dụ, các công ty cần biết thông tin giới tính của khách hàng để có thể quảng cáo và đưa ra những sản phẩm thích hợp với đặc điểm giới tính của người đó. Hoặc nhằm nghiên cứu sự chênh lệch giới tính trong một phạm vi, khu vực xác định. Hoặc đối với các trang web nhập thông tin user, sau khi người dùng nhập họ và tên của người đó thì ứng dụng đó sẽ tự dự đoán giới tính hiển thị trên màn hình nhằm giúp người dùng tiết kiệm thời gian.
2. Tập dữ liệu
- Mô tả về bộ dữ liệu: Bộ dữ liệu bao gồm xx (họ và tên) kèm theo giới tính của người đó
- Cách thức xây dựng bộ dữ liệu:
- Số lượng, độ đa dạng: khoảng 10000(nếu quá nhiều để Colab xử lý thì sẽ giảm xuống), số lượng giới tính nam và nữ (cần cân bằng hoặc độ chênh lệch ít để tránh việc bị information bias)
- Các thao tác tiền xử lý dữ liệu: crawl data có nhiều hơn 2 thành phần: họ tên với giới tính, thì lượt bỏ đi.
- Phân chia: 80% cho training và 20% cho testing
3. Mô tả về đặc trưng + feature engineering
- Các features:
+ full_name : họ và tên
+ gender : 0 hoặc 1 (Quy ước: 0 là nữ, 1 là nam)
- Feature engineering:
+ Bag-of-words
+ Bỏ bớt họ của người đó (Thông thường họ của người Việt Nam là Nguyễn, Trần, Lê, ...)
4. Mô tả thuật toán máy học
+ Classification model: KNN, Support Vector Machine, Multinomial Naive Bayes, Logictics Regression)
5. Cài đặt, tinh chỉnh tham số: chưa biết, tạm thời chỉ đoán thông qua họ tên. Trong quá trình thực hiện nếu tìm được thêm tham số nào đó giúp cải thiện model thì nhóm sẽ cân nhắc
6. Đánh giá kết quả, kết luận: Nhóm mong muốn kết quả train có accuracy khoảng 90%
