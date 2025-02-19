# <center>TÌM HIỂU VỀ MACHINE LEARNING (ML) </center>

- Contributor: @andreafletcherdinh (22520101@gm.uit.edn.vn), @22520117Bao (22520117@gm.uit.edu.vn)
- GVHD: Thầy ThS. Nguyễn Khánh Thuật
- Ngày báo cáo: 26-Sep-2024, E3.1

## Định nghĩa 

- `Machine Learning` (viết tắt là ML) là một tập con của AI (Artificial Intelligence), có tên khác là máy học, nó có khả năng giúp máy tính học hỏi dựa trên dữ liệu đưa vào mà không cần phải lập trình cụ thể.

- Phân biệt khái niệm `Artificial Intelligence`, `Machine Learning`, `Deep Learning`: 
    + Al- `Artificial Intelligence` hay còn gọi là trí tuệ nhân tạo, là lĩnh xây dựng các hệ thống có cấu trúc mô phỏng não bộ con người giúp chúng có thể “tư duy”, xử lý vấn đề và cải thiện theo thời gian.

    + ML - `Machine Learning` , là một nhánh con của AI, trong đó các hệ thống có khả năng học hỏi từ dữ liệu và cải thiện kết quả dự đoán mà không cần được lập trình cụ thể để thực hiện từng tác vụ. ML sử dụng các thuật toán và mô hình để "học" từ dữ liệu, nhận ra các mẫu và dự đoán kết quả.

    + DL - `Deep Learning` hay Học sâu, là một nhánh nâng cao của `Machine Learning`, trong đó các thuật toán dựa trên **mạng nơ-ron nhân tạo**(Artificial Neural Networks - ANN) với nhiều lớp (do đó gọi là "deep" - sâu).



- So sánh cách thức hoạt động của `Machine Learning` và `Deep learning`:

    + Cách thức vận hành: Cả hai đều tiếp nhận dữ liệu đầu vào

        * `Machine Learning` sẽ phụ thuộc vào những thuật toán có sẵn để phân tích và xử lý vấn đề.

        * `Deep learning` thì có khả năng tự bóc tách, điều phối các lớp lọc của mình và cho ra phương án không những tối ưu mà còn hiệu quả nhất thông qua việc đối chiếu "kinh nghiệm" của mình.

    => `Machine learning` nổi bật với khả năng tối ưu thì `Deep learning` vừa tối ưu vừa tìm ra cách xử lý mới.

    + Mức độ giám sát của con người: 

        * `Machine Learning` được giám sát từ xa, hoặc được kiểm soát bởi con người, tùy phân loại.

        * `Deep Learning` hoạt động dộc lập cao hơn, dựa vào setup ban đầu và tự vận hành để tìm ra sáng kiến mới.


## Phân nhóm các thuật toán Machine learning

- Một là dựa trên **phương thức học** (learning style), hai là dựa trên **chức năng** (function) (của mỗi thuật toán):

    + Theo phương thức học, các thuật toán `Machine Learning` thường được chia làm 4 nhóm: **Supervised learning** (Học có giám sát), **Unsupervised learning** (Học không giám sát), **Semi-supervised learning** (Học bán giám sát) và **Reinforcement learning** (Học Củng Cố). Có một số cách phân nhóm không có Semi-supervised learning hoặc Reinforcement learning.

    + Có một cách phân nhóm thứ hai dựa trên chức năng của các thuật toán, trong phần này chỉ liệt kê các thuật toán: **Regression Algorithms**, **Classification Algorithms**, **Instance-based Algorithms**, ...


## Supervised Learning (Học có giám sát)

- `Supervised learning` là thuật toán dự đoán đầu ra (outcome) của một dữ liệu mới (new input) dựa trên các cặp (input, outcome) *đã biết từ trước*. Cặp dữ liệu này còn được gọi là (data, label), tức (dữ liệu, nhãn).

=> Dữ liệu huấn luyện đã có sẵn các cặp đầu vào và đầu ra chính xác, và nhiệm vụ của mô hình là học cách dự đoán đầu ra từ đầu vào.

- Thuật toán `Supervised learning` còn được tiếp tục chia nhỏ ra thành hai loại chính:

    + `Classification` (Phân loại): Một bài toán được gọi là classification nếu các label của input data được chia thành một số hữu hạn nhóm. 

    => Dự đoán một **nhãn cụ thể** từ một tập hợp các nhãn xác định trước. Kết quả đầu ra thường là **dữ liệu rời rạc** (discrete), chẳng hạn như "mèo" hoặc "chó", "bệnh" hoặc "không bệnh".

    + `Regression` (Hồi quy): dự đoán **giá trị liên tục**. Kết quả đầu ra là một biến số liên tục như giá trị thực tế (ví dụ: dự đoán giá nhà, nhiệt độ).

## Unsupervised Learning (Học không giám sát)

- Trong thuật toán này, chúng ta không biết được outcome hay nhãn mà chỉ có dữ liệu đầu vào.

- Các bài toán `Unsupervised learning` được tiếp tục chia nhỏ thành hai loại:

    + `Clustering` (phân nhóm): phân nhóm toàn bộ dữ liệu X thành các nhóm nhỏ dựa trên **sự liên quan** giữa các dữ liệu trong mỗi nhóm.

    Ví dụ: Mô hình clustering sẽ tự động chia khách hàng thành các nhóm dựa trên các đặc điểm mua sắm giống nhau

    + `Association` (liên kết): tìm ra các **mối quan hệ** hoặc **luật liên kết** giữa các mục dữ liệu

    Ví dụ: Mô hình học từ dữ liệu mua sắm trước đó và phát hiện ra các luật liên kết như: "Nếu mua bánh mì, thì khả năng cao họ sẽ mua bơ"

## Semi-Supervised Learning (Học bán giám sát)

- Các bài toán khi chúng ta có một lượng lớn dữ liệu X nhưng chỉ **một phần** trong chúng được gán nhãn.

- Thực tế cho thấy rất nhiều các bài toán Machine Learning thuộc vào nhóm này vì việc thu thập dữ liệu có nhãn tốn rất nhiều thời gian và có chi phí cao.

## Reinforcement Learning (Học Củng Cố)

- Một **tác nhân** (agent) học cách đưa ra các quyết định tốt nhất bằng cách tương tác với **môi trường**.

- Agent thực hiện các hành động và nhận **phản hồi** (feedback) dưới dạng phần thưởng hoặc hình phạt. 

=> Mục tiêu của tác nhân là **tối ưu hóa phần thưởng tích lũy** trong suốt quá trình học.

- Từ khóa:
    + `Tác nhân` (Agent): Là đối tượng thực hiện hành động trong môi trường.
    + `Môi trường` (Environment): Là thế giới mà agent tương tác và nhận phản hồi.
    + `Hành động` (Action): Là những gì mà agent có thể thực hiện để thay đổi trạng thái của môi trường.
    + `Phần thưởng` (Reward): Là phản hồi mà agent nhận được sau khi thực hiện hành động.
    + `Chính sách` (Policy): Là chiến lược mà agent học để chọn hành động tốt nhất dựa trên kinh nghiệm đã có.

- Đặc điểm: 
    + **Không có dữ liệu đầu vào hay đầu ra cố định**: Agent tự học từ kinh nghiệm thông qua việc tương tác với môi trường.
    + **Phần thưởng (Reward)**: Phản hồi sau mỗi hành động giúp tác nhân biết hành động nào là tốt và hành động nào là không tốt.
    + **Chiến lược dài hạn**: Agent học cách tối ưu hóa phần thưởng tổng thể trong quá trình học, thay vì chỉ tập trung vào phần thưởng ngay lập tức.

- Ví dụ: Giống như cách một chú chó học từ trải nghiệm để thực hiện hành động theo yêu cầu nhằm nhận được phần thưởng.

## Triển khai mô hình Machine Learning:

- `Centralized ML` (Tập trung): Triển khai tập trung là cách triển khai mô hình `Machine Learning` truyền thống, trong đó chúng ta đào tạo và cập nhật mô hình của mình trên server trung tâm hoặc nền tảng cloud, sau đó gửi dự đoán hoặc đề xuất đến người dùng cuối hoặc thiết bị.


- **Ưu điểm**: 

    + Tận dụng sức mạnh tính toán và dung lượng lưu trữ của đám mây để xử lý các mô hình và tập dữ liệu lớn và phức tạp.

    + Dễ dàng giám sát và quản lý hiệu suất, chất lượng và bảo mật của mô hình từ một điểm kiểm soát duy nhất (server).

    + Cho phép các quy trình đào tạo mô hình và xử lý dữ liệu nhất quán và chuẩn hóa trong toàn tổ chức.

- **Nhược điểm**:

    + Độ trễ cao và chi phí băng thông.

    + Dễ bị tấn công do có điểm yếu tập trung.

    + Khó khăn trong việc mở rộng khi số lượng người dùng tăng lên

- `Decentralized ML` (Phi tập trung): Là một cách mới nổi để triển khai các mô hình `Machine Learning` theo cách **phân tán**, trong đó chúng ta phân phối đào tạo mô hình và suy luận trên nhiều thiết bị biên hoặc node, chẳng hạn như điện thoại thông minh, thiết bị IoT, ... mà không cần đến máy chủ tập trung.


- **Ưu điểm**:
    
    + Giảm độ trễ và chi phí băng thông vì dữ liệu được xử lý ở thiết bị cục bộ.

    + Tăng cường quyền riêng tư và bảo mật dữ liệu.

    + Cải thiện khả năng mở rộng và độ tin cậy.

- **Nhược điểm**:

    + Sức mạnh tính toán và dung lượng lưu trữ hạn chế trên các thiết bị biên.

    + Xử lý chất lượng dữ liệu và hiệu suất mô hình không nhất quán hoặc nhiễu trên các thiết bị biên.

=> Kết luận: `Decentralized ML` đang ngày càng phát triển, đặc biệt là trong các hệ thống yêu cầu tính bảo mật và phân phối cao như các ứng dụng IoT, mạng viễn thông và các dịch vụ tài chính.

## Federated Learning

- **Từ khóa**: "Distributed"

- **Định nghĩa**: `Federated Learning` (còn được gọi là *học cộng tác*) là một kỹ thuật `Decentralized Machine Learning` đào tạo một thuật toán trên nhiều thiết bị biên phi tập trung và **chỉ chia sẻ các tham số mô hình** với server, không chia sẻ dữ liệu thô.

=> Giúp bảo vệ quyền riêng tư và bảo mật dữ liệu.


- **Các đặc điểm chính**:

    + `Bảo vệ quyền riêng tư`: Vì dữ liệu thô không bao giờ rời khỏi thiết bị, nên nó giúp bảo vệ quyền riêng tư của người dùng và tuân thủ các quy định pháp lý về dữ liệu.
    
    + `Phân tán`: Quá trình huấn luyện được thực hiện trên nhiều thiết bị khác nhau.
    
    + `Tính tổng hợp`: Máy chủ trung tâm chỉ tổng hợp các thông số mô hình đã được huấn luyện cục bộ, chứ không truy cập vào dữ liệu gốc.
    
   + `Đồng bộ hóa` hoặc `không đồng bộ hóa`: Các thiết bị có thể gửi cập nhật mô hình đồng thời (đồng bộ) hoặc không đồng thời (không đồng bộ), tùy thuộc vào cách thiết kế hệ thống.

- **Nhược điểm**: 

    + `Dữ liệu không phải IID`: Dữ liệu được tạo ra từ nhiều thiết bị không độc lập và không phân phối giống nhau.

    + `Khả năng tính toán của thiết bị`: Các thiết bị khác nhau có phần cứng và phần mềm khác nhau, ảnh hưởng đến khả năng xử lý.

    + `Gắn nhãn dữ liệu`: Cần có nhãn rõ ràng và nhất quán cho dữ liệu, nhưng với nguồn dữ liệu từ nhiều thiết bị, việc dán nhãn tự động gặp khó khăn.

    + `Rò rỉ dữ liệu`: Có khả năng xác định và lấy dữ liệu từ người dùng thông qua kỹ thuật đảo ngược.

## Swarm Learning

- **Từ khóa**: "Decentralized + Collaborative"

- **Định nghĩa**: `Swarm Learning` là một khái niệm tiên tiến hơn của `Decentralized ML`, trong đó các thiết bị hoặc node không chỉ huấn luyện mô hình cục bộ mà còn hợp tác và chia sẻ kết quả với nhau trực tiếp, không cần đến một server nào cả. Thay vào đó, chúng hợp tác và ra quyết định dựa trên mạng blockchain-based peer-to-peer, điện toán biên (edge computing), đảm bảo tính minh bạch và bảo mật cao hơn.

- Về bản chất, `Federated Learning` và `Swarm Learning` đều thuộc `Decentralized ML`, nhưng chúng khác nhau ở cách thức các node trong hệ thống giao tiếp và hợp tác với nhau.

- **Ưu điểm**:

    + Không cần server để quản lý và huấn luyện mô hình, giúp giảm sự phụ thuộc vào hạ tầng trung tâm và tránh tắc nghẽn hệ thống.

    + Bảo vệ quyền riêng tư và tuân thủ các quy định bảo mật dữ liệu.

    + Khả năng mở rộng tốt.

- **Nhược điểm**: 

    + Việc đồng bộ hóa và hợp nhất các mô hình từ nhiều node có thể phức tạp.

    + Các thiết bị cục bộ cần có đủ tài nguyên tính toán để huấn luyện mô hình.

    + Khi các nút có dữ liệu không đồng nhất hoặc chất lượng dữ liệu thấp, điều này có thể ảnh hưởng đến **chất lượng mô hình tổng thể**.


## Domain cho nghiên cứu: Smart Health

- Lý do lựa chọn: 

    + Giảm tải công việc cho nhân viên y tế và nâng cao hiệu quả quản lý bệnh viện, từ đó cung cấp dịch vụ y tế nhanh hơn và hiệu quả hơn.

    + Giảm chi phí vận hành của các cơ sở y tế.

    + Hỗ trợ bác sĩ trong việc phân tích dữ liệu sức khỏe của từng bệnh nhân, từ đó đưa ra phương án điều trị tối ưu và cá nhân hóa cho từng người.

    + Bảo vệ thông tin cá nhân của các bệnh nhân.
    
    + Tiếp cận dịch vụ y tế ngay tại nhà mà không cần đến bệnh viện, cực kì hữu ích cho người dân ở vùng xa hoặc những người có khó khăn trong việc di chuyển.

## Các trang học tập tham khảo

* https://www.youtube.com/watch?v=WgtTRwYwrJI&list=PLZEIt444jqpBPoqtW2ARJp9ICnF3c7vJC&ab_channel=SonNguyen

* https://machinelearningcoban.com/2016/12/26/introduce/

* https://mlsysbook.ai/contents/introduction/introduction.html?fbclid=IwY2xjawFhqrtleHRuA2FlbQIxMAABHUGV7QmxoMOigRDySs3LXhhkJWsgv4tB4WVM4Vj49gVUAjL5zvAH1jz2Ow_aem_lhdw_LG4DRaBC5PQtz8BmA

* https://www.coursera.org/programs/nic-x-uit-3-revb1/professional-certificates/google-it-automation?collectionId=JsnkQ
