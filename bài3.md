


# Phần 1: Báo cáo phân tích (I/O)

**Input:** Hai khung "Nội dung bài học" và "Danh sách video" bị chồng lấn.

**Sơ đồ Box Model (minh họa):**

```text
+--------- Margin ---------+
| +------- Border -------+ |
| | +----- Padding ----+ | |
| | |     Content      | | |
| | +------------------+ | |
| +----------------------+ |
+--------------------------+
```

- Content: Nội dung.
- Padding: Khoảng cách bên trong.
- Border: Đường viền.
- Margin: Khoảng cách bên ngoài.

**Output:** Xác định nguyên nhân chồng lấn.

# Phần 2: Thiết kế giải pháp

**CSS đề xuất:**

```css
.lesson-content, .video-list {
    box-sizing: border-box;
    padding: 16px;
    border: 1px solid #ddd;
    margin: 0;
}

.lesson-content {
    margin-bottom: 20px;
}
```

**Giải thích:**
- `box-sizing`: Tránh vượt kích thước.
- `padding`: Tạo khoảng cách bên trong.
- `margin-bottom`: Tách hai khung xếp dọc.

**Bẫy:** Chỉ tăng Margin mà không kiểm tra Padding có thể khiến giao diện tiếp tục tràn hoặc chồng lấn.

**Kết luận:** Kiểm tra Box Model bằng F12 → Elements → Computed để chỉnh CSS phù hợp.

