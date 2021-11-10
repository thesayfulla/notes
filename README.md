# only-git

# Configure tooling
`$ git config --global user.name "[name]"` - gitni yozib olgandan so'ng unga username kiritiladi(github.com dagi misol uchun)

`$ git config --global user.email "[email address]"` - email address

### Keyinchlik commit da ham shu ma'lumotlar chiqadi !

# Init
`$ git clone <url>` — clone qilib oladi

`$ git init` - **.git** papka yaratadi keyin REMOTE bilan ishlanadi odatda initdan so'ng, remote add url qilinadi

# Branch
`$ git branch <branch_name>` - yangi branch yaratadi

`$ git branch -m <oldname> <newname>` - branch nomini o'zgartirish

`$ git checkout -b <branch_name>` — yangi branch yaratib unga o'tib oladi

`$ git branch -d <branch_name>` — local branch o'chirish

`$ git push <remote_name> --delete <branch_name>` - remote branch o'chirish

`$ git checkout <branch_name>` — boshqa branchga o'tadi

`$ git switch <branch_name>` - bu ham boshqa branchga o'tadi 

# Add file
`$ git add .` — file larni hammasi qo'shib yuboradi

`$ git add filename.txt` — 1ta file qo'shadi


# View Tree

`$ git log --graph --oneline --all` - tree ko'rish uchun (magic)

# Commit
`$ git commit -a` — commit qiladi message beradi add qilingan file uchun va *nano* yoki *vim* ni ishga tushirib yuboradi

`$ git commit -m "my message"` - 1ta line orqali commit qiladi message beradi add qilingan file uchun

# Push
`$ git push` - default turgan branchga push qiladi

### push remote
`$ git push origin <branch_name>` — remote'dagi branch uchun push qilib yuboradi

`$ git push  <REMOTENAME> --tags` - remote tag uchun push qiladi

<a href="https://stackoverflow.com/questions/5195859/how-do-you-push-a-tag-to-a-remote-repository-using-git">Git push tags more information</a>


# Remote
`$ git remote` 
— remote ga ulangan narsalarni ko'rsatadi va odatda origin turgan bo'ladi

`$ git remote add <new_remote_name> <remote_url>.git`
 — yangi remote qo'shish uchun ishlatiladi

`$ git remote show <remote_name>` — remote origin haqida ma'lumot beradi

# Diff
`$ git diff` - add qilinmagan odatda o'zgartirilgan fayllarni ko'rsatadi, yani o'zgartirish qanday kiritilganini

`$ git diff <filename>` - bu aynan o'sha fayldagi o'zgarishlar `+, -` bo'lgan ishlarni ko'rsatadi


## Redo commit <a href="https://stackoverflow.com/questions/2530060/in-plain-english-what-does-git-reset-do">url</a>
`$ git reset <commit>` - commit'ni orqaga qaytaradi(preserving changes locally, local saqlab qoladi)

`$ git reset --hard <commit>` - barchasini orqaga qaytaradi hech qanday saqlashlarsiz

# Log changes
`$ git log` — barcha loglar, commitlar listi

`$ git tag -l` — tag list(version list) 

`$ git log -p <filename>` - barcha faylga tegishli o'zgarishlar commit, kim qilgani nima qo'shgani nimani o'chirganini ko'rsatadi

`$ git show <logid/tag>`
 — aynan o'sha logga tegishli o'zgarishlar qo'shilishlarni ko'rsatadi, commit message and more. . .

# Help olish
`$ git <command> --help` - ushbu komanda orqali kerakli docs malumotlar ochiladi


# Mergetool

### 1. Default shu turishi shart !
1. git dagi conlictlarni vim bilan ochishga to'g'rilash
2. conflict stilini tanlash
3. Promp ishlashi yoki yo'qligi uchun
```shell
$ git config merge.tool vimdiff
$ git config merge.conflictstyle diff3
$ git config mergetool.prompt false
```

### 2. mergetool ishga tushiriladi
`$ git mergetool`
```
  ╔═══════╦══════╦════════╗
  ║       ║      ║        ║
  ║ LOCAL ║ BASE ║ REMOTE ║
  ║       ║      ║        ║
  ╠═══════╩══════╩════════╣
  ║                       ║
  ║        MERGED         ║
  ║                       ║
  ╚═══════════════════════╝
```

- LOCAL – this is file from the current branch
- BASE – common ancestor, how file looked before both changes
- REMOTE – file you are merging into your branch
- MERGED – merge result, repoda nimani saqlash kerakligi chiqadi

### 3. Shulardan biri tanlanadi
`$ :diffg RE` - for Remote
`$ :diffg BA` - for Base
`$ :diffg LO` - for Local

### 4. Save qilamiz va commit
`$ :wqa` save qilish

`$ git commit -m "message"` - commit qilish

`$ git clean -f` - Remove extra files (e.g. *.orig) created by diff tool.

<a href="https://git-scm.com/docs/merge-config">More...</a>

# Pull
`$ git pull origin master` — remote branch dan pull oladi malumot olib keladi

# Rebase
`$ git rebase master` — master bilan rebase qiladi qo'shib yuboradi

# Blame
`$ git blame <filename>` — filedagi commitlar, kim yozgani, kim nima commit qilganini ko'rsatadi


# Other hozircha aniqlanmagan


## Links:
- <a href="https://www.youtube.com/watch?v=CRlGDDprdOQ&ab_channel=Academind">Git MERGE vs REBASE
</a>
