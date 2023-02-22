HTTP hỗ trợ một số lượng lớn tiêu đề, một số tiêu đề được thiết kế cho các mục đích bất thường cụ thể. Một số tiêu đề có thể được sử dụng cho cả yêu cầu và phản hồi, và một số tiêu đề khác dành riêng cho một trong các loại thông báo này.  

General Header:  

    CONNECT cho đầu kia của giao tiếp biết liệu nó có nên đóng kết nối TCP sau khi quá trình truyền HTTP hoàn tất hay giữ nó mở cho các thông báo tiếp theo.  
    
    Content-Encoding chỉ định loại mã hóa nào đang được sử dụng cho nội dung chứa trong nội dung thư, chẳng hạn như gzip, được một số ứng dụng sử dụng để nén phản hồi nhằm truyền nhanh hơn.  
    
    Content-Length chỉ định độ dài của nội dung thư, tính bằng byte (ngoại trừ trường hợp phản hồi cho yêu cầu HEAD, khi nó chỉ ra độ dài của nội dung trong phản hồi cho yêu cầu GET tương ứng).  
    
    Content-Type chỉ định loại nội dung có trong nội dung thư, chẳng hạn như văn bản/html cho tài liệu HTML.  
    
    Transfer-Encoding chỉ định bất kỳ mã hóa nào được thực hiện trên nội dung thư để tạo điều kiện chuyển nó qua HTTP. Nó thường được sử dụng để chỉ định mã hóa khối khi điều này được sử dụng.  
    
Request Headers:  
    
    Accept cho máy chủ biết loại nội dung nào mà máy khách sẵn sàng chấp nhận, chẳng hạn như loại hình ảnh, định dạng tài liệu văn phòng, v.v.  
    
    Accept-Encoding cho máy chủ biết loại mã hóa nội dung nào mà máy khách sẵn sàng chấp nhận.  
    
    Authorization gửi thông tin đăng nhập tới máy chủ cho một trong các loại xác thực HTTP tích hợp.  
    
    Cookie là những tập tin một trang web gửi đến máy người dùng và được lưu lại thông qua trình duyệt khi người dùng truy cập trang web đó. Cookie được dùng với mục đích phổ biến là để lưu trữ phiên đăng nhập nhằm phục vụ cho mục đích xác thực với website, duy trì trạng thái đăng nhập. Ngoài ra, cookie còn được dùng để ghi nhớ thông tin trạng thái (ví dụ, quốc gia, ngôn ngữ), ghi nhớ hoạt động người dùng thực hiện trong quá trình truy cập và duyệt một trang web (ví dụ, những nút bấm hay đường liên kết người dùng tương tác). Cookie cũng được dùng để lưu lại các thông tin khác mà người dùng nhập hay điền vào trang web như tên, địa chỉ, email, v.v.  
    
    Host chỉ định tên máy chủ xuất hiện trong URL đầy đủ được yêu cầu.  
    
    If-Modified-Since chỉ định khi trình duyệt nhận được tài nguyên được yêu cầu lần cuối. Nếu tài nguyên không thay đổi kể từ thời điểm đó, máy chủ có thể hướng dẫn máy khách sử dụng bản sao được lưu trong bộ nhớ cache của nó, sử dụng phản hồi có mã trạng thái 304.  
    
    If-None-Match chỉ định một thẻ thực thể, là một mã định danh biểu thị nội dung của nội dung thư. Trình duyệt gửi thẻ thực thể mà máy chủ đã cấp cùng với tài nguyên được yêu cầu khi nó được nhận lần cuối. Máy chủ có thể sử dụng thẻ thực thể để xác định xem trình duyệt có thể sử dụng bản sao tài nguyên được lưu trong bộ nhớ cache của nó hay không.  
    
    Origin cho biết nguồn gốc truy vấn đến từ đâu. Nội dung của nó bao gồm tên miền của truy vấn (giao thức, địa chỉ, port nếu có) và không bao gồm bất cứ đường dẫn nào khác. Nó được gửi đi trong một truy vấn CORS và POST. Origin tương tự như Referer tuy nhiên khác với Referer, Origin không cho biết toàn bộ đường dẫn của website gửi truy vấn đi.  
    
    Referrer chỉ định URL mà từ đó yêu cầu hiện tại bắt nguồn.  
    
    User-Agent cung cấp thông tin về trình duyệt hoặc phần mềm máy khách khác đã tạo ra yêu cầu.  
    
Response Headers:  
    
    Access-Control-Allow-Origin là một cơ chế cho phép các tài nguyên bị hạn chế trên trang web được yêu cầu từ một miền khác bên ngoài miền mà từ đó tài nguyên đầu tiên được phân phát. Một trang web có thể tự do nhúng các hình ảnh, bảng định kiểu, tập lệnh, iframe và video có nguồn gốc chéo.  
    
    Cache-Control chuyển các chỉ thị bộ đệm tới trình duyệt (vd, no-cache).  
    
    ETag chỉ định một thẻ thực thể. Khách hàng có thể gửi mã nhận dạng này trong các yêu cầu tương lai cho cùng một tài nguyên trong If-None-Match để thông báo cho máy chủ phiên bản tài nguyên nào mà trình duyệt hiện đang lưu trong bộ đệm của nó.  
    
    Expires được sử dụng để thông báo cho khách hàng khi phản hồi HTTP hiện tại hết hạn. Nó chứa ngày và giờ cụ thể, mặc dù nếu thay vào đó nó chứa số 0 thì phản hồi HTTP đã hết hạn.  
    
    Location được sử dụng trong phản hồi chuyển hướng (những phản hồi có mã trạng thái bắt đầu bằng 3) để chỉ định mục tiêu của chuyển hướng.  
    
    Pragma giống với Cache-Control.  
    
    Server cung cấp thông tin về phần mềm máy chủ web đang được sử dụng.  
    
    Set-Cookie cấp cookie cho trình duyệt mà nó sẽ gửi lại cho máy chủ trong các yêu cầu tiếp theo.  
    
    WWW-Authenticate được sử dụng trong các phản hồi có mã trạng thái 401 để cung cấp chi tiết về các loại xác thực mà máy chủ hỗ trợ.  
    
    X-Frame-Options có thể được sử dụng để cho biết liệu trình duyệt có được phép hiển thị trang trong <frame>, <iframe>, <embed> hoặc <object> hay không. Các trang web có thể sử dụng điều này để tránh các cuộc tấn công nhấp chuột, bằng cách đảm bảo rằng nội dung của chúng không được nhúng vào các trang web khác.  
    
