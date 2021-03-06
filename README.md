Understanding Git
   - Tham khảo
     1. https://git-scm.com/docs
     2. https://www.atlassian.com/git/tutorials/learn-git-with-bitbucket-cloud
     
   I. Base command line:

1. Tạo 1 directory (make directory).
   ```
       mkdir <tên thư mục 1> <tên thư mục n>
   ```
   ===
   ```
       md <tên thư mục> <tên thư mục n>
   ```
2. xóa 1 directory (remove directory).
   ```
       rd <tên thư mục 1> <tên thư mục n>
   ```
   ===
   ```
       rm -rf <tên thư mục 1> <tên thư mục n>
   ```
3. Tạo 1 file mới.
   ```
       echo "message" >> <tên file>
   ```
4. Xem files và folders trong directory.
   ```
       ls
   ```
   ===
   ```
       dir
   ```
5. Xem cả files ẩn (ví dụ: .<ten file>).
   ```
       ls -a
   ```
   ===
   ```
      ls -al
   ```
6. Di chuyển vào trong folder.
   ```
       cd nameFolder
   ```

7. Trỏ về folder trước đó.
   ```
       cd ..
   ```
8. Trỏ về thư mục gốc.
   ```
       cd ~
   ```
9. đường dẫn hiện tại (Current working directory).
   ```
       pwd
   ```
10. create .gitignore file
   ```
      touch .gitignore
   ```

II. Base Git
1. View file change or new file.
```
    git status
```
2. Add file to git.
```
    git add <ten file>
```
3. Add description.
```
    git commit
```

4. Git push.

   4.1 Push file to remote.
      ```
          git push
      ```
      u: viết tắt của "--set-upstream"
      ```
         git push -u origin <branch name>
      ```