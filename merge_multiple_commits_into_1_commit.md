### Gộp nhiều commit thành 1 commit.
- Step 1. Kiểm tra xem cần gộp những commit nào.
```
    git log --oneline
```
- Step 2. N là số lượng commit cần gộp.
```
    git rebase -i HEAD~N
```
- Step 3. 
  - Giữ 1 từ pick đầu tiên và thay những từ pick còn lại thành s và lưu lại.
  - (Nhấn phím i để sửa và nhấn phím Esc, sau đó nhấn :wq để lưu lại).
- Step 4.
  - Xóa các nội dung mô tả cũ và thay bằng mô tả mới.
  - (Để xóa chỉ cần thêm # ở trước hoặc xóa hết các dòng mô tả).
  - (Nhấn phím i để sửa, nhấn phím Esc, sau đó nhấn :wq để lưu lại).
- Step 5. Kiểm tra lại.
```
    git log --oneline
```
- Step 6. Đẩy lại tới git (-f hoặc --force).
```
    git push --force
```