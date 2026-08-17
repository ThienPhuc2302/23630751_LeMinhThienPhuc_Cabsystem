# 23630751_LeMinhThienPhuc_Cabsystem
## 1. Phân tích nghiệp vụ
### Hiện tại, Công ty ABC đang gặp nhiều khó khăn trong hoạt động đặt xe do việc phân công tài xế chủ yếu được thực hiện thủ công, khách hàng khó theo dõi trạng thái chuyến đi, thông tin thanh toán chưa được quản lý tập trung và bộ phận vận hành gặp nhiều hạn chế khi số lượng khách hàng, tài xế tăng lên. Ngoài ra, doanh nghiệp chưa có cơ chế tự động tìm và phân công tài xế phù hợp, xử lý trường hợp tài xế từ chối hoặc không phản hồi, cũng như chưa quản lý hiệu quả dữ liệu chuyến đi, giao dịch và hoạt động của tài xế. 
### Vì vậy, doanh nghiệp cần xây dựng một hệ thống CAB nhằm số hóa và tự động hóa toàn bộ quy trình đặt xe. Hệ thống cho phép khách hàng đăng ký, quản lý thông tin, nhập điểm đón và điểm đến, lựa chọn loại xe, gửi yêu cầu đặt xe và theo dõi trạng thái chuyến. Hệ thống tự động tìm kiếm và phân công tài xế dựa trên vị trí, trạng thái sẵn sàng và các tiêu chí vận hành; nếu tài xế không phản hồi hoặc từ chối, hệ thống tiếp tục tìm tài xế khác và thông báo cho khách hàng khi không tìm được tài xế. Tài xế có thể quản lý hồ sơ, phương tiện, trạng thái hoạt động, nhận hoặc từ chối chuyến và cập nhật trạng thái trong quá trình thực hiện chuyến. Sau khi chuyến hoàn thành, hệ thống thực hiện tính cước, hỗ trợ thanh toán bằng tiền mặt hoặc thanh toán điện tử thông qua nhà cung cấp bên ngoài, đồng thời quản lý lịch sử giao dịch và xử lý trường hợp thanh toán thất bại. Nhân viên vận hành có thể quản lý khách hàng, tài xế, phương tiện và chuyến đi, theo dõi các chuyến đang diễn ra, xử lý sự cố và tra cứu lịch sử. 
### Bên cạnh đó, hệ thống cung cấp thông báo cho khách hàng và tài xế, phân quyền người dùng, lưu vết các thao tác quan trọng và cung cấp báo cáo về số lượng chuyến, doanh thu, tỷ lệ hoàn thành, tỷ lệ hủy và hiệu quả hoạt động của tài xế. Hệ thống được định hướng xây dựng linh hoạt, có khả năng mở rộng để đáp ứng nhu cầu tăng trưởng và bổ sung các loại dịch vụ, phương thức thanh toán hoặc kênh thông báo mới trong tương lai.
## 2. Stakeholder

| Tên Stakeholder | Vai trò |
|:---|:---|
| Ban lãnh đạo | Định hướng, phê duyệt và đưa ra các quyết định quan trọng của dự án |
| Khách hàng | Đăng ký, đặt xe, theo dõi chuyến, thanh toán và đánh giá tài xế |
| Tài xế | Nhận chuyến, thực hiện chuyến và cập nhật trạng thái chuyến đi |
| Nhân viên vận hành | Quản lý khách hàng, tài xế, phương tiện, chuyến đi và xử lý sự cố |
| Nhà cung cấp thanh toán | Cung cấp dịch vụ và xử lý các giao dịch thanh toán điện tử |
| Bộ phận tài chính / kế toán | Quản lý doanh thu, giao dịch, đối soát và báo cáo tài chính |
| Nhà cung cấp bản đồ / định vị | Cung cấp dữ liệu vị trí, bản đồ, khoảng cách và hỗ trợ xác định tài xế |
| Nhà cung cấp dịch vụ thông báo | Cung cấp kênh gửi như thông báo ứng dụng, tin nhắn, thư điện tử... |
## Stakeholder matrix

```mermaid
quadrantChart
    title Power - Interest Matrix
    x-axis "Low Interest" --> "High Interest"
    y-axis "Low Power" --> "High Power"

    quadrant-1 "Manage Closely"
    quadrant-2 "Keep Satisfied"
    quadrant-3 "Monitor"
    quadrant-4 "Keep Informed"

    "Ban lãnh đạo": [0.90, 0.95]
    "Khách hàng": [0.90, 0.30]
    "Tài xế": [0.82, 0.35]
    "Nhân viên vận hành": [0.85, 0.80]
    "Nhà cung cấp thanh toán": [0.55, 0.75]
    "Bộ phận tài chính / kế toán": [0.80, 0.85]
    "Nhà cung cấp bản đồ / định vị": [0.50, 0.55]
    "Nhà cung cấp dịch vụ thông báo": [0.55, 0.60]
```
## 3. Business Goals

| Mã | Business Goal | Mô tả |
|:---|:---|:---|
| **BG01** | **Tự động hóa và tối ưu hóa hoạt động điều phối xe** | Chuyển đổi quy trình tiếp nhận và phân công chuyến từ thủ công sang tự động, giảm thời gian xử lý yêu cầu và nâng cao hiệu quả sử dụng đội ngũ tài xế. |
| **BG02** | **Nâng cao chất lượng dịch vụ và trải nghiệm khách hàng** | Cung cấp quy trình đặt xe minh bạch, thuận tiện và có khả năng theo dõi xuyên suốt từ khi tạo yêu cầu đến khi hoàn thành chuyến, đồng thời cung cấp thông tin kịp thời thông qua hệ thống thông báo. |
| **BG03** | **Nâng cao hiệu quả quản lý và vận hành** | Cung cấp cho bộ phận vận hành khả năng theo dõi tập trung khách hàng, tài xế, phương tiện và chuyến đi; hỗ trợ xử lý các tình huống bất thường và đưa ra quyết định dựa trên dữ liệu vận hành. |
| **BG04** | **Chuẩn hóa và kiểm soát hoạt động tính cước, thanh toán và doanh thu** | Quản lý thống nhất quá trình tính cước và thanh toán, hỗ trợ nhiều phương thức thanh toán, kiểm soát trạng thái giao dịch và cung cấp dữ liệu phục vụ đối soát, quản lý doanh thu và báo cáo. |
| **BG05** | **Tăng cường khả năng kiểm soát và khai thác dữ liệu** | Hình thành nguồn dữ liệu tập trung về khách hàng, tài xế, phương tiện, chuyến đi và giao dịch nhằm phục vụ vận hành, tra cứu, báo cáo và phân tích hiệu quả kinh doanh. |
| **BG06** | **Đảm bảo tính liên tục và khả năng mở rộng của hoạt động kinh doanh** | Xây dựng nền tảng có khả năng đáp ứng sự gia tăng về số lượng khách hàng, tài xế và chuyến đi; hạn chế việc một thành phần gặp sự cố làm gián đoạn toàn bộ dịch vụ. |
| **BG07** | **Tạo nền tảng linh hoạt cho việc phát triển dịch vụ trong tương lai** | Cho phép doanh nghiệp bổ sung loại hình dịch vụ, phương thức thanh toán, kênh thông báo và các thành phần tích hợp mới mà không phải thay đổi lớn toàn bộ hệ thống. |
| **BG08** | **Đảm bảo an toàn thông tin và tuân thủ trong hoạt động kinh doanh** | Bảo vệ thông tin cá nhân, dữ liệu vị trí và dữ liệu giao dịch; kiểm soát quyền truy cập, lưu vết các thao tác quan trọng và hỗ trợ truy xuất khi phát sinh sự cố. |
## 4. Phạm vi dự án

Trong thời gian 7 tuần, dự án tập trung xây dựng các chức năng cơ bản và cần thiết để hệ thống CAB có thể vận hành như một nền tảng đặt xe trực tuyến, đồng thời hỗ trợ nhân viên vận hành quản lý khách hàng, tài xế, phương tiện và chuyến đi.

| STT | Module | Nội dung |
|:---:|:---|:---|
| 1 | **Quản lý khách hàng** | Quản lý thông tin tài khoản, hồ sơ, trạng thái hoạt động và lịch sử chuyến đi của khách hàng. |
| 2 | **Quản lý tài xế** | Quản lý thông tin tài khoản, hồ sơ, trạng thái hoạt động và thông tin phương tiện của tài xế. |
| 3 | **Đặt xe** | Khách hàng nhập điểm đón, điểm đến, lựa chọn loại xe và gửi yêu cầu đặt xe. |
| 4 | **Tìm và phân công tài xế** | Hệ thống tìm tài xế phù hợp dựa trên vị trí, trạng thái sẵn sàng và các tiêu chí cơ bản. |
| 5 | **Quản lý chuyến đi** | Tài xế nhận chuyến và cập nhật trạng thái trong quá trình thực hiện chuyến. |
| 6 | **Theo dõi chuyến đi** | Khách hàng theo dõi trạng thái và vị trí tài xế. |
| 7 | **Tính cước và thanh toán** | Tính số tiền phải trả và hỗ trợ thanh toán bằng tiền mặt hoặc thanh toán điện tử. |
| 8 | **Thông báo** | Gửi thông báo về các trạng thái quan trọng của chuyến đi cho khách hàng và tài xế. |
| 9 | **Quản lý vận hành** | Nhân viên vận hành theo dõi và xử lý khách hàng, tài xế, phương tiện và các chuyến đi đang diễn ra. |
| 10 | **Lịch sử và đánh giá** | Lưu lịch sử chuyến đi và cho phép khách hàng đánh giá tài xế sau khi hoàn thành chuyến. |
| 11 | **Bảo mật và phân quyền** | Xác thực người dùng, phân quyền chức năng quản trị và bảo vệ dữ liệu cơ bản. |
## 5. Business Requirements

Trong phạm vi MVP với thời gian triển khai **7 tuần**, hệ thống CAB tập trung vào các nghiệp vụ cốt lõi phục vụ toàn bộ quy trình đặt xe, từ quản lý người dùng, đặt xe, tìm tài xế, thực hiện chuyến, thanh toán đến quản lý vận hành và bảo mật.

| BR ID | Nhóm nghiệp vụ | Business Requirement |
|:---:|:---|:---|
| **BR01** | Quản lý khách hàng | Hệ thống phải hỗ trợ khách hàng đăng ký, đăng nhập và quản lý tài khoản để sử dụng dịch vụ CAB. |
| **BR02** | Quản lý khách hàng | Hệ thống phải cho phép khách hàng quản lý và cập nhật thông tin cá nhân cần thiết cho việc sử dụng dịch vụ. |
| **BR03** | Quản lý khách hàng | Hệ thống phải lưu trữ và hỗ trợ tra cứu lịch sử các chuyến đi của khách hàng. |
| **BR04** | Quản lý tài xế | Hệ thống phải hỗ trợ doanh nghiệp quản lý tài khoản và thông tin hồ sơ của tài xế. |
| **BR05** | Quản lý tài xế | Hệ thống phải hỗ trợ quản lý thông tin phương tiện và liên kết phương tiện với tài xế. |
| **BR06** | Quản lý tài xế | Hệ thống phải cho phép quản lý trạng thái hoạt động và khả năng sẵn sàng nhận chuyến của tài xế. |
| **BR07** | Đặt xe | Hệ thống phải cho phép khách hàng tạo yêu cầu đặt xe bằng cách cung cấp điểm đón, điểm đến và loại xe hoặc loại dịch vụ. |
| **BR08** | Đặt xe | Hệ thống phải quản lý trạng thái của yêu cầu đặt xe từ khi tạo yêu cầu đến khi được phân công, hoàn thành hoặc kết thúc. |
| **BR09** | Tìm và phân công tài xế | Hệ thống phải tự động tìm kiếm tài xế phù hợp khi khách hàng tạo yêu cầu đặt xe. |
| **BR10** | Tìm và phân công tài xế | Hệ thống phải xác định tài xế phù hợp dựa trên trạng thái sẵn sàng, vị trí và các tiêu chí vận hành do doanh nghiệp quy định. |
| **BR11** | Tìm và phân công tài xế | Hệ thống phải hỗ trợ gửi yêu cầu nhận chuyến và ghi nhận việc tài xế chấp nhận hoặc từ chối chuyến. |
| **BR12** | Tìm và phân công tài xế | Hệ thống phải tiếp tục tìm tài xế khác khi tài xế được đề xuất từ chối hoặc không phản hồi, đồng thời thông báo cho khách hàng khi không tìm được tài xế. |
| **BR13** | Quản lý chuyến đi | Hệ thống phải hỗ trợ tạo và quản lý chuyến đi sau khi tài xế chấp nhận yêu cầu đặt xe. |
| **BR14** | Quản lý chuyến đi | Hệ thống phải cho phép tài xế cập nhật các trạng thái chính của chuyến đi gồm đã đến điểm đón, đã đón khách, đang di chuyển và hoàn thành chuyến. |
| **BR15** | Quản lý chuyến đi | Hệ thống phải lưu trữ thông tin và trạng thái chuyến đi để phục vụ theo dõi, tra cứu, thanh toán và quản lý vận hành. |
| **BR16** | Theo dõi chuyến đi | Hệ thống phải cho phép khách hàng theo dõi trạng thái hiện tại và thông tin tài xế trong quá trình thực hiện chuyến. |
| **BR17** | Theo dõi chuyến đi | Hệ thống phải hỗ trợ theo dõi vị trí và thời gian dự kiến tài xế đến điểm đón. |
| **BR18** | Tính cước và thanh toán | Hệ thống phải xác định số tiền khách hàng phải trả dựa trên loại dịch vụ và thông tin chuyến đi theo chính sách của doanh nghiệp. |
| **BR19** | Tính cước và thanh toán | Hệ thống phải hỗ trợ khách hàng thanh toán bằng tiền mặt hoặc phương thức thanh toán điện tử. |
| **BR20** | Tính cước và thanh toán | Hệ thống phải tích hợp với nhà cung cấp thanh toán bên ngoài và không lưu trực tiếp thông tin nhạy cảm của thẻ hoặc tài khoản thanh toán. |
| **BR21** | Tính cước và thanh toán | Hệ thống phải quản lý kết quả giao dịch, thông báo khi thanh toán thất bại và hỗ trợ xử lý lại theo chính sách doanh nghiệp. |
| **BR22** | Thông báo | Hệ thống phải thông báo cho khách hàng về các sự kiện quan trọng của yêu cầu đặt xe và chuyến đi. |
| **BR23** | Thông báo | Hệ thống phải thông báo cho khách hàng về kết quả thanh toán và các thay đổi quan trọng liên quan đến chuyến đi. |
| **BR24** | Thông báo | Hệ thống phải thông báo cho tài xế khi có chuyến mới hoặc có thay đổi quan trọng liên quan đến chuyến đang thực hiện. |
| **BR25** | Quản lý vận hành | Hệ thống phải cung cấp cho nhân viên vận hành khả năng tra cứu và quản lý thông tin khách hàng, tài xế và phương tiện theo quyền được cấp. |
| **BR26** | Quản lý vận hành | Hệ thống phải cho phép nhân viên vận hành theo dõi các chuyến đang diễn ra và trạng thái hoạt động của tài xế. |
| **BR27** | Quản lý vận hành | Hệ thống phải hỗ trợ nhân viên vận hành tra cứu và xử lý các trường hợp chuyến đi phát sinh lỗi hoặc bất thường. |
| **BR28** | Quản lý vận hành | Hệ thống phải hỗ trợ tra cứu lịch sử giao dịch và thông tin liên quan phục vụ hoạt động vận hành. |
| **BR29** | Lịch sử và đánh giá | Hệ thống phải cho phép khách hàng tra cứu lịch sử chuyến đi và thông tin số tiền của các chuyến đã thực hiện. |
| **BR30** | Lịch sử và đánh giá | Hệ thống phải cho phép khách hàng đánh giá tài xế sau khi chuyến đi hoàn thành và lưu kết quả đánh giá. |
| **BR31** | Bảo mật và phân quyền | Hệ thống phải xác thực khách hàng, tài xế và nhân viên trước khi cho phép sử dụng các chức năng yêu cầu tài khoản. |
| **BR32** | Bảo mật và phân quyền | Hệ thống phải kiểm soát quyền truy cập dựa trên vai trò và đảm bảo nhân viên chỉ thực hiện được các chức năng được cấp quyền. |
| **BR33** | Bảo mật và phân quyền | Hệ thống phải bảo vệ thông tin cá nhân, thông tin phương tiện, dữ liệu vị trí và dữ liệu giao dịch khỏi truy cập trái phép. |
| **BR34** | Bảo mật và phân quyền | Hệ thống phải lưu vết các thao tác quan trọng để phục vụ kiểm tra, đối soát và xử lý sự cố. |
| **BR35** | Khả năng mở rộng | Hệ thống phải được thiết kế đủ linh hoạt để có thể mở rộng các loại dịch vụ, phương thức thanh toán và kênh thông báo trong tương lai mà hạn chế ảnh hưởng đến các chức năng hiện có. |

## 6. Functional Requirements

Functional Requirements (FR) được phân rã từ 35 Business Requirements (BR), mô tả các chức năng cụ thể mà hệ thống CAB cần cung cấp để đáp ứng phạm vi MVP trong thời gian 7 tuần.

## 6.1. Quản lý khách hàng

| FR ID | BR ID | Functional Requirement |
|:---:|:---:|:---|
| **FR01** | BR01 | Hệ thống cho phép khách hàng đăng ký tài khoản bằng các thông tin cần thiết. |
| **FR02** | BR01 | Hệ thống cho phép khách hàng đăng nhập và đăng xuất khỏi hệ thống. |
| **FR03** | BR01 | Hệ thống kiểm tra thông tin xác thực trước khi cho phép khách hàng sử dụng các chức năng yêu cầu tài khoản. |
| **FR04** | BR02 | Hệ thống cho phép khách hàng xem thông tin cá nhân của mình. |
| **FR05** | BR02 | Hệ thống cho phép khách hàng cập nhật thông tin cá nhân. |
| **FR06** | BR02 | Hệ thống lưu trữ thông tin cá nhân sau khi cập nhật thành công. |
| **FR07** | BR03 | Hệ thống lưu thông tin các chuyến đi đã phát sinh của khách hàng. |
| **FR08** | BR03 | Hệ thống cho phép khách hàng xem danh sách lịch sử chuyến đi. |
| **FR09** | BR03 | Hệ thống cho phép khách hàng xem chi tiết một chuyến đi trong lịch sử. |

## 6.2. Quản lý tài xế

| FR ID | BR ID | Functional Requirement |
|:---:|:---:|:---|
| **FR10** | BR04 | Hệ thống cho phép tài xế đăng ký tài khoản hoặc nhân viên vận hành tạo tài khoản tài xế. |
| **FR11** | BR04 | Hệ thống cho phép tài xế đăng nhập và đăng xuất. |
| **FR12** | BR04 | Hệ thống cho phép doanh nghiệp xem và cập nhật thông tin hồ sơ tài xế. |
| **FR13** | BR05 | Hệ thống cho phép nhân viên vận hành tạo thông tin phương tiện. |
| **FR14** | BR05 | Hệ thống cho phép cập nhật thông tin phương tiện. |
| **FR15** | BR05 | Hệ thống cho phép liên kết phương tiện với tài xế. |
| **FR16** | BR05 | Hệ thống cho phép tra cứu thông tin phương tiện đang được liên kết với tài xế. |
| **FR17** | BR06 | Hệ thống cho phép tài xế chuyển trạng thái sang sẵn sàng nhận chuyến. |
| **FR18** | BR06 | Hệ thống cho phép tài xế chuyển trạng thái sang không sẵn sàng nhận chuyến. |
| **FR19** | BR06 | Hệ thống cập nhật trạng thái hoạt động hiện tại của tài xế. |

## 6.3. Đặt xe

| FR ID | BR ID | Functional Requirement |
|:---:|:---:|:---|
| **FR20** | BR07 | Hệ thống cho phép khách hàng nhập hoặc lựa chọn điểm đón. |
| **FR21** | BR07 | Hệ thống cho phép khách hàng nhập hoặc lựa chọn điểm đến. |
| **FR22** | BR07 | Hệ thống cho phép khách hàng lựa chọn loại xe hoặc loại dịch vụ. |
| **FR23** | BR07 | Hệ thống hiển thị lại thông tin đặt xe để khách hàng kiểm tra trước khi xác nhận. |
| **FR24** | BR07 | Hệ thống cho phép khách hàng xác nhận và gửi yêu cầu đặt xe. |
| **FR25** | BR08 | Hệ thống tạo mã định danh cho mỗi yêu cầu đặt xe. |
| **FR26** | BR08 | Hệ thống quản lý trạng thái yêu cầu đặt xe. |
| **FR27** | BR08 | Hệ thống cập nhật trạng thái yêu cầu khi có thay đổi trong quá trình xử lý. |

## 6.4. Tìm và phân công tài xế

| FR ID | BR ID | Functional Requirement |
|:---:|:---:|:---|
| **FR28** | BR09 | Hệ thống tự động kích hoạt quá trình tìm kiếm tài xế khi nhận yêu cầu đặt xe hợp lệ. |
| **FR29** | BR09 | Hệ thống lấy danh sách các tài xế có khả năng nhận chuyến. |
| **FR30** | BR10 | Hệ thống lọc tài xế dựa trên trạng thái sẵn sàng nhận chuyến. |
| **FR31** | BR10 | Hệ thống sử dụng thông tin vị trí tài xế để xác định tài xế phù hợp. |
| **FR32** | BR10 | Hệ thống áp dụng các tiêu chí vận hành đã được doanh nghiệp cấu hình để lựa chọn tài xế. |
| **FR33** | BR10 | Hệ thống sắp xếp hoặc ưu tiên các tài xế phù hợp theo tiêu chí phân công. |
| **FR34** | BR11 | Hệ thống gửi yêu cầu nhận chuyến đến tài xế được lựa chọn. |
| **FR35** | BR11 | Hệ thống ghi nhận khi tài xế chấp nhận chuyến. |
| **FR36** | BR11 | Hệ thống ghi nhận khi tài xế từ chối chuyến. |
| **FR37** | BR12 | Hệ thống xác định trường hợp tài xế không phản hồi trong thời gian quy định. |
| **FR38** | BR12 | Hệ thống chuyển sang tài xế tiếp theo khi tài xế từ chối hoặc không phản hồi. |
| **FR39** | BR12 | Hệ thống tiếp tục quá trình tìm kiếm cho đến khi tìm được tài xế hoặc kết thúc quá trình tìm kiếm. |
| **FR40** | BR12 | Hệ thống cập nhật yêu cầu đặt xe khi không tìm được tài xế. |
| **FR41** | BR12 | Hệ thống thông báo cho khách hàng khi không tìm được tài xế. |

## 6.5. Quản lý chuyến đi

| FR ID | BR ID | Functional Requirement |
|:---:|:---:|:---|
| **FR42** | BR13 | Hệ thống tạo chuyến đi khi tài xế chấp nhận yêu cầu đặt xe. |
| **FR43** | BR13 | Hệ thống liên kết chuyến đi với khách hàng, tài xế và phương tiện. |
| **FR44** | BR13 | Hệ thống lưu thông tin điểm đón, điểm đến và loại dịch vụ của chuyến đi. |
| **FR45** | BR14 | Hệ thống cho phép tài xế cập nhật trạng thái đã đến điểm đón. |
| **FR46** | BR14 | Hệ thống cho phép tài xế cập nhật trạng thái đã đón khách. |
| **FR47** | BR14 | Hệ thống cho phép tài xế cập nhật trạng thái đang di chuyển. |
| **FR48** | BR14 | Hệ thống cho phép tài xế cập nhật trạng thái hoàn thành chuyến. |
| **FR49** | BR15 | Hệ thống lưu trữ thông tin và trạng thái của chuyến đi. |
| **FR50** | BR15 | Hệ thống cập nhật thông tin chuyến khi trạng thái chuyến thay đổi. |
| **FR51** | BR15 | Hệ thống cho phép tra cứu thông tin chuyến đi phục vụ vận hành và các nghiệp vụ sau chuyến. |

## 6.6. Theo dõi chuyến đi

| FR ID | BR ID | Functional Requirement |
|:---:|:---:|:---|
| **FR52** | BR16 | Hệ thống hiển thị trạng thái hiện tại của chuyến đi cho khách hàng. |
| **FR53** | BR16 | Hệ thống hiển thị thông tin tài xế đã nhận chuyến cho khách hàng. |
| **FR54** | BR17 | Hệ thống tiếp nhận và cập nhật thông tin vị trí của tài xế. |
| **FR55** | BR17 | Hệ thống hiển thị vị trí hiện tại của tài xế cho khách hàng trong phạm vi cho phép. |
| **FR56** | BR17 | Hệ thống cung cấp thời gian dự kiến tài xế đến điểm đón dựa trên dữ liệu vị trí và thông tin hành trình. |

## 6.7. Tính cước và thanh toán

| FR ID | BR ID | Functional Requirement |
|:---:|:---:|:---|
| **FR57** | BR18 | Hệ thống xác định số tiền phải trả dựa trên loại dịch vụ và thông tin chuyến đi. |
| **FR58** | BR18 | Hệ thống lưu thông tin cước của chuyến đi. |
| **FR59** | BR18 | Hệ thống hiển thị số tiền khách hàng phải thanh toán. |
| **FR60** | BR19 | Hệ thống cho phép khách hàng lựa chọn phương thức thanh toán bằng tiền mặt. |
| **FR61** | BR19 | Hệ thống cho phép khách hàng lựa chọn phương thức thanh toán điện tử. |
| **FR62** | BR20 | Hệ thống kết nối với nhà cung cấp dịch vụ thanh toán bên ngoài. |
| **FR63** | BR20 | Hệ thống gửi yêu cầu thanh toán đến nhà cung cấp thanh toán. |
| **FR64** | BR20 | Hệ thống không lưu trực tiếp thông tin nhạy cảm của thẻ hoặc tài khoản thanh toán. |
| **FR65** | BR21 | Hệ thống tiếp nhận kết quả giao dịch từ nhà cung cấp thanh toán. |
| **FR66** | BR21 | Hệ thống cập nhật trạng thái giao dịch theo kết quả thanh toán. |
| **FR67** | BR21 | Hệ thống thông báo cho khách hàng khi giao dịch thanh toán thất bại. |
| **FR68** | BR21 | Hệ thống cho phép thực hiện lại thanh toán theo chính sách của doanh nghiệp. |

## 6.8. Thông báo

| FR ID | BR ID | Functional Requirement |
|:---:|:---:|:---|
| **FR69** | BR22 | Hệ thống gửi thông báo cho khách hàng khi yêu cầu đặt xe được tiếp nhận. |
| **FR70** | BR22 | Hệ thống gửi thông báo cho khách hàng khi tài xế nhận chuyến. |
| **FR71** | BR22 | Hệ thống gửi thông báo cho khách hàng khi tài xế đến điểm đón. |
| **FR72** | BR22 | Hệ thống gửi thông báo cho khách hàng khi chuyến đi hoàn thành. |
| **FR73** | BR23 | Hệ thống gửi thông báo cho khách hàng về kết quả thanh toán. |
| **FR74** | BR23 | Hệ thống gửi thông báo cho khách hàng khi có thay đổi quan trọng liên quan đến chuyến đi. |
| **FR75** | BR24 | Hệ thống gửi thông báo cho tài xế khi có chuyến mới phù hợp. |
| **FR76** | BR24 | Hệ thống gửi thông báo cho tài xế khi có thay đổi quan trọng liên quan đến chuyến đang thực hiện. |

## 6.9. Quản lý vận hành

| FR ID | BR ID | Functional Requirement |
|:---:|:---:|:---|
| **FR77** | BR25 | Hệ thống cho phép nhân viên vận hành tra cứu thông tin khách hàng. |
| **FR78** | BR25 | Hệ thống cho phép nhân viên vận hành tra cứu và quản lý thông tin tài xế theo quyền được cấp. |
| **FR79** | BR25 | Hệ thống cho phép nhân viên vận hành tra cứu và quản lý thông tin phương tiện theo quyền được cấp. |
| **FR80** | BR26 | Hệ thống hiển thị danh sách các chuyến đang diễn ra. |
| **FR81** | BR26 | Hệ thống cho phép nhân viên vận hành xem trạng thái hiện tại của chuyến. |
| **FR82** | BR26 | Hệ thống cho phép nhân viên vận hành xem trạng thái hoạt động của tài xế. |
| **FR83** | BR27 | Hệ thống cho phép nhân viên vận hành tra cứu thông tin các chuyến bị lỗi hoặc bất thường. |
| **FR84** | BR27 | Hệ thống hỗ trợ nhân viên vận hành cập nhật hoặc xử lý trạng thái chuyến theo quyền được cấp. |
| **FR85** | BR28 | Hệ thống lưu trữ thông tin giao dịch phục vụ tra cứu. |
| **FR86** | BR28 | Hệ thống cho phép nhân viên vận hành tra cứu lịch sử giao dịch. |

## 6.10. Lịch sử và đánh giá

| FR ID | BR ID | Functional Requirement |
|:---:|:---:|:---|
| **FR87** | BR29 | Hệ thống cho phép khách hàng xem danh sách các chuyến đã thực hiện. |
| **FR88** | BR29 | Hệ thống cho phép khách hàng xem chi tiết chuyến và số tiền phải trả. |
| **FR89** | BR30 | Hệ thống cho phép khách hàng đánh giá tài xế sau khi chuyến đi hoàn thành. |
| **FR90** | BR30 | Hệ thống lưu kết quả đánh giá và liên kết với chuyến đi tương ứng. |

## 6.11. Bảo mật và phân quyền

| FR ID | BR ID | Functional Requirement |
|:---:|:---:|:---|
| **FR91** | BR31 | Hệ thống xác thực khách hàng, tài xế và nhân viên trước khi truy cập các chức năng yêu cầu tài khoản. |
| **FR92** | BR32 | Hệ thống xác định quyền truy cập dựa trên vai trò của người dùng. |
| **FR93** | BR32 | Hệ thống ngăn người dùng thực hiện các chức năng ngoài phạm vi quyền được cấp. |
| **FR94** | BR33 | Hệ thống kiểm soát quyền truy cập đối với thông tin cá nhân của khách hàng và tài xế. |
| **FR95** | BR33 | Hệ thống bảo vệ dữ liệu phương tiện và dữ liệu vị trí của tài xế. |
| **FR96** | BR33 | Hệ thống bảo vệ dữ liệu giao dịch và thông tin liên quan đến thanh toán. |
| **FR97** | BR34 | Hệ thống ghi nhận các thao tác quan trọng của người dùng và nhân viên vận hành. |
| **FR98** | BR34 | Hệ thống cho phép người dùng có quyền tra cứu lịch sử các thao tác quan trọng phục vụ kiểm tra và xử lý sự cố. |

## 6.12. Khả năng mở rộng

| FR ID | BR ID | Functional Requirement |
|:---:|:---:|:---|
| **FR99** | BR35 | Hệ thống cho phép bổ sung loại dịch vụ mới mà hạn chế ảnh hưởng đến các chức năng hiện có. |
| **FR100** | BR35 | Hệ thống cho phép bổ sung phương thức thanh toán mới thông qua cơ chế tích hợp phù hợp. |
| **FR101** | BR35 | Hệ thống cho phép bổ sung hoặc thay đổi kênh thông báo mà hạn chế thay đổi các nghiệp vụ hiện có. |
