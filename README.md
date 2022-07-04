Understanding Git

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
5. Git branch.

    5.1 View all branch (local and remote git).
    ```
        git branch -a
    ```
   ===
   ```
      git branch -al
   ```
    5.2 View all branch (local).
    ```
        git branch
    ```
    5.3 Create new branch and switch to new branch.
    ```
        git check -b <branch name>
    ```
    5.4 Create new a branch.
    ```
        git branch <branch name>
    ```
    5.5 Switch to a branch.
    ```
        git checkout <branch name>
    ```
   5.6 Update name branch.
   ```
      git branch -m <new branch name>
   ```
   ===
   ```
      git branch -m <old branch> <new branch>
   ```
    5.7 Delete a branch local.
    ```
        git branch -d <branch name>
    ```
   5.8 Delete a branch remote.
   ```
      git push origin -d <branch name> 
   ```
   ===
   ```
      git push origin :<branch name>
   ```
   5.9 Delete all branch local (ngoại trừ branch master).
   ```
      git branch | grep -v "master" | xargs git branch -D
   ```
   ===
   ```
      git branch -D `git branch --merged | grep -v \* | xargs`
   ```
   ===
   ```
      git branch --merged | grep -v \* | xargs git branch -D 
   ```
   ===
   ```
      git for-each-ref --format '%(refname:short)' refs/heads | grep -v "master\|main" | xargs git branch -D
   ```
   5.9.1 Delete all branch local (mà nó có branch: master-product, master-ui, master-test mà chỉ muốn để lại branch master).
   ```
      git branch | grep -v "master$" | xargs git branch -D
   ```