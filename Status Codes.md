Status Code là câu trả lời của máy chủ (server) cho yêu cầu đến từ máy khách (client). Khi bạn truy cập tới một trang web nào đó, mã trạng thái HTTP là thông báo từ server phản hồi cho yêu cầu truy cập đó của bạn. Mã trạng thái HTTP không phải là nội dung của trang web. Bạn có thể xem nó như ghi chú chú thích về việc gì đang diễn ra tại trang web này.  

Mỗi thông báo phản hồi HTTP phải chứa mã trạng thái trong dòng đầu tiên, cho biết kết quả của yêu cầu. Các mã trạng thái được chia thành năm nhóm, theo chữ số đầu tiên của mã:  
    
    1xx - Thông tin.  
    
    2xx - Yêu cầu đã thành công.  
    
    3xx - Máy khách được chuyển hướng đến một tài nguyên khác.  
    
    4xx - Yêu cầu chứa lỗi thuộc một số loại.  
    
    5xx - Máy chủ gặp lỗi khi thực hiện yêu cầu.  
    
Có rất nhiều mã trạng thái cụ thể, nhiều mã chỉ được sử dụng trong các trường hợp đặc biệt. Dưới đây là các mã trạng thái mà bạn có nhiều khả năng gặp phải nhất:  
    
    100 Continue được gửi trong một số trường hợp khi khách hàng gửi yêu cầu có chứa nội dung. Phản hồi chỉ ra rằng các tiêu đề yêu cầu đã được nhận và máy khách sẽ tiếp tục gửi phần thân. Máy chủ trả về phản hồi thứ hai khi yêu cầu đã được hoàn thành.  
    
    200 OK cho biết rằng yêu cầu đã thành công và nội dung phản hồi chứa kết quả của yêu cầu.  
    
    201 Created được trả về để phản hồi yêu cầu PUT để cho biết rằng yêu cầu đã thành công.  
    
    301  Moved Permanently chuyển hướng trình duyệt vĩnh viễn đến một URL khác, URL này được chỉ định trong Location. Khách hàng nên sử dụng URL mới trong tương lai thay vì URL gốc.  
    
    302 Found tạm thời chuyển hướng trình duyệt đến một URL khác, URL này được chỉ định trong Location. Máy khách sẽ hoàn nguyên về URL ban đầu trong các yêu cầu tiếp theo.  
    
    304 Not Modified hướng dẫn trình duyệt sử dụng bản sao được lưu trong bộ nhớ cache của tài nguyên được yêu cầu. Máy chủ sử dụng các tiêu đề yêu cầu If-Modified-Since và If-None-Match để xác định xem máy khách có phiên bản tài nguyên mới nhất hay không.  
    
    400 Bad Request cho biết rằng khách hàng đã gửi một yêu cầu HTTP không hợp lệ. Bạn có thể gặp phải điều này khi bạn đã sửa đổi một yêu cầu theo một số cách không hợp lệ, chẳng hạn như bằng cách đặt một ký tự khoảng trắng vào URL.  
    
    401 Unauthorized cho biết rằng máy chủ yêu cầu xác thực HTTP trước khi yêu cầu được cấp. Tiêu đề WWW-Authenticate chứa thông tin chi tiết về các loại xác thực được hỗ trợ.  
    
    403 Forbidden chỉ ra rằng không ai được phép truy cập tài nguyên được yêu cầu, bất kể xác thực.  
    
    404 Not Found chỉ ra rằng tài nguyên được yêu cầu không tồn tại.  
    
    405 Method Not Allowed cho biết rằng phương thức được sử dụng trong yêu cầu không được hỗ trợ cho URL đã chỉ định. Ví dụ: bạn có thể nhận được mã trạng thái này nếu bạn cố gắng sử dụng phương thức PUT khi nó không được hỗ trợ.
    
    413 Request Entity Too Large - Nếu bạn đang thăm dò các lỗ hổng tràn bộ đệm trong mã gốc và do đó đang gửi các chuỗi dữ liệu dài, thì điều này cho thấy phần nội dung yêu cầu của bạn quá lớn để máy chủ xử lý.  
    
    414 Request URI Too Long tương tự như phản hồi 413. Nó chỉ ra rằng URL được sử dụng trong yêu cầu quá lớn để máy chủ xử lý.  
    
    500 Internal Server Error cho biết rằng máy chủ đã gặp lỗi khi thực hiện yêu cầu. Điều này thường xảy ra khi bạn đã gửi thông tin đầu vào không mong muốn gây ra lỗi chưa được xử lý ở đâu đó trong quá trình xử lý của ứng dụng. Bạn nên xem kỹ toàn bộ nội dung phản hồi của máy chủ để biết bất kỳ chi tiết nào cho thấy bản chất của lỗi.  
    
    503 Service Unavailable thường chỉ ra rằng, mặc dù bản thân máy chủ web đang hoạt động và có thể phản hồi các yêu cầu, nhưng ứng dụng được truy cập qua máy chủ không phản hồi. Bạn nên xác minh xem đây có phải là kết quả của bất kỳ hành động nào bạn đã thực hiện hay không.  
    
