# Sổ tay — bản đã khoá

Ghi chú học tập cá nhân, **đã mã hoá**. Repo này chỉ chứa bản mã, không chứa nội dung dạng chữ thường.

Mở tại: **https://thekizzz.github.io/ecom-mrr-sotay/**

Cần mật khẩu để mở. Không có mật khẩu thì mọi file ở đây chỉ là chuỗi base64 vô nghĩa.

## Cách khoá

- PBKDF2-SHA256, 600.000 vòng lặp, salt ngẫu nhiên riêng cho từng trang
- AES-256-GCM
- Giải mã ngay trên trình duyệt bằng Web Crypto — không tải thư viện ngoài, không gọi server
- Mật khẩu nhớ trong `sessionStorage`, đóng tab là mất, không ghi xuống đĩa

## Giới hạn — nói thẳng

- Ai có mật khẩu đều có thể chuyển cho người khác.
- Bản mã nằm công khai, nên về lý thuyết có thể thử mật khẩu offline không giới hạn.
  600.000 vòng PBKDF2 làm việc đó rất chậm và tốn kém, nhưng không loại trừ được.
- Muốn chặt hơn thì cần host kiểm tra danh tính phía server (Cloudflare Access
  có gói free tới 50 người), hoặc GitHub Pro để dùng Pages trên repo private.

Bản gốc dạng chữ thường nằm ở một repo private riêng, không nằm ở đây.
