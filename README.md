# E-Commerce User Behavior Optimization & Predictive Analytics

## Tổng quan dự án (Project Overview)

Dự án này tập trung vào việc khai phá dữ liệu hành vi người dùng trên một nền tảng Thương mại điện tử (E-commerce) quy mô lớn. Mục tiêu cốt lõi là giải quyết các bài toán kinh doanh thực tế: Tối ưu hóa phễu chuyển đổi (Conversion Funnel), phân khúc khách hàng (Customer Segmentation) và xây dựng hệ thống gợi ý bán chéo (Cross-selling/Market Basket Analysis).

Dự án bao gồm toàn bộ vòng đời phân tích dữ liệu (End-to-End Pipeline): từ việc xử lý tập dữ liệu thô khổng lồ (10GB+), phân tích khám phá (EDA), ứng dụng thuật toán Machine Learning, cho đến thiết kế Dashboard báo cáo tương tác trên Power BI.

## Công cụ & Công nghệ (Tech Stack)

Xử lý dữ liệu & Tính toán: Python (Pandas, NumPy).

Machine Learning: Scikit-Learn, Mlxtend (K-Means Clustering, Apriori Algorithm).

Trực quan hóa dữ liệu (Data Visualization): Matplotlib, Seaborn, Power BI (DAX, Data Modeling).

Kỹ thuật xử lý Data lớn: Data Chunking, Strategic Sampling.

## Các giai đoạn & Kết quả chính (Key Results & Insights)

1. Xử lý dữ liệu quy mô lớn (Data Engineering)

Thách thức: Tập dữ liệu log thô ban đầu có dung lượng lên tới hơn 10GB, vượt quá khả năng xử lý của RAM tiêu chuẩn, dễ gây tràn bộ nhớ (Memory Crash).

Giải pháp: Sử dụng kỹ thuật chunking trong Pandas kết hợp strategic sampling để đọc, làm sạch và trích xuất ra một tập dữ liệu chuẩn hóa gồm ~674,000 records giữ nguyên các đặc trưng hành vi cốt lõi.

2. Phân tích Khám phá & Nhịp đập hệ thống (Deep EDA)

Phễu chuyển đổi (Conversion Funnel): Phát hiện điểm nghẽn nghiêm trọng (Bottleneck) với Tỷ lệ rớt khách (Drop-off rate) lên tới 94% ngay từ bước Xem sản phẩm (View) sang Thêm vào giỏ (Cart).

Khung giờ vàng (Temporal Dynamics): Hành vi chốt đơn hội tụ mạnh mẽ vào các khung giờ hành chính (10:00 AM và 14:00 - 16:00 PM), trong khi buổi tối tỷ lệ rớt đơn cao do khách hàng có xu hướng "Window Shopping" (chỉ xem giải trí).

3. Machine Learning: Phân cụm khách hàng (K-Means Clustering)

Áp dụng thuật toán K-Means dựa trên các đặc trưng tương tác (Event Score) và giá trị mua hàng, phân tách thành công tệp người dùng thành 3 nhóm:

🥇 Cluster 2 (VIPs): Chỉ chiếm 2.39% lưu lượng nhưng đóng góp 100% doanh thu thực tế. Hành vi mua sắm quyết đoán, nhắm thẳng đồ giá trị cao.

🥈 Cluster 1 (Window Shoppers): Chiếm 57.39%, lướt xem rất nhiều sản phẩm cao cấp nhưng không bao giờ chốt đơn. (Nhóm cần chạy chiến dịch Remarketing/Mã giảm giá).

🥉 Cluster 0 (Active Potentials): Nhóm chuyên săn đồ giá rẻ.

4. Machine Learning: Hệ thống gợi ý bán chéo (Apriori - Market Basket)

Triển khai thuật toán Apriori để khai phá Luật kết hợp (Association Rules) từ các giỏ hàng thành công:

Bóc tách từ hơn 2,000 luật thô xuống 20 luật cấu hình tối ưu.

Phát hiện các "Liên minh Brand" có hệ số cải tiến (Lift) cực cao, ví dụ: Khách hàng mua Nokia có tỷ lệ cực kỳ cao sẽ mua kèm phụ kiện Xiaomi (Lift: 4.16). Thiết lập cơ sở vững chắc cho hệ thống tự động Pop-up bán kèm tại trang thanh toán.

5. Interactive Power BI Dashboard

Xây dựng Dashboard chuẩn Enterprise để theo dõi sức khỏe hệ thống:

Tích hợp các hàm DAX phức tạp để đo lường KPI (Total Traffic, CR, Session Action Count).

Trực quan hóa bản đồ phân tán (Scatter Plot) của mô hình K-Means và biểu đồ ma trận (Matrix) của hệ thống Apriori.


## 📁 Cấu trúc thư mục (Repository Structure)

```text
ecommerce-behavior-analysis/
|
├
├── notebooks/            # Chứa các file Jupyter Notebook xử lý chính
|   ├── 01_data_understanding.ipynb
|   ├── 02_sampling_strategy.ipynb
|   ├── 03_data_processing.ipynb
|   ├── 04_feature_engineering.ipynb
|   ├── 05_EDA.ipynb
|   ├── 06_K-means_clustering.ipynb
|   └── 07_Apriori_association_rules.ipynb
├── dashboard/            # File thiết kế Power BI
|   └── dashboard_powerbi.pdf
├── images/               # Chứa ảnh xuất ra từ biểu đồ Python
└── README.md
```

## Thông tin liên hệ (Contact)

Trần Quang Duy - Data Analytics & AI Enthusiast

Email: [tranquangduy1512@gmail.com]

LinkedIn: [https://www.linkedin.com/in/tr%E1%BA%A7n-quang-duy-ba8b0536a/]
