# NGHIÊN CỨU KHOA HỌC - TÌM HIỂU CƠ BẢN VỀ TRÍ TUỆ NHÂN TẠO (ARTIFICIAL INTELLIGENCE- AI), HỌC MÁY (MACHINE LEARNING - ML) VÀ HỌC SÂU (DEEP LEARNING)

## Giới thiệu

Repo này tập trung vào nghiên cứu cơ bản AI, ML và cách thức triển khai. Mục tiêu chính của dự án là tạo hệ thống dự đoán bệnh trong SmartHealth (y tế thông minh). Chúng tôi sử dụng các công nghệ đám mây (trong quá trình thực hiện sẽ phát sinh các công nghệ mới), ngôn ngữ lập trình Python và thư viện liên quan để thực hiện các phân tích và thử nghiệm hệ thống.

## Mục tiêu
- Xác định được bài toán và phương pháp thực hiện nhằm phục vụ cho Đồ án chuyên ngành (NT114) và Khóa luận tốt nghiệp (NT505).
- Hiểu được kiến thức cơ bản về AI cũng như các phương pháp triển khai FL.
- Tìm được các bộ datasets uy tín và đạt được kết quả mong muốn

## Cấu trúc dự án


```
📂 Asset
 ├── 📂 Image
 ├── 📂 SVG
📂 Note
 ├── 📂 Documentation
📂 Paper
📂 Report
📂 Task
📄 .gitignore
📄 LICENSE
📄 README.md
```

## Cách cài đặt và sử dụng

Để bắt đầu với dự án này, bạn cần cài đặt các thư viện cần thiết bằng cách chạy các lệnh sau:

```bash
# Clone repo
git clone https://github.com/yourusername/your-repo.git
cd your-repo

# Cài đặt các thư viện cần thiết
[Update later]
```

## Kết quả
[Mô tả các kết quả chính của nghiên cứu]


Đóng góp của chúng tôi luôn hoan nghênh các đóng góp từ cộng đồng. Nếu bạn muốn đóng góp, hãy thực hiện theo các bước sau:

- Fork dự án
- Tạo một nhánh mới (git checkout -b feature-name)
- Commit thay đổi của bạn (git commit -m 'Add feature')
- Push nhánh (git push origin feature-name)
- Tạo pull request

## Tác giả

@andreafletcherdinh - 22520101@gm.uit.edu.vn

@22520117Bao - 22520117@gm.uit.edu.vn

Nếu bạn có bất kỳ câu hỏi nào về dự án, vui lòng liên hệ với chúng tôi qua một trong các email trên hoặc tạo issue trên GitHub.

## License
Dự án này sử dụng giấy phép Apache License 2.0. Xem thêm chi tiết tại file LICENSE.


```mermaid
flowchart TD
    subgraph Client_1[Client 1 - Hospital A]
        C1_I[Image Data] & C1_T[Text Data] --> C1_P[Local Preprocessing]
        C1_P --> C1_F[Feature Extraction]
        C1_F --> C1_M[Local Multimodal Model]
        C1_M --> C1_T1[Local Training]
    end

    subgraph Client_2[Client 2 - Hospital B]
        C2_I[Image Data] & C2_T[Text Data] --> C2_P[Local Preprocessing]
        C2_P --> C2_F[Feature Extraction]
        C2_F --> C2_M[Local Multimodal Model]
        C2_M --> C2_T1[Local Training]
    end

    subgraph Client_N[Client N - Hospital N]
        CN_I[Image Data] & CN_T[Text Data] --> CN_P[Local Preprocessing]
        CN_P --> CN_F[Feature Extraction]
        CN_F --> CN_M[Local Multimodal Model]
        CN_M --> CN_T1[Local Training]
    end

    subgraph Server[Federated Server]
        MA[Model Aggregation - FedAvg] --> GM[Global Model Update]
        GM --> QC[Quality Control]
    end

    subgraph Security[Security Layer]
        E[Encryption]
        DP[Differential Privacy]
        Auth[Authentication]
    end

    C1_T1 --> Security
    C2_T1 --> Security
    CN_T1 --> Security
    Security --> Server
    QC --> Client_1
    QC --> Client_2
    QC --> Client_N
```