# <center>TỔNG QUAN VỀ DEEP LEARNING (HỌC SÂU) </center>
Là một lĩnh vực của Trí tuệ nhân tạo (AI), bắt chước cách hoạt động của não bộ con người để xử lý dữ liệu, tạo ra các mẫu để sử dụng cho việc đưa ra quyết định.

## Mục lục
1. [Deep Learning là gì?](#deep-learning-là-gì)
2. [Ưu điểm và nhược điểm](#ưu-điểm-và-nhược-điểm)
3. [Cách hoạt động của Deep Learning](#cách-hoạt-động-của-deep-learning)
4. [Kĩ thuật Deep Learning](#kĩ-thuật-deep-learning)
    * [ANN](#artificial-neural-network-ann---mạng-nơ-ron-cổ-điển)
    * [CNN](#convolutional-neural-network-cnn)
    * [RNN](#recurrent-neural-network-rnn)
    * [GAN](#generative-adversarial-networks-gan)
    * [Boltzmann machine](#boltzmann-machine)
    * [Deep Reinforcement Learning](#deep-reinforcement-learning)
    * [Autoencoder](#autoencoder)
    * [Backpropagation](#backpropagation)
    * [Decent gradient](#decent-gradient)
5. [Deep Learning giải quyết những vấn đề gì?](#deep-learning-giải-quyết-những-vấn-đề-gì)
6. [Có nên sử dụng Deep Learning thay cho Machine Learning?](#có-nên-sử-dụng-deep-learning-thay-cho-machine-learning)
7. [Môi trường huấn luyện](#môi-trường-huấn-luyện)

## Deep Learning là gì?

- Deep Learning (DL) - học sâu, được xem là một lĩnh vực con của trí tuệ nhân tạo, ở đây, các máy tính **sẽ học và cải thiện chính nó thông qua các thuật toán**. Deep learning chủ yếu hoạt động với các **mạng nơ-ron nhân tạo** để bắt chước khả năng tư duy và suy nghĩ của con người.


- Mạng nơ-ron nhân tạo chính là động lực để phát triển DL. Mạng nơ-ron sâu (DNN) bao gồm nhiều lớp nơ-ron khác nhau, có khả năng thực hiện các phép tính phức tạp.

## Ưu điểm và Nhược điểm

- Ưu điểm:
    - Kiến trúc mạng nơ-ron linh hoạt, có thể dễ dàng thay đổi dựa trên các yêu cầu khác nhau.
    - Có khả năng giải quyết nhiều bài toán với tính chính xác rất cao.
    - Tính tự động hoá cao, có khả năng tự điều chỉnh và tự tối ưu.
    - Có khả năng thực hiện tính toán song song, hiệu năng tốt, xử lý được lượng dữ liệu lớn.

- Nhược điểm:
    - Cần có khối lượng dữ liệu rất lớn để tận dụng sức mạnh của DL.
    - Chi phí tính toán cao.
    - Chưa có nền tảng lý thuyết mạnh mẽ để lựa chọn các công cụ tối ưu cho Deep Learning.

## Cách hoạt động của Deep Learning

- Một mạng nơ-ron bao gồm nhiều lớp (layer) khác nhau, số layer càng nhiều thì mạng sẽ càng "sâu". Nhưng về thực tế chỉ có 3 loại layer khác nhau:
    - *Input layer*: Nhận dữ liệu
    - *Hidden layer*: Thực hiện các phép tính trung gian và trích xuất đặc trưng từ dữ liẹu
    - *Output layer*: Đưa ra kết quả cuối cùng.
- Trong các kiến trúc hiện đại, như mạng ResNet hay Transformer, còn có thêm khái niệm như **skip connections** hoặc **attention layers**, nhưng chúng vẫn tuân theo nguyên tắc cơ bản của ba loại lớp trên.

- Trong mỗi layer là các nút mạng (node) và được liên kết với những lớp liền kề khác. Mỗi kết nối giữa các node sẽ có một **trọng số** tương ứng (xác định mức độ quan trọng của kết nối giữa 2 nơ-ron), trọng số càng cao thì ảnh hưởng của kết nối này đến mạng nơ-ron càng lớn.

- Bên cạnh đó, chúng ta còn có **độ chệch (bias)**, giá trị giúp điều chỉnh đầu ra của nơ-ron, đảm bảo học được các mối quan hệ *phi tuyến tính* trong dữ liệu.

- Các hidden layer thực hiện các phép tính cho các input đầu vào. Thử thách lớn nhất đó chính là quyết định số lượng mạng nơ-ron cho mỗi layer cũng như các hidden layer, dựa trên các yếu tố sau:
    - Đặc trưng của dữ liệu.
    - Độ phức tạp của bài toán.
    - Nguy cơ **overfitting** nếu dùng quá nhiều nơ-ron/layers.

- Mỗi nơ-ron sẽ có một **hàm kích hoạt** (Activation function), về cơ bản thì có nhiệm vụ “chuẩn hoá” đầu ra từ nơ-ron này. 

## Kĩ thuật Deep Learning

### Artificial Neural Network (ANN - Mạng nơ-ron cổ điển)

- Về cơ bản, đây là một mô hình tính toán được xây dựng dựa trên cấu trúc và chức năng của mạng lưới nơ ron trong Sinh học.

- Nói cách khác, đây là loại mạng mô phỏng bộ não con người và được sử dụng trong Machine Learing và Deep Learning để đưa ra **dự đoán và thu thập thông tin chi tiết từ dữ liệu**.

- ANN là dữ liệu thống kê **phi tuyến tính.**

- Kiến trúc ANN tương đối đơn giản, phù hợp nhất với các bộ dữ liệu có **dạng bảng** hoặc **những bài toán phân loại, hồi quy** có đầu vào là **giá trị thực.**



- Có 2 loại ANN:    
    
    - *FeedForward ANN:*

        * Chỉ gồm luồng thông tin 1 chiều, khong xuất hiện vòng phản hồi (gửi ngược thông tin về lại). Mô hình này được sử dụng để nhận dạng một mẫu cụ thể, vì chúng chứa các đầu vào và ra cố định


    - *FeedBack ANN:*

        * Cho phép các vòng lặp phản hồi. Sử dụng mô hình này trong các bộ nhớ có thể giải quyết nội dung.


### Convolutional Neural Network (CNN)

- Đây là một kiến trúc Neural Network nhân tạo nâng cao, dùng để giải quyết các bài toán phức tạp, đặc biệt là **phân biệt hình ảnh**

- Tích chập là một khái niệm quan trọng trong việc xử lý thông tin đầu vào thông qua một phép tính gọi là phép tích chập (khác với tương quan chéo) với bộ lọc, nhằm trả về đầu ra là một tín hiệu mới.

- Sự khác nhau giữa Tích chập (Convolution và Cross - correlation):

| Tính chất | Tích chập (Convolution) | Tương quan chéo (Cross-correlation) |
|---|---|---|
| Định nghĩa | Phép toán giữa hai hàm số, trong đó một hàm số (kernel) **được lật ngược** trước khi thực hiện tích phân hoặc tổng. | Phép toán giữa hai hàm số, trong đó một hàm số (kernel) **không được lật ngược.** |
| Mục đích |  * Trích xuất **đặc trưng trong xử lý ảnh** (CNN) <br> * Mô hình hóa các hệ thống tuyến tính thời **bất biến** | * **Tìm kiếm** một mẫu cụ thể trong một tín hiệu lớn hơn |
| Ứng dụng |  * Mạng nơ ron tích chập <br> * Xử lý tín hiệu (lọc, phân tích phổ) <br> * **Xử lý ảnh** (phát hiện cạnh, làm mờ) |  * **Xử lý tín hiệu** (tìm kiếm mẫu) <br> * Thị giác máy tính (so sánh hình ảnh) |
| Kernel | **Được lật ngược** trước khi thực hiện phép toán | **Không được lật ngược** |
| Tính chất giao hoán | Trong một số trường hợp, có tính giao hoán | Không có tính giao hoán |

- Bên cạnh input và output layer, mô hình CNN còn có thêm một **Sampling Layer** để giới hạn số lượng nơ-ron tham gia vào các layer tương ứng.

- Việc xây dựng mô hình này trải qua 3 giai đoạn chính:



   - *Convolution (Quá trình tích chập)*: Đây là phép toán dùng trong xử lý ảnh với thuật toán **cửa sổ trượt** (sliding window hoặc kernel). Hình ảnh bên trái mô tả một ma trận đầu vào (Image, dựa trên phân giải hình ảnh, máy tính sẽ thấy HH x W x D (H: Chiều cao, W: Chiều rộng, D: Độ dày)) và hình bên phải là kết quả ma trận đặc trưng (Convolved Feature) sau khi áp dụng phép tích chập.
        - Ý nghĩa: **Trích xuất đặc trưng** từ ảnh đầu vào (Convolved feature)
        - Image input + filter (feature detect) -> Convolved feature
        - Trong xử lý truyền thông, kernel sẽ do người dùng định nghĩa. Trong trí tuệ nhân tạo, kernel sẽ được quyết định thông qua nhiều quá trình huấn luyện.



   - *Max pooling (Quá trình tổng hợp, thủ tục tìm ra giá trị lớn nhất)*: Ngay sau lớp Convolution, Pooling layer có nhiệm vụ giảm kích thước khối ma trận đầu vào thông qua việc tìm ra một giá trị đại diện cho mỗi một vùng không gian mà filter đi qua sẽ không làm thay đổi các đường nét chính của bức ảnh nhưng lại giảm được kích thước của ảnh. (Pooling size: thường là 2x2 hoặc 4xx4 cho ảnh đầu vào lớn)
     - Trong một mạng CNN có nhiều Feature Map nên mỗi Feature Map chúng ta sẽ cho mỗi Max Pooling khác nhau. Chúng ta có thể thấy rằng Max Pooling là cách hỏi xem trong các đặc trưng này thì đặc trưng nào là đặc trưng nhất. Ngoài Max Pooling còn có L2 Pooling.



   - *Full connected (Quá trình kết nối hoàn toàn)*: Sau khi giảm kích thước đến một mức độ nhất định. ma trận cần được làm phẳng (flatten) thành một vector và sử dụng fully connected giữa các tầng. Fully connected layer sẽ có **số lượng đơn vị bằng với số lớp**.

- Cách chọn tham số cho CNN:
    - *Số các convolution layer*: càng nhiều các convolution layer thì performance càng được cải thiện. Sau khoảng 3 hoặc 4 layer, các tác động được giảm một cách đáng kể
    - *Filter size*: thường filter theo size 5x5 hoặc 3x3
    - *Pooling size*: thường là 2x2 hoặc 4x4 cho ảnh đầu vào lớn
    - Cách cuối cùng là thực hiện nhiều lần việc train test để chọn ra được param tốt nhất.

### Recurrent Neural Network (RNN)

- Recurent Neural Network (RNN), có tên gọi trong tiếng Việt là Mạng nơ-ron hồi quy, là một thuật toán nổi tiếng trong lĩnh vực **xử lý ngôn ngữ tự nhiên**. 

- Trong các mô hình mạng nơ-ron truyền thống, đầu vào và đầu ra độc lập với nhau, tuy nhiên **RNN thực hiện cùng một tác vụ cho tất cả phần tử của một chuỗi** với đầu ra phụ thuộc vào cả các phép tính trước đó. Vì vậy mạng **RNN có khả năng nhớ các thông tin được tính toán trước đó.**

- Cách hoạt động của RNN: Quá trình xử lý dữ liệu, phân tích và dự đoán diễn ra trong **lớp ẩn**. 


    - *Lớp ẩn:* RNN hoạt động bằng cách **truyền dữ liệu tuần tự nhận được đến các lớp ẩn**. Tuy nhiên, RNN cũng có quy trình làm việc **tự lặp lại** hay **hồi quy**: lớp ẩn có thể **ghi nhớ** và sử dụng các đầu vào trước đó cho các dự đoán trong tương lai trong một thành phần bộ nhớ ngắn hạn. Quy trình này sử dụng đầu vào hiện tại và bộ nhớ đã lưu trữ để dự đoán chuỗi tiếp theo.

- RNN có hai thiết kế chính:
    - *LSTM (Long Short-Term Memory)*: Được dùng để dự đoán dữ liệu **dạng chuỗi thời gian**, có khả năng bỏ đi hoặc thêm các thông tin cần thiết, được điều chỉnh bởi các nhóm được gọi là cổng (gate): Input, Output và Forget. Cách hoạt động:
        - Cổng quên (Forget): Quyết định thông tin nào từ bộ nhớ cũ cần bỏ qua.
        - Cổng vào (Input): Quyết định thông tin mới nào cần được thêm vào bộ nhớ.
        - Cập nhật bộ nhớ (Cell State): Kết hợp thông tin cũ và thông tin mới để tạo ra bộ nhớ mới.
        - Cổng ra (Output): Quyết định thông tin nào từ bộ nhớ sẽ được sử dụng để tính toán trạng thái ẩn hiện tại.


    - *Gated recurrent units (GRUs)*: Cũng là một thiết kế phổ biến trong lĩnh vực dự đoán dữ liệu của chuỗi thời gian, có hai cổng là **Update và Reset.** Cách hoạt động:
        - Cổng đặt lại (Reset Gate): Quyết định mức độ sử dụng thông tin từ trạng thái ẩn trước đó.
        - Cổng cập nhật (Update Gate): Quyết định mức độ kết hợp thông tin mới và thông tin cũ để tạo ra trạng thái ẩn mới.
        - Cập nhật trạng thái ẩn: Kết hợp thông tin từ trạng thái ẩn trước đó và trạng thái ứng viên để tạo ra trạng thái ẩn mới.

- Bảng so sánh giữa LSTM và GRU:


| Đặc điểm | GRU (Gated Recurrent Unit) | LSTM (Long Short-Term Memory) |
|---|---|---|
| **Số cổng** | 2 cổng: Cổng cập nhật (update gate) và cổng đặt lại (reset gate) | 3 cổng: Cổng vào (input gate), cổng quên (forget gate) và cổng ra (output gate) |
| **Bộ nhớ bên trong** | Không có bộ nhớ bên trong riêng biệt | Có bộ nhớ bên trong (cell state) c<sub>t</sub> |
| **Cơ chế hoạt động** | Sử dụng cổng cập nhật để điều khiển việc kết hợp trạng thái ẩn trước đó và trạng thái ẩn hiện tại. Cổng đặt lại quyết định mức độ bỏ qua trạng thái ẩn trước đó. | Sử dụng cổng quên để quyết định thông tin nào cần giữ lại từ bộ nhớ bên trong. Cổng vào quyết định thông tin mới nào được lưu vào bộ nhớ bên trong. Cổng ra quyết định thông tin nào từ bộ nhớ bên trong được đưa ra làm trạng thái ẩn hiện tại. |
| **Số lượng tham số** | Ít hơn LSTM | Nhiều hơn GRU |
| **Khả năng tính toán** | Tính toán nhanh hơn LSTM | Tính toán chậm hơn GRU |
| **Hiệu suất** | Thường có hiệu suất tương đương với LSTM trong nhiều bài toán. Đôi khi hoạt động tốt hơn LSTM trong các bài toán với dữ liệu ít hoặc cần tốc độ xử lý nhanh. | Thường đạt hiệu suất tốt hơn GRU trong các bài toán phức tạp với lượng dữ liệu lớn. |
| **Độ phức tạp** | Đơn giản hơn LSTM | Phức tạp hơn GRU |
| **Ưu điểm** | Đơn giản, tính toán nhanh, ít tham số, phù hợp với dữ liệu nhỏ và yêu cầu tốc độ xử lý. | Mạnh mẽ trong việc xử lý các chuỗi dài, khả năng ghi nhớ thông tin tốt hơn, phù hợp với các bài toán phức tạp và dữ liệu lớn. |
| **Nhược điểm** | Khả năng ghi nhớ thông tin trong chuỗi dài có thể kém hơn LSTM trong một số trường hợp. | Phức tạp, tính toán chậm hơn, nhiều tham số hơn. |

- Ngoài ra còn 1 thiết kế nữa là *Bidirectional Recurrent Neural Network (BRNN)*: Xử lý các chuỗi dữ liệu với các lớp tiến và lùi của các nút ẩn.
    - Lớp tiến (forward layer) hoạt động tương tự như RNN, lưu trữ đầu vào trước đó ở trạng thái ẩn và sử dụng đầu vào đó để dự đoán đầu ra tiếp theo.
    - Lớp lùi (backward layer) hoạt động theo hướng ngược lại bằng cách lấy cả đầu vào hiện tại và trạng thái ẩn trong tương lai để cập nhật trạng thái ẩn hiện tại.

- Các dạng bài toán RNN:
    - One to One: Chỉ một input kết nối với một output duy nhất, chẳng hạn như phân loại hình ảnh.
    - One to Many: Một input nhưng cho ra nhiều input, phổ biến là bài toán đặt caption cho ảnh.
    - Many to One: Nhiều input nhưng chỉ cho ra một Output, ví dụ phân loại cảm xúc.
    - Many to Many: Nhiêu input và nhiều output, chẳng hạn như phân loại video.


### Generative Adversarial Networks (GAN)

- Generative Adversarial Network (GAN), hay có tên gọi trong tiếng Việt là **mạng sinh đối kháng** là một dạng mạng nơ-ron thuộc nhóm Generative Model. 

- Đây là lớp mô hình có mục tiêu tạo ra dữ liệu giả giống dữ liệu thật, tên của mạng được dựa trên 2 mục tiêu đối nghịch nhau: Generator và Discriminator. Trong đó, Generator học cách sinh dữ liệu giả để lừa mô hình Discriminator, còn Discriminator lại học cách phân biệt giữa dữ liệu giả và dữ liệu thật.



### Boltzmann machine



### Deep Reinforcement Learning 

### Autoencoder

### Backpropagation

### Decent gradient

## Deep Learning giải quyết những vấn đề gì?

- Trợ lý ảo
- Hệ thống lái xe tự động
- Mạng xã hội
- Phân tích cảm xúc
- ... 

## Có nên sử dụng Deep Learning thay cho Machine Learning?

- Phụ thuộc phần lớn vào mục tiêu và chiến lược kinh doanh cụ thể, số lượng dữ liệu, tài nguyên,… 
- Ngoài ra, còn dựa vào điều kiện dữ liệu có lớn hay không, model có nặng hay không.

## Môi trường huấn luyện

- Máy tính cá nhân
- Google Collab
- ai.uitiot.vn
- A100

## Trang web tham khảo:

https://vietnix.vn/deep-learning-la-gi/#cac-ky-thuat-deep-learning

https://viettelidc.com.vn/tin-tuc/cam-nang-ai-artificial-neural-network-la-gi-cau-truc-cach-hoat-dong-va-ung-dung-cua-mo-hinh-nay

https://topdev.vn/blog/thuat-toan-cnn-convolutional-neural-network/#cnn-convolutional-neural-network-la-gi

https://viblo.asia/p/deep-learning-tim-hieu-ve-mang-tich-chap-cnn-maGK73bOKj2