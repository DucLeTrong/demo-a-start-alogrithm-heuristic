# Tìm đường đi trong mê cung áp dụng A* search

## Giới thiệu

Project này là bài tập lớn môn Trí tuệ nhân tạo (học kì 20181)

Giảng viên hướng dẫn: TS.Nguyễn Nhật Quang

Sinh viên thực hiện: Lê Trọng Đức - Đỗ Ngọc Sơn

[Truy cập đường link để trực tiếp phần demo](https://ducletrong.github.io/demo-a-start-alogrithm-heuristic/)

## Lời nói đầu

Tìm đường đi trong mê cung sử dụng A* là một bài toán kinh điển và quen thuộc đã xuất hiện trong nhiều giáo trình, sách vở và các bài nghiên cứu. 

Trong tài liệu này, chúng tôi sẽ nêu ra một số khái niệm cơ bản về thuật toán A* và hàm Heuristic, và nêu thí nghiệm đánh giá hiệu năng của các hàm heuristic trong một số trường qua công cụ trực quan mô phỏng lại thuật toán được viết bằng ngôn ngữ javascrip. Tài liệu giúp người dùng biết các sử dụng công cụ mô phỏng và hiểu được các khái niệm và ý tưởng của thuật toán A*, và đánh giá sự hiệu quả của các hàm Heuristic trong các trường hợp.

Chúng tôi xin được gửi lời cảm ơn tới giảng viên trực tiếp hướng dẫn – TS.Nguyễn Nhật Quang, giảng viên môn Trí tuệ nhân tạo (IT4040), đã tận tình dạy bảo, hướng dẫn chúng tôi hoàn thành đề tài của mình. 

Hướng dẫn này sẽ chỉ ra các thực hiện deploy project để so sánh hiệu quả của các hàm heuristics trong A* search

## Nội dung

### Các chức năng chính

Visualize bài toán tìm đường đi trong mê cung, áp dụng thuật toán A* search
Trong ứng dụng này, chúng tôi đặt một số tham số (có thể customize bởi người dùng) trước khi thực hiện thuật toán như sau:

1. Được đi chéo hay không

2. Chọn hàm heuristics

3. Chúng tôi cũng cung cấp chức năng cho phép người dùng sử dụng mê cung được sinh bởi thuật toán DFS hoặc có thể customize hình dạng mê cung theo ý họ. Trên bản đồ mê cung, ô đen thể hiện rằng nó không thể đi tới được, ô trắng thể hiện nó có thể đi tới được

4. Người dùng có thể tùy ý chọn ô source và ô destination trên bản đồ mê cung miễn là 2 điểm đó nằm trong mê cung, không trùng nhau và không trùng với ô đen.

### Cách deploy
Để deploy được ứng dụng, người dùng phải có kết nối internet ổn định

Các bước Deploy ứng dụng:

  B1: Vào thư mục A-star-Algorithm, Mở file index.html bằng trình duyệt máy tính (Khuyến cáo nên mở bằng google chrome để tránh bị lỗi không mong muốn về giao diện)
  
      Giao diện hiện lên gồm có 2 phần chính: Bên trái là phần Option, bên phải là mê cung được xây dựng sẵn, nơi thực hiện visualize thuật toán
      
  B2: Lựa chọn các Option:
  
        Nếu muốn cho thuật toán tìm đường đi tới các ô chéo nhau thì lựa chọn "Cho phép đi chéo", nếu không thì lựa chọn "Không cho phép đi chéo"
        
        Người dùng có thể chọn các hàm Heuristics như họ mong muốn bằng việc chọn option trong phần Heuristic
        
        Người dùng có thể chọ chế độ "Select source-destination" để bắt đầu chọn node source và destination và bắt đầu thuật toán. Node source được tô màu đỏ, node destination được tô màu tím, sau khi source được chọn thì lần click tiếp theo được hiểu là chọn destination, sau khi cả source và destination được chọn thì thuật toán sẽ tự động tiến hành. Lưu ý, Sau khi thực hiện thuật toán xong, nếu tiếp tục chọn source thì kết quả thực hiện trước đó sẽ được reset, ô vừa chọn được hiểu là source của lần tìm kiếm tiếp theo
        
        Người dùng có thể chọn chế độ "Create Maze" để thực hiện customize mê cung. Chọn "Clear maze" để xóa mê cung được sinh sẵn và thực hiện tạo mê cung từ đầu
        
        Người dùng có thể chọn "New session" để reset lại mê cung. Sau khi reset lại, mê cung mới sẽ được tự động sinh ra

### Kết quả hiển thị

Chúng tôi hiển thị 3 đại lựa đại diện cho độ hiệu quả của mối hàm heuristic:

1. Số ô trong đường đi được tìm ra

2. Chi phí cho đường đi

3. Số ô đã được duyệt

## Kết luận

Chúng tôi đã cố gắng hết sức để hoàn thành đè tài một cách tốt nhất, song trong quá trình thực hiện không tránh khỏi các sai sót. Rất mong nhận được sự đóng góp để chúng tôi có thể hoàn thiện bài tập lớn này.
