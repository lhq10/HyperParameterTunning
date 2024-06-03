### Điều chỉnh siêu tham số cho mô hình phân tích ngữ điệu của câu

#### Chuẩn bị dữ liệu:

Bộ dữ liệu được lấy từ IMDB Dataset với 50.000 câu. Trong đó có 25.000 positive và 25.000 negative.
Dữ liệu được xử lí để đưa vào huấn luyện mô hình với các bước: xóa content HTML, xóa các kí tự đặc biệt hoặc các thứ không liên quan tới giọng điệu của câu, chuyển qua từ thường, tách từ, xử lí stopword, stemming, ....

#### Triển khai mô hình:

Dữ liệu đã được chuẩn bị sẽ được đưa vào huấn luyện.
Sử dụng linearSVC để phân loại dữ liệu.

#### Điều chỉnh siêu tham số:

Điều chỉnh siêu tham số C của mô hình LinearSVC để thấy được sự tăng hay giảm độ chính xác của mô hình.
Không nhất thiết tham số C phải càng cao thì mô hình càng chính xác mà có thể khiến mô hình dẫn đến bị overfitting.
Vì vậy sử dụng các thư viện GridSearchCV và RandomizedSearchCV để kiểm tra mô hình hiệu quả với tham số C nào hơn.
