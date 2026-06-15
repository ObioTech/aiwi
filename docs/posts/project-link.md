# Project Link: Khi các Project Brain có thể đọc nhau

Mỗi project phần mềm thường có một "vùng ngữ cảnh" (context) riêng biệt. Với AIWI, mỗi project có thể có một **Project Brain** riêng, đóng vai trò như một bộ não lưu trữ toàn bộ documents, code context, decisions, và memory của dự án đó.

Tuy nhiên, trong các hệ thống thực tế, các project thường xuyên giao tiếp với nhau. Làm sao để AI agent khi code frontend có thể hiểu được backend API mà không cần gộp chung source code?

Đó là lúc **Project Link** phát huy tác dụng.

## Read-only Linking

Một project có thể tạo link read-only tới Project Brain của project khác.

Ví dụ: Bạn đang code một React Native app. App này cần gọi tới một Odoo backend. Thay vì bắt AI agent đoán cấu trúc API hoặc phải clone cả source code backend nặng nề về máy, React Native project có thể "link" thẳng tới Project Brain của Odoo backend.

Khi đó, AI Agent đang làm việc trên React Native có thể dễ dàng tra cứu:
- API contracts.
- Data models và services.
- Architectural decisions.
- Code context từ backend.

Tất cả diễn ra:
- **Không cần merge source code:** Giữ nguyên tính độc lập của từng repository.
- **Không cần re-index:** Dữ liệu đã được index ở backend Brain có thể được đọc trực tiếp.
- **Không mutate dữ liệu backend:** Kết nối hoàn toàn là read-only, bảo vệ tính toàn vẹn của backend Brain.

## Tính minh bạch và Giới hạn ngữ cảnh (Explicit Scope)

Việc link giữa các Project Brain được thiết kế với sự rõ ràng:
- **Provenance (Nguồn gốc rõ ràng):** Agent luôn biết thông tin nào đến từ Brain nào.
- **Explicit Scope:** Chỉ những phần ngữ cảnh được public qua interface mới được chia sẻ.
- **Không tự ý suy diễn cross-project dependency:** Hệ thống sẽ không tự động tạo ra các ranh giới phụ thuộc mập mờ giữa các project nếu không có evidence rõ ràng.

Project Link mở ra một cách tiếp cận mới cho các AI agents khi làm việc trong các hệ thống microservices hoặc các kiến trúc đa dự án phân định ranh giới rõ ràng: **Hiểu toàn cảnh hệ thống một cách an toàn và nhẹ nhàng.**
