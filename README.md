# Antsomi CDP — AI Agent Đánh giá Use Case

Web app cho phép brand mô tả một bài toán marketing bằng ngôn ngữ tự nhiên,
AI Agent đối chiếu với năng lực nền tảng Antsomi CDP 365 và trả về phán quyết
khả thi.

## Cấu trúc

- `index.html` — trang giao diện.
- `api/evaluate.js` — lớp trung gian, giữ API key và gọi Anthropic.

## Cách triển khai (deploy)

1. Đưa toàn bộ thư mục này lên một repository GitHub.
2. Vào vercel.com, đăng nhập bằng tài khoản GitHub, chọn Import repository này.
3. Trong phần Environment Variables của Vercel, thêm một biến:
   - Tên: `ANTHROPIC_API_KEY`
   - Giá trị: API key lấy từ console.anthropic.com
4. Bấm Deploy. Vercel trả về một link công khai.

## Lưu ý

- API key chỉ được lưu trên Vercel, không nằm trong mã nguồn — an toàn.
- Mỗi lượt đánh giá gọi Anthropic API và phát sinh chi phí theo lượng dùng.
