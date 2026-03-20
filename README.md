PHÂN TÍCH DỮ LIỆU WORLD HAPPINESS REPORT

1. Vấn đề (Problem)
1.1 Giới thiệu
Hạnh phúc là một trong những chỉ số quan trọng phản ánh chất lượng cuộc sống và mức độ hài lòng của con người trong xã hội. Việc phân tích mức độ hạnh phúc giữa các quốc gia giúp hiểu rõ hơn về tác động của các yếu tố kinh tế, xã hội và sức khỏe đối với đời sống con người.
Trong dự án này, bộ dữ liệu World Happiness Report được sử dụng để khám phá các xu hướng và yếu tố ảnh hưởng đến mức độ hạnh phúc trên toàn thế giới. Dữ liệu cung cấp thông tin về điểm hạnh phúc của các quốc gia cùng với nhiều yếu tố liên quan như GDP, sức khỏe, hỗ trợ xã hội và tự do cá nhân.
Mục tiêu của dự án là sử dụng các kỹ thuật trực quan hóa dữ liệu để phân tích và hiểu rõ hơn về các yếu tố ảnh hưởng đến hạnh phúc.

1.2 Câu hỏi nghiên cứu
Dự án nhằm trả lời các câu hỏi sau:
Quốc gia nào có mức độ hạnh phúc cao nhất và thấp nhất?
Những yếu tố nào ảnh hưởng đến mức độ hạnh phúc?
Có mối quan hệ giữa GDP và hạnh phúc không?
Mức độ hạnh phúc có khác nhau giữa các khu vực không?


2. Dữ liệu (Data)
2.1 Mô tả bộ dữ liệu
Bộ dữ liệu được sử dụng là World Happiness Report Dataset, bao gồm thông tin của hơn 150 quốc gia.
Dữ liệu cung cấp điểm số hạnh phúc và các yếu tố liên quan nhằm phân tích mức độ hạnh phúc trên toàn cầu.

2.2 Các biến chính
Các biến quan trọng trong bộ dữ liệu gồm:
Country – Tên quốc gia
Happiness Score – Điểm hạnh phúc
Economy – GDP bình quân đầu người
Family – Hỗ trợ xã hội
Health – Tuổi thọ
Freedom – Tự do lựa chọn
Generosity – Mức độ hào phóng
Corruption – Nhận thức về tham nhũng
Region – Khu vực

2.3 Khám phá dữ liệu
Dữ liệu được xử lý bằng Python với các bước:
Kiểm tra cấu trúc dữ liệu
Kiểm tra kiểu dữ liệu
Kiểm tra giá trị thiếu
Thống kê mô tả (mean, min, max)
Kết quả cho thấy dữ liệu đầy đủ và phù hợp cho việc phân tích.

3. Phân tích và Trực quan hóa (Analysis & Visualization)
Để hiểu rõ các yếu tố ảnh hưởng đến hạnh phúc, nhiều kỹ thuật trực quan hóa dữ liệu đã được áp dụng. Các biểu đồ giúp khám phá mối quan hệ giữa điểm hạnh phúc và các yếu tố quan trọng.

3.1 Quốc gia hạnh phúc nhất và kém hạnh phúc nhất
Hình 1: Điểm hạnh phúc của các quốc gia
Biểu đồ thể hiện 10 quốc gia có điểm hạnh phúc cao nhất và 10 quốc gia có điểm thấp nhất.
Kết quả cho thấy sự khác biệt rõ rệt giữa hai nhóm. Các quốc gia hạnh phúc nhất thường có điểm số trên 7 và chủ yếu thuộc các khu vực phát triển.
Ngược lại, các quốc gia kém hạnh phúc có điểm số thấp hơn nhiều, thường dưới 4.
Điều này cho thấy các yếu tố như kinh tế, sức khỏe và hỗ trợ xã hội có ảnh hưởng lớn đến mức độ hạnh phúc.
<img width="682" height="403" alt="image" src="https://github.com/user-attachments/assets/e39ef049-71c6-4b13-bd0b-2531dfe71d09" />


3.2 Phân bố điểm hạnh phúc
Hình 2: Phân bố điểm hạnh phúc
Biểu đồ histogram thể hiện phân bố điểm hạnh phúc của các quốc gia.
Phần lớn các quốc gia có điểm nằm trong khoảng từ 4 đến 6. Chỉ có một số ít quốc gia có điểm rất cao hoặc rất thấp.
Điều này cho thấy mức độ hạnh phúc trên thế giới tập trung ở mức trung bình.
<img width="576" height="404" alt="image" src="https://github.com/user-attachments/assets/31fd60f5-a9d2-4b4d-9204-fa8ae4cf8abd" />






3.3 Mối tương quan giữa các yếu tố
Hình 3: Ma trận tương quan
Biểu đồ heatmap thể hiện mối tương quan giữa các biến.
Kết quả cho thấy các yếu tố có tương quan mạnh với hạnh phúc gồm:
GDP
Sức khỏe
Hỗ trợ xã hội
Điều này cho thấy các quốc gia có nền kinh tế phát triển, tuổi thọ cao và hệ thống xã hội tốt thường có mức độ hạnh phúc cao hơn.
<img width="667" height="588" alt="image" src="https://github.com/user-attachments/assets/57f76344-bb1d-4d01-84c8-0cd92ead59e3" />



3.4 Mối quan hệ giữa GDP và hạnh phúc
Hình 4: GDP và điểm hạnh phúc
Biểu đồ scatter cho thấy mối quan hệ giữa GDP và điểm hạnh phúc.
Có xu hướng tăng rõ ràng: GDP càng cao thì mức độ hạnh phúc càng cao.
Tuy nhiên, dữ liệu không hoàn toàn tuyến tính, cho thấy ngoài kinh tế còn nhiều yếu tố khác ảnh hưởng đến hạnh phúc.
<img width="508" height="412" alt="image" src="https://github.com/user-attachments/assets/917f54b5-8b85-452e-bf28-9e0ad637ddeb" />






3.5 So sánh theo khu vực
Hình 5: Điểm hạnh phúc theo khu vực
Biểu đồ boxplot so sánh mức độ hạnh phúc giữa các khu vực.
Một số khu vực như châu Âu và Bắc Mỹ có mức hạnh phúc cao hơn, trong khi các khu vực khác có mức thấp hơn và biến động lớn hơn.
Điều này phản ánh sự khác biệt về điều kiện kinh tế và xã hội giữa các khu vực.
<img width="741" height="459" alt="image" src="https://github.com/user-attachments/assets/06ab7c7b-4054-44d9-a41c-0f90ae1d43ca" />








3.6 Tổng hợp kết quả
Từ các biểu đồ, có thể rút ra:
Các quốc gia phát triển có mức độ hạnh phúc cao hơn
Hạnh phúc tập trung ở mức trung bình
GDP có mối quan hệ dương với hạnh phúc
Có sự khác biệt rõ giữa các khu vực
Những kết quả này cho thấy hạnh phúc chịu ảnh hưởng bởi nhiều yếu tố kết hợp.

4. Kết luận (Conclusion)
Dự án đã phân tích dữ liệu hạnh phúc toàn cầu bằng các phương pháp trực quan hóa.
Kết quả cho thấy mức độ hạnh phúc khác nhau rõ rệt giữa các quốc gia và khu vực. Kinh tế đóng vai trò quan trọng, nhưng không phải yếu tố duy nhất.
Các yếu tố như sức khỏe, hỗ trợ xã hội và điều kiện sống cũng góp phần quan trọng vào mức độ hạnh phúc.
Nhìn chung, để nâng cao hạnh phúc, cần có sự kết hợp giữa phát triển kinh tế và cải thiện các yếu tố xã hội.

5. Phụ lục (Code)
Toàn bộ code của dự án được lưu tại:
https://github.com/nicowilliamxvii/TQHDC_CS441


