# only-git

# Init
`$ git clone <url>` — clone qilib oladi

`$ git init` - **.git** papka yaratadi keyin REMOTE bilan ishlanadi odatda initdan so'ng, remote add url qilinadi

## Branch
`$ git checkout -b <branch_name>` — yangi branch yaratib unga o'tib oladi

`$ git branch -d <branch_name>` — branch o'chirish

`$ git checkout <branch_name>` — boshqa branchga o'tadi 

## Add file
`$ git add .` — file larni hammasi qo'shib yuboradi

`$ git add filename.txt` — 1ta file qo'shadi

## Commit
`$ git commit -a` — commit qiladi message beradi add qilingan file uchun va *nano* yoki *vim* ni ishga tushirib yuboradi

`$ git commit -m "my message"` - 1ta line orqali commit qiladi message beradi add qilingan file uchun

## Push
`$ git push origin <branch_name>` — remotega push qilib yuboradi

## Remote
`$ git remote` 
— remote ga ulangan narsalarni ko'rsatadi va odatda origin turgan bo'ladi

`$ git remote add <new_remote_name> <remote_url>.git`
 — yangi remote qo'shish uchun ishlatiladi

`$ git remote show <remote_name>` — remote origin haqida ma'lumot beradi


## Redo commit <a href="https://stackoverflow.com/questions/2530060/in-plain-english-what-does-git-reset-do">url</a>
`$ git reset <commit>` - commit'ni orqaga qaytaradi(preserving changes locally, local saqlab qoladi)

`$ git reset --hard <commit>` - barchasini orqaga qaytaradi hech qanday saqlashlarsiz

## Log changes
`$ git log` — barcha loglar, commitlar listi

`$ git tag -l` — tag list(version list) 


`$ git show <logid/tag>`
 — aynan o'sha logga tegishli o'zgarishlar qo'shilishlarni ko'rsatadi, commit message and more. . .


# Other hozircha aniqlanmagan
`$ git blame <filename>` — filedagi commitlar, kim yozgani, kim nima commit qilganini ko'rsatadi


`$ git pull origin master` — remote branch dan pull oladi malumot olib keladi

`$ git rebase master` — master bilan rebase qiladi qo'shib yuboradi
