Revert Commit
- Step 1: lấy id cần revert vể
```
    git log
```
- Step 2: reset về commit cần lấy bằng id
```
    git reset --hard <id>
```
- Step 3: Nếu muốn đổi tên lại commit (optional)
```
    git commit --amend -m 'new commit'
```
- Step 4: đẩy lại lên remote bằng push force (override)
```
    git push --force
```