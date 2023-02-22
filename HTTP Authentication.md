HTTP authentication – còn được gọi là cơ chế xác thực HTTP giúp người dùng xác minh danh tính. Nó là một cơ chế bảo mật kiểm tra xem người dùng có đủ điều kiện truy cập web hay không. Khi máy khách và máy chủ giao tiếp với nhau, dựa vào thành phần HTTP, máy chủ sẽ yêu cầu thông tin đăng nhập để xác thực. Vậy nên có thể nói, việc xác thực web sẽ thông qua tiêu chuẩn HTTP bảo đảm an toàn cho người dùng.  

Một phiên bản bảo mật hơn HTTP chính là HTTPS (S viết tắt từ SSL) có khả năng thiết lập mã hóa khi giao tiếp. Có nhiều cách để cơ chế xác thực HTTP để khiến cho các thông tin đăng nhập của tin tặc không đủ quyền bẻ khóa. Từ đó, việc truy cập của người dùng sẽ trở nên an toàn hơn trong môi trường mạng.  

HTTP có một framework chung để kiểm soát kiềm truy cập của người dùng vào tài nguyên web. Tất nhiên framework sẽ dựa vào tiêu đề (header) xác thực để sử dụng. Các header hỗ trợ người dùng cách cung cấp thông tin đăng nhập của họ và hồ sơ. Có hai loại header chủ yếu là: WWW-Authenticate header và Proxy Authentication header.  

Giao thức HTTP bao gồm các cơ chế riêng để xác thực người dùng bằng các sơ đồ xác thực khác nhau, bao gồm:  
    
    Basic là một cơ chế xác thực đơn giản gửi thông tin đăng nhập của người dùng dưới dạng chuỗi được mã hóa Base64 trong tiêu đề yêu cầu (request header) với mỗi thông báo.  
    
    NTLM là một cơ chế thử thách-phản hồi và sử dụng một phiên bản của giao thức Windows NTLM.  
    
    Digest là một cơ chế thử thách-phản hồi và sử dụng tổng kiểm tra MD5 của nonce với thông tin đăng nhập của người dùng.  
    
    HTTP Authentication Schemes: còn được gọi là lược đồ xác thực HTTP. Máy chủ đưa ra những lược đồ xác thực khác nhau cho người dùng lựa chọn. Chúng đều là những phương pháp dùng trên web cho độ an toàn cao.  
    
    Bearer authentication (xác thực đa yếu tố): xác thực dựa trên mã thông báo. Nó có thêm một lớp bổ sung và bảo mật cấp với mã thông báo để xác thực thông tin nhận được từ người dùng.  
    
    Negotiate authentication (đàm phán xác thực): là phiên bản nâng cấp của NTLM. Nó sử dụng giao thức Kerberos làm nhà cung cấp xác thực một cách nhanh chóng và an toàn.  
    
    
Tương đối hiếm khi gặp các giao thức xác thực này đang được sử dụng bởi các ứng dụng web được triển khai trên Internet. Chúng được sử dụng phổ biến hơn trong các tổ chức để truy cập các dịch vụ dựa trên mạng nội bộ.  

Web Functionality:  
  Ngoài giao thức liên lạc cốt lõi được sử dụng để gửi tin nhắn giữa máy khách và máy chủ, các ứng dụng web sử dụng nhiều công nghệ để cung cấp chức năng của chúng. Bất kỳ ứng dụng chức năng hợp lý nào cũng có thể sử dụng hàng chục công nghệ riêng biệt trong các thành phần máy chủ và máy khách của nó. Trước khi bạn có thể thực hiện một cuộc tấn công nghiêm trọng vào một ứng dụng web, bạn cần có hiểu biết cơ bản về cách thức triển khai chức năng của ứng dụng đó, cách các công nghệ được sử dụng được thiết kế để hoạt động và điểm yếu của chúng có thể nằm ở đâu.  
