Một proxy HTTP là một máy chủ làm trung gian truy cập giữa trình duyệt máy khách và máy chủ đích. Khi một trình duyệt đã được định cấu hình để sử dụng máy chủ proxy, trình duyệt sẽ thực hiện tất cả các yêu cầu của nó tới máy chủ đó. Proxy chuyển tiếp các yêu cầu đến các máy chủ có liên quan và chuyển tiếp phản hồi của chúng trở lại trình duyệt. Hầu hết các proxy cũng cung cấp các dịch vụ bổ sung, bao gồm bộ nhớ đệm, xác thực và kiểm soát truy cập.  

Có hai điểm khác biệt trong cách thức hoạt động của HTTP khi máy chủ proxy đang được sử dụng:  
    
    Khi trình duyệt đưa ra yêu cầu HTTP không được mã hóa tới máy chủ proxy, trình duyệt sẽ đặt URL đầy đủ vào yêu cầu, bao gồm tiền tố giao thức http://, tên máy chủ của máy chủ và số cổng nếu đây không phải là tiêu chuẩn. Máy chủ proxy trích xuất tên máy chủ và cổng và sử dụng những thông tin này để hướng yêu cầu đến đúng máy chủ đích.  
    
    Khi HTTPS đang được sử dụng, trình duyệt không thể thực hiện quá trình bắt tay SSL với máy chủ proxy, vì điều này sẽ phá vỡ đường hầm an toàn và khiến các giao tiếp dễ bị tấn công chặn. Do đó, trình duyệt phải sử dụng proxy làm chuyển tiếp cấp TCP thuần túy, chuyển tiếp tất cả dữ liệu mạng theo cả hai hướng giữa trình duyệt và máy chủ đích, qua đó trình duyệt thực hiện bắt tay SSL như bình thường. Để thiết lập chuyển tiếp này, trình duyệt tạo một yêu cầu HTTP tới máy chủ proxy bằng phương thức CONNECT và chỉ định tên máy chủ đích và số cổng làm URL. Nếu proxy cho phép yêu cầu, nó sẽ trả về phản hồi HTTP với trạng thái 200, giữ kết nối TCP mở và từ thời điểm đó trở đi hoạt động như một chuyển tiếp cấp TCP thuần túy tới
máy chủ đích.  

Bằng nhiều cách khác nhau, mục hữu ích nhất trong bộ công cụ của bạn khi tấn công các ứng dụng web là một loại máy chủ proxy chuyên dụng nằm giữa trình duyệt của bạn và trang web mục tiêu, đồng thời cho phép bạn chặn và sửa đổi tất cả các yêu cầu và phản hồi, ngay cả những yêu cầu và phản hồi sử dụng HTTPS.  
