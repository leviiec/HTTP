Cookie là một phần quan trọng của giao thức HTTP mà hầu hết các ứng dụng web đều dựa vào. Thông thường, chúng có thể được sử dụng như một phương tiện để khai thác các lỗ hổng. Cơ chế cookie cho phép máy chủ gửi các mục dữ liệu đến máy khách, mà máy khách sẽ lưu trữ và gửi lại cho máy chủ. Không giống như các loại tham số yêu cầu khác (những tham số trong chuỗi truy vấn URL hoặc nội dung thư), cookie tiếp tục được gửi lại trong mỗi yêu cầu tiếp theo mà ứng dụng hoặc người dùng không yêu cầu bất kỳ hành động cụ thể nào.  

Máy chủ phát hành cookie bằng cách sử dụng tiêu đề phản hồi Set-Cookie, như:  
    
    Set-Cookie: tracking=tI8rk7joMx44S2Uu85nSWc  
    
Sau đó, trình duyệt của người dùng sẽ tự động thêm tiêu đề sau vào các yêu cầu tiếp theo quay lại cùng một máy chủ:  
    
    Cookie: tracking=tI8rk7joMx44S2Uu85nSWc  
    
Các cookie thường bao gồm một cặp tên/giá trị, như được hiển thị, nhưng chúng có thể bao gồm bất kỳ chuỗi nào không chứa khoảng trắng. Nhiều cookie có thể được phát hành bằng cách sử dụng nhiều tiêu đề Set-Cookie trong phản hồi của máy chủ. Chúng được gửi trở lại máy chủ trong cùng một tiêu đề Cookie, với dấu chấm phẩy phân tách các cookie riêng lẻ khác nhau.  

Ngoài giá trị thực tế của cookie, tiêu đề Set-Cookie có thể bao gồm bất kỳ thuộc tính tùy chọn nào sau đây, có thể được sử dụng để kiểm soát cách trình duyệt xử lý cookie:  
    
    Expires đặt ngày cho đến khi cookie hợp lệ. Điều này khiến trình duyệt lưu cookie vào bộ lưu trữ liên tục và cookie này được sử dụng lại trong các phiên trình duyệt tiếp theo cho đến khi đạt đến ngày hết hạn. Nếu thuộc tính này không được đặt, thì cookie chỉ được sử dụng trong phiên trình duyệt hiện tại.  
    
    Domain chỉ định tên miền mà cookie hợp lệ. Tên này phải giống hoặc tên gốc của tên miền mà từ đó cookie được nhận.  
    
    Path chỉ định đường dẫn URL mà cookie hợp lệ.  
    
    Secure - Nếu thuộc tính này được đặt, cookie sẽ chỉ được gửi trong các yêu cầu HTTPS.  
    
    HttpOnly - Nếu thuộc tính này được đặt, cookie không thể được truy cập trực tiếp qua JavaScript phía máy khách.  
    
Mỗi thuộc tính cookie này có thể ảnh hưởng đến bảo mật của ứng dụng. Tác động chính là khả năng kẻ tấn công nhắm mục tiêu trực tiếp vào những người dùng khác của ứng dụng.  
