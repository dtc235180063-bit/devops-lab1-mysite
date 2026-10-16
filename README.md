# DevOps Lab 1 — Trải nghiệm DevOps Workflow End-to-End

## 1. Thông tin sinh viên
- **Họ và tên:** Nguyễn Văn Hải
- **Mã sinh viên:** DTC235180063
- **Lớp:** KTPMK22C
- **Khoa:** Công nghệ Thông tin
- **Trường:** Đại học Công nghệ Thông tin & Truyền thông (ICTU)
- **Học phần:** Vận hành và Bảo trì Phần mềm với DevOps (2026)

---

## 2. Thông tin dự án Lab 1
- **GitHub Repository:** [dtc235180063-bit/devops-lab1-mysite](https://github.com/dtc235180063-bit/devops-lab1-mysite)
- **GitHub Pages URL:** [https://dtc235180063-bit.github.io/devops-lab1-mysite/](https://dtc235180063-bit.github.io/devops-lab1-mysite/)
- **CI/CD Pipeline:** GitHub Actions (`.github/workflows/deploy.yml`)

---

## 3. Cấu trúc thư mục dự án
```
devops-lab1-mysite/
├── .github/
│   └── workflows/
│       └── deploy.yml          # GitHub Actions CI/CD Pipeline
├── index.html                  # Trang Portfolio cá nhân (HTML5/CSS3/JS)
└── README.md                   # Báo cáo và tài liệu dự án
```

---

## 4. Quy trình CI/CD Pipeline
Mỗi khi lập trình viên thực hiện `git push origin main`:
1. **Trigger:** Sự kiện push vào nhánh `main` kích hoạt GitHub Actions workflow `🚀 Deploy to GitHub Pages`.
2. **Checkout Code:** Runner ảo `ubuntu-latest` tải toàn bộ mã nguồn của commit mới nhất.
3. **Validate HTML:** Kiểm tra tệp `index.html` tồn tại và kiểm tra dung lượng tệp.
4. **Deploy to GitHub Pages:** Sử dụng action `peaceiris/actions-gh-pages@v3` đóng gói và đẩy trang tĩnh sang nhánh `gh-pages`.
5. **Live:** GitHub Pages tự động phát hành trang web lên Internet qua URL public trong vòng vài giây.
