Khi bạn đang tấn công các ứng dụng web, bạn hầu như chỉ xử lý các phương thức được sử dụng phổ biến nhất: GET và POST. Bạn cần lưu ý một số phương pháp khác (POST, PUT, PATCH, DELETE, CONNECT, OPTIONS, TRACE) và sự khác biệt quan trọng giữa các phương pháp này vì chúng có thể ảnh hưởng đến tính bảo mật của ứng dụng nếu bị bỏ qua.  

    Phương thức GET được thiết kế để truy xuất tài nguyên. Nó có thể được sử dụng để gửi tham số đến tài nguyên được yêu cầu trong chuỗi truy vấn URL. Điều này cho phép người dùng đánh dấu một URL cho tài nguyên động mà họ có thể sử dụng lại. Hoặc những người dùng khác có thể truy xuất tài nguyên tương đương trong lần tiếp theo (như trong truy vấn tìm kiếm được đánh dấu trang). Các URL được hiển thị trên màn hình và được ghi lại ở nhiều nơi khác nhau, chẳng hạn như lịch sử trình duyệt và nhật ký truy cập của máy chủ web. Chúng cũng được truyền trong tiêu đề Người giới thiệu đến các trang web khác khi các liên kết bên ngoài được theo dõi. Vì những lý do này, không nên sử dụng chuỗi truy vấn để truyền bất kỳ thông tin nhạy cảm nào.  
    
    Phương thức POST được thiết kế để thực hiện các hành động. Với phương pháp này, các tham số yêu cầu có thể được gửi cả trong chuỗi truy vấn URL và trong phần nội dung của thư. Mặc dù URL vẫn có thể được đánh dấu trang nhưng bất kỳ tham số nào được gửi trong nội dung thư sẽ bị loại trừ khỏi dấu trang. Các tham số này cũng sẽ bị loại trừ khỏi các vị trí khác nhau trong đó nhật ký URL được duy trì và khỏi tiêu đề Người giới thiệu. Vì phương thức POST được thiết kế để thực hiện các hành động, nếu người dùng nhấp vào nút Quay lại của trình duyệt để quay lại trang được truy cập bằng phương thức này, thì trình duyệt sẽ không tự động đưa ra lại yêu cầu. Thay vào đó, nó cảnh báo người dùng về những gì nó sắp làm, như thể hiện trong hình. Điều này ngăn người dùng vô tình thực hiện một hành động nhiều lần. Vì lý do này, các yêu cầu POST phải luôn được sử dụng khi một hành động đang được thực hiện.  
    
<img width="410" alt="image" src="https://user-images.githubusercontent.com/125866921/220383818-8d979448-6de7-4e28-8f99-86bd0c9c4357.png">

    Phương thức HEAD hoạt động theo cách tương tự như yêu cầu GET, ngoại trừ việc máy chủ không được trả về nội dung thư trong phản hồi của nó. Máy chủ sẽ trả về các tiêu đề giống như nó sẽ trả về yêu cầu GET tương ứng. Do đó, phương pháp này có thể được sử dụng để kiểm tra xem tài nguyên có tồn tại hay không trước khi thực hiện yêu cầu GET cho nó.  
    
    Phương thức TRACE được thiết kế cho mục đích chẩn đoán. Máy chủ sẽ trả lại trong nội dung phản hồi nội dung chính xác của thông báo yêu cầu mà nó nhận được. Điều này có thể được sử dụng để phát hiện ảnh hưởng của bất kỳ máy chủ proxy nào giữa máy khách và máy chủ có thể thao túng yêu cầu.  
    
    Phương thức OPTIONS yêu cầu máy chủ báo cáo các phương thức HTTP khả dụng cho một tài nguyên cụ thể. Máy chủ thường trả về phản hồi có chứa tiêu đề Cho phép liệt kê các phương thức khả dụng.  
    
    Phương thức PUT cố gắng tải tài nguyên được chỉ định lên máy chủ, sử dụng nội dung có trong phần nội dung của yêu cầu. Nếu phương thức này được bật, bạn có thể tận dụng nó để tấn công ứng dụng, chẳng hạn như bằng cách tải lên một tập lệnh tùy ý và thực thi tập lệnh đó trên máy chủ.  
    
    Phương thức PATCH cũng giống như PUT, PATCH được dùng để thay đổi data thế nhưng nó chỉ thay đổi những field được yêu cầu thay đổi thay vì toàn bộ resource.  
    
    Phương thức DELETE dùng để xóa tài nguyên trên server.  
    
    Phương thức CONNECT dùng để thiết lập một kết nối tới server theo URL.  
