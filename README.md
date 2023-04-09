# Collaborative using Git

1. Introduction Git and Github: DONE
2. How to push and pull on Github
3. Collaborative Working
    - Review dan Pull Request
    - Code Conflict
4. FAQ Bebas

# How to Push and Pull on Github

- Prerequisites:

    - Make sure **git sudah terinstall** dalam komputer masing-masing
        - How to check:
            - Open terminal / command prompt / miniconda prompot / powershell
            - Ketik `git`, kalau sudah terinstall akan muncul ada command apa aja yang bisa digunakan
    - **Sign in** to Github account
    - Create **new repository** on Github
   
   
- Push Several Files and Folders -> Remote Repository
    - Prerequisites:
        - Folder sudah terintegrasi dengan git
            - How: `git init`
            - Check: `git status` (kita bisa check apakah ada folder .git di dalam folder kita)
            - kalau belum ada muncul error: `fatal: not a git repository (or any of the parent directories): .git`
        - Sudah ada alamat repository yang mau dituju
            - How: `git remote add origin <alamat_repository>`
            - Check: `git remote -v`
    - How:
        - **git add**
            - `git add <specific file>` -> highly recommended
            - `git add .` -> to add all files
            - `git add -u`
        - **git commit**
            - `git commit -m <commit message>`
        - **git push**
            - `git push origin master`

# Collaborative Working

- **Pull dan Clone**

    - **REMEMBER** -> `git init` and `git remote add origin <alamat repository>`
    - Pull -> Mengambil semua files di Github
        - `git pull origin master`
        - When:
            - Update code -> daily atau waktu dapet tiket baru
    - Clone ->
        - `git init`, `git remote add origin <alamat repository>`, `git pull origin master`
        - When:
            - Start new project

- **Conflict:** terjadi karena perbedaan commit history antara local dan remote

    - How:
        - `git pull origin master`
        - To solve code conflict
            - `git add`, `git commit` lagi untuk merge

- **Manage Branch**:
    - How to make a new branch
        - `git branch` -> untuk melihat ada branch apa saja
        - `git branch <nama branch>` -> membuat branch baru
        - `git checkout <nama branch>` -> pindah ke branch baru
        - `git checkout -b <nama branch>` -> membuat branch baru sekaligus pindah ke branch yang baru dibuat tersebut
