---
title: "Project Link: When Project Brains Can Read Each Other"
permalink: /posts/project-link/
---

# Project Link: When Project Brains Can Read Each Other

*(Vietnamese version below)*

Every software project usually has its own distinct context boundary. With ObiBrain, each project can have its own **Project Brain**, acting as a repository that stores all documents, code context, decisions, and memory for that specific project.

However, in real-world systems, projects frequently communicate with each other. How can an AI agent coding a frontend application understand the backend API without merging the source code?

That's the idea behind **Project Link**.

## Read-only Linking

Project Link explores a read-only way for one Project Brain to query selected evidence from another Project Brain.

For example: You are coding a React Native app that needs to call an Odoo backend. Instead of forcing the AI agent to guess the API structure or cloning the heavy backend source code to your machine, the React Native project can "link" directly to the Odoo backend's Project Brain.

Then, the AI Agent working on React Native can look up:
- API contracts.
- Data models and services.
- Architectural decisions.
- Code context from the backend.

Everything happens with:
- **No source code merging:** Preserves the independence of each repository.
- **No re-indexing:** Data already indexed in the backend Brain can be read directly.
- **No data mutation:** The connection is strictly read-only, protecting the integrity of the backend Brain.

## Transparency and Explicit Scope

Linking between Project Brains is designed with clarity in mind:
- **Provenance:** The agent always knows which Brain the information comes from.
- **Explicit Scope:** Only context explicitly exposed through the interface is shared.
- **No cross-project dependency inference:** The system will not automatically infer vague dependency boundaries between projects without explicit evidence.

Project Link opens up a new approach for AI agents working in microservices systems or multi-project architectures with clear boundaries: **Understanding the entire system safely and lightly.**

---

# Project Link: Khi các Project Brain có thể đọc nhau

Mỗi project phần mềm thường có một "vùng ngữ cảnh" (context) riêng biệt. Với ObiBrain, mỗi project có thể có một **Project Brain** riêng, đóng vai trò như một bộ não lưu trữ toàn bộ documents, code context, decisions, và memory của dự án đó.

Tuy nhiên, trong các hệ thống thực tế, các project thường xuyên giao tiếp với nhau. Làm sao để AI agent khi code frontend có thể hiểu được backend API mà không cần gộp chung source code?

Đó là ý tưởng phía sau **Project Link**.

## Read-only Linking

Project Link khám phá một cách tiếp cận read-only để một Project Brain có thể truy vấn phần evidence được chọn lọc từ Project Brain khác.

Ví dụ: Bạn đang code một React Native app. App này cần gọi tới một Odoo backend. Thay vì bắt AI agent đoán cấu trúc API hoặc phải clone cả source code backend nặng nề về máy, React Native project có thể "link" thẳng tới Project Brain của Odoo backend.

Khi đó, AI Agent đang làm việc trên React Native có thể tra cứu:
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
